# Week 9 Evidence Index

**Evidence date:** 12 November 2026

These artifacts document the handbook `group_exec` example. The contract was
built locally with the pinned Docker toolchain, and the focused test ran with
`ckb-testtool`. No Devnet deployment was performed.

| Evidence | Activity | Result |
| --- | --- | --- |
| [WitnessArgs test source](01-witnessargs-source.png) | Inspect `test_group_exec` witness construction | Shows `lock`, `input_type`, and `output_type` fields for two witnesses |
| [group_exec build](02-group-exec-build.png) | Build `contracts/group_exec` | RISC-V release build completed and binary copied to `build/release` |
| [Focused test](03-group-exec-test.png) | Run `test_group_exec` | Script group and witness logs shown; 1 passed, 0 failed |

## Acceptance Scope

Week 9 acceptance covers the `group_exec` build and focused
`test_group_exec` only. The full workspace suite and Devnet deployment were not
used as acceptance criteria.
