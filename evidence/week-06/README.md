# Week 6 Evidence Index

These screenshots document the local Rust Type ID build and targeted test.
Devnet deployment was intentionally skipped because this week's scope is local
Type ID verification with `ckb-testtool`.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Type ID compilation](01-type-id-build-compile.png) | Compile `contracts/type-id` with the pinned Docker toolchain | Release compilation completed successfully |
| [Type ID artifacts](02-type-id-artifacts.png) | Inspect the release build directory | `type-id` and `type-id.debug` are present |
| [Type ID targeted test](03-type-id-test-pass.png) | Run `test_type_id_minting` | 1 test passed |

## Acceptance scope

The Week 6 acceptance scope is the handbook Rust Type ID contract and
`tests/src/test_type_id.rs`. The full workspace suite, Devnet deployment, and
custom negative tests were not used as acceptance criteria.
