# Week 2 Evidence Index

This directory contains the evidence referenced by the [Week 2 report](../../reports/week-02.md). Private keys are not recorded in this repository.

| Evidence | Activity | Result |
| --- | --- | --- |
| [xUDT issue](01-xudt-issued-submitted.png) | Issue custom xUDT | Transaction hash, xUDT args, token Cell capacity, lock script, and Type Script returned |
| [RPC verification](02-rpc-committed-reference.png) | `get_transaction` through OffCKB RPC proxy | Devnet transaction status returned as `committed` |
| [CCC output declaration](02-ccc-output-declared.png) | Declare a 100 CKB output | Transaction contains no input Cells yet |
| [CCC input completion](03-ccc-inputs-completed.png) | `completeInputsByCapacity()` | CCC selected 122 CKB of inputs and constructed 100 CKB plus 22 CKB outputs |

## Transaction identifiers

- xUDT issue: `0xc0b292df1cbb1b967093137ad47f159e650e1ef99ddf914dfbf20691ed2e2482`
