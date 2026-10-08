# Week 4 Evidence Index

These screenshots document the local Rust/CKB-VM work. Devnet deployment was
intentionally skipped because Week 4 is a local Script execution exercise.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Rust build artifacts](01-rust-build-artifacts.png) | Build with the handbook Docker toolchain | `build/release/simple-lock` and `build/release/group_exec` exist |
| [Simple Lock baseline](02-simple-lock-baseline-tests.png) | Run the original Simple Lock tests | Correct preimage passes; wrong preimage is rejected; 2 passed |
| [Script group test](03-script-group-test.png) | Run `test_group_exec` | Group lock/type witness logging is shown; 1 passed |
| [Simple Lock validation](04-simple-lock-validation-tests.png) | Run the updated Simple Lock tests | Correct, wrong, and missing-preimage cases pass; 3 passed |

## Acceptance scope

The Week 4 acceptance scope is the Rust `simple-lock` contract and the
`group_exec` script-group example. The complete workspace test suite was not
used as the acceptance command because it also covers unrelated handbook
contracts and requires every example binary to be built.
