# Week 8 Evidence Index

These artifacts document the local CKB-VM Spawn and IPC exercises. The four
parent/child contracts were built with the handbook Docker toolchain. The two
focused tests ran with `ckb-testtool`; no Devnet deployment was performed.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Spawn parent build](01-spawn-parent-build.png) | Build `contracts/spawn-parent` | Release build completed and binary copied to the build directory |
| [Spawn child build](02-spawn-child-build.png) | Build `contracts/spawn-child` | Release build completed and binary copied to the build directory |
| [IPC parent build](03-ipc-parent-build.png) | Build `contracts/ipc-parent` | Release build completed and binary copied to the build directory |
| [IPC child build](04-ipc-child-build.png) | Build `contracts/ipc-child` | Release build completed and binary copied to the build directory |
| [Spawn test output](05-spawn-test-output.txt) | Run `test_spawn` | Parent spawned the child, verified the pipe message, and passed |
| [IPC test](06-ipc-test.png) | Run `test_ipc` | Client received `"hello, world"`; focused test passed |
| [Second IPC test capture](07-ipc-test-second-capture.png) | Additional supplied screenshot | Duplicate capture of the same IPC output; not counted as a separate test |

## Acceptance Scope

The Week 8 acceptance scope is the four Spawn/IPC contracts and the focused
`test_spawn` and `test_ipc` tests. The full workspace suite and Devnet
deployment were not used as acceptance criteria.

The Spawn result was provided as terminal output in the conversation and is
preserved as text. Both supplied IPC screenshots are included; they show the
same test output, so the duplicate is not counted as another test.
