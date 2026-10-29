# Week 7 Evidence Index

These screenshots document the local Rust `script-hash` and `tx-hash`
exercise. The contract build and focused syscall tests were run with the
handbook Docker toolchain and `ckb-testtool`; no Devnet deployment was needed.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Script hash implementation](01-script-hash-source.png) | Inspect the `load_script` and `load_script_hash` checks | The current Script hash is calculated and compared with the syscall value |
| [Script hash build](02-script-hash-build.png) | Build `contracts/script-hash` with the Docker toolchain | Release compilation completed and the binary was copied to `build/release` |
| [Focused syscall tests](03-syscall-tests.png) | Run the `test_syscalls` module | Lock Script, Input Type Script, and transaction hash paths pass; 4 tests passed |
| [Focused test details](04-syscall-test-details.png) | Inspect the scripted hash test cases and result | The suite finishes with `4 passed; 0 failed` |

## Acceptance scope

The Week 7 acceptance scope is the Rust `script-hash` and `tx-hash` examples,
exercised through `tests/src/test_syscalls.rs`. The full workspace suite,
Devnet deployment, and the contract's output Type Script debug branch were not
used as acceptance criteria.
