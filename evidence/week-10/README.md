# Week 10 Evidence Index

**Evidence date:** 19 November 2026

These artifacts document the handbook `crypto-service-hash` example, built
with the pinned Docker toolchain and tested locally with `ckb-testtool`. No
Devnet deployment was performed.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Contract build](01-crypto-service-build.png) | Build `contracts/crypto-service-hash` | RISC-V release binary copied to `build/release` |
| [Valid witness](02-valid-witness.png) | Verify the expected witness hash | Focused test passed the valid transaction |
| [Invalid witness rejection](03-invalid-witness-rejected.png) | Replace the witness hash with 32 zero bytes | CKB rejected the transaction; focused test finished with 1 passed, 0 failed |

## Acceptance Scope

Week 10 acceptance covers the contract build and the focused
`test_crypto_service_hash` test, including its valid and invalid witness cases.
The full workspace suite was not run.
