# Week 3 Evidence Index

This directory contains the screenshots referenced by the [Week 3 report](../../reports/week-03.md).
The evidence uses local Devnet data and contains no seed phrase or private key.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Mock tests](01-mock-tests-pass.png) | Run the hash-lock Jest tests | Correct preimage succeeds; incorrect preimage returns exit code 11 |
| [Deployment](02-deployment-success.png) | Build and deploy `hash-lock.bc` | Contract deployment committed on Devnet |
| [Deployment health](03-deployment-health-ready.png) | Frontend dependency check | Contract and `ckb-js-vm` OutPoints are live; status is `READY` |
| [Deposit submitted](04-deposit-submitted.png) | Deposit CKB to the generated hash-lock address | Deposit transaction hash returned |
| [Hash-lock funded](05-hash-lock-funded.png) | Refresh committed balance | Hash-lock Cell contains 500 CKB |
| [Wrong preimage](06-wrong-preimage-rejected.png) | Spend with an incorrect preimage | Frontend reports failure and error 11; original Cell remains live |
| [Correct preimage](07-correct-preimage-committed.png) | Spend with `Hello World` | 130 CKB transfer is committed and a transaction hash is shown |
| [RPC verification](08-rpc-committed-transaction.png) | Query `get_transaction` | Status is `committed`; inputs, outputs, cell deps, and witness are visible |

## Transaction identifiers

- Contract deployment:
  `0x767db0cea95d8e2090afd35f002f10544149137d35f523573b1f1ebc7ff5b0bd`
- Deposit:
  `0x16835d429d65544bdb79bdaaad713595546dc352209915e86c6a707ffa849967`
- Successful unlock:
  `0xa2ff3a8de46082b10753314b1f096fca879c835181a890c63f82488439734bf2`
