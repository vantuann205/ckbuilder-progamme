# Week 4 — Rust Simple Lock and CKB-VM

## Scope

Week 4 moved from using the JavaScript hash-lock dApp to reading and testing
the Rust implementation with `ckb-testtool` and CKB-VM. The work stayed local:
there was no Devnet deployment.

## Execution model

```text
Rust contract
  -> RISC-V binary
  -> CellDep in the mock transaction
  -> CKB-VM
  -> Script reads args and GroupInput witness
  -> return code
```

The Simple Lock contract stores the expected Blake2b-256 hash in `script.args`.
The spending transaction supplies a preimage in `WitnessArgs.lock`. The
contract hashes that preimage and returns:

- `0` when the hash matches;
- `11` when the preimage is present but does not match;
- `10` when the witness/preimage or script arguments fail validation.

## Key concepts

- **Witness:** transaction data supplied to the Script at spend time.
- **Script args:** Script-specific configuration attached to the lock Script.
- **Script group:** inputs or outputs using the same Script, evaluated together.
- **GroupInput:** the input side of the current Script group; Simple Lock reads
  its first `WitnessArgs`.
- **CellDep:** a referenced Cell containing the Script bytecode. It supplies
  code and is not consumed like a transaction input.
- **CKB-VM:** the VM that executes the compiled RISC-V Script and checks its
  return code and cycle limit.

## Validation change

The Simple Lock check was tightened so malformed inputs fail explicitly:

```text
args length != 32 bytes -> error 10
missing or empty witness lock -> error 10
non-matching preimage -> error 11
matching preimage -> success
```

The added missing-preimage test confirms the new error-10 path.
