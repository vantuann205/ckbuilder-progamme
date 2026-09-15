# Week 1 Evidence Index

This directory contains the evidence referenced by the [Week 1 report](../../reports/week-01.md). Private keys are not recorded in the report or this index.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Academy theory](01-academy-theory-completed.png) | CKB basic theoretical knowledge | Required modules completed |
| [Academy practical course](02-academy-practical-completed.png) | Basic transaction operation | Course completed and transaction packaged |
| [Local Devnet](03-offckb-devnet-running.png) | `offckb node` | Node and RPC proxy running |
| [Development accounts](04-offckb-devnet-accounts.png) | `offckb accounts` | Funded local accounts available |
| [Transfer submission](05-ckb-transfer-submitted.png) | Transfer 77 CKB | Transaction hash returned |
| [Transfer RPC details](06-transfer-rpc-details.png) | `get_transaction` | Transaction structure returned |
| [Transfer confirmation](07-transfer-rpc-committed.png) | Transaction status check | `committed` |
| [Store and read message](08-store-data-write-read.png) | Store Data on Cell | Message written and read successfully |
| [Live Cell response](09-live-cell-rpc-response.png) | `get_live_cell` | `live` |
| [Live Cell data](10-live-cell-data-details.png) | Inspect output and data | Expected data bytes returned |
| [DOB transaction](11-dob-creation-submitted.png) | Create a Spore digital object | Transaction hash returned |
| [DOB content](12-dob-content-rendered.png) | Read Spore Cell content | Stored image rendered |
| [Hash-lock build](13-hash-lock-build-success.png) | Build TypeScript contract | Bytecode generated |
| [Hash-lock deployment](14-hash-lock-deployment-success.png) | Deploy contract to Devnet | Deployment committed and artifacts synchronized |
| [Hash-lock funding](15-hash-lock-funding-transactions.png) | Deposit Devnet CKB | 130 CKB and 170 CKB deposits submitted |
| [Capacity rejection](16-hash-lock-capacity-rejection.png) | Attempt transfer with insufficient capacity | Rejected before submission |
| [Hash-lock transfer](17-hash-lock-transfer-committed.png) | Reveal matching preimage and transfer 99 CKB | `committed` |

## Transaction identifiers

- Transfer: `0xd24f08cf55176324c926da1334870d21fb4e7b8fa7bb9fcbc3ca0061665c250c`
- Store Data on Cell: `0x896399a2355a142733004a07128af84c79edf3d9c7088af399af1dd5ddbfece7`
- Create DOB: `0x2641f3bd8b97b9350c9d2d835a394cd34d5ea2c0a39f3a49fa6f2af588db1551`
- Hash-lock deployment: `0xef8578782f8add2083becd0fb29d0201e860871620a5514a2c2486493f748acf`
- Hash-lock deposit 130 CKB: `0x072da714f72aa64b3f511c2e34d68701634bd38c9c9f3d48ad1e5d2b90fcb7d8`
- Hash-lock deposit 170 CKB: `0x918125decd57721031ffb093945c6bf79e2392086b520d88b49bd5c18870f456`
- Hash-lock transfer: `0x1b68a6404e1d4744ea840f0d72128eaf1f97c889cdef6675445c9a57cae33694`
