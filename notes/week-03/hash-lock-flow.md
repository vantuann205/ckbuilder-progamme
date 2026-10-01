# Week 3 — Hash-lock flow

## Core terms

- **Preimage:** the original secret text, `Hello World`.
- **Hash:** `blake2b-256(preimage)`. The lock stores the hash, not the readable
  preimage.
- **Witness:** transaction data supplied when spending the input Cell. The
  hash-lock contract reads the revealed preimage from the witness.
- **Lock Script:** the validator attached to the input Cell. It checks that the
  hash of the revealed preimage equals the hash in its arguments.
- **Cell dependency:** the deployed contract bytecode and `ckb-js-vm` Cells
  required to execute the validator.
- **Exit code 11:** the contract's intentional failure code for a hash mismatch.

## State transition

```text
deposit Cell
  lock args = hash("Hello World")
        |
        | witness reveals "Hello World"
        v
receiver output + change output
```

The wrong preimage fails before the input Cell is consumed. The correct
preimage authorizes the transition, pays the transaction fee, and creates the
receiver and change outputs.

## Week 3 values

- Contract deployment transaction:
  `0x767db0cea95d8e2090afd35f002f10544149137d35f523573b1f1ebc7ff5b0bd`
- Contract code hash:
  `0xcd262cb39d9e83f63e5415a56a23982fb6ae79b993e3cf371c12fad71dd23519`
- Deposit transaction:
  `0x16835d429d65544bdb79bdaaad713595546dc352209915e86c6a707ffa849967`
- Successful unlock transaction:
  `0xa2ff3a8de46082b10753314b1f096fca879c835181a890c63f82488439734bf2`
