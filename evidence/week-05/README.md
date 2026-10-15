# Week 5 Evidence Index

These screenshots document the local Rust SUDT build and targeted tests.
Devnet deployment was intentionally skipped because this week's scope is local
Type Script execution with `ckb-testtool`.

| Evidence | Activity | Result |
| --- | --- | --- |
| [SUDT build](01-sudt-build-success.png) | Build `contracts/sudt` with the pinned Docker toolchain | `sudt` and `sudt.debug` are produced |
| [SUDT targeted tests](02-sudt-tests-pass.png) | Run `test_sudt` | Transfer, owner mode, and over-issue rejection pass; 3 passed |

## Acceptance scope

The Week 5 acceptance scope is the handbook Rust SUDT Type Script and
`tests/src/test_sudt.rs`. The full workspace suite and Devnet deployment were
not used as acceptance criteria.
