# CKBuilder Weekly Development Report

**Reporting date:** 2026-09-09  
**Programme:** CKBuilder Programme  
**Handbook area:** Introduction → Getting started on CKB → Quick start  
**Status:** Completed on a local CKB devnet

## 1. Objective

Set up a local CKB development environment with OffCKB, create and compile a TypeScript CKB JavaScript VM contract, and deploy the contract to the local devnet.

## 2. Work completed

1. Started the local CKB devnet with `offckb node`.
2. Confirmed that the devnet RPC and RPC proxy were available.
3. Confirmed that OffCKB provided development-only, pre-funded accounts.
4. Created the `hello-world` TypeScript contract project.
5. Built the contract successfully to JavaScript and CKB bytecode.
6. Deployed `hello-world.bc` to the local devnet.
7. Preserved the generated deployment configuration, migration record, and script metadata in `deployment/`.

## 3. Key learnings

- OffCKB provides a repeatable local development workflow for running a CKB devnet.
- The accounts created by OffCKB are for development and testing only.
- The project build produces both a bundled JavaScript file and a compiled CKB bytecode file.
- Deployment is performed through the project deployment script and produces artifacts that can be inspected and reused.
- The CKB JavaScript VM workflow separates contract source, build output, deployment configuration, and migration history.

## 4. Evidence summary

| Evidence ID | Activity | Result |
| --- | --- | --- |
| E1 | Local devnet startup | Verified |
| E2 | Pre-funded development accounts | Verified |
| E3 | Contract build | Verified |
| E4 | Local devnet deployment | Verified |

The complete evidence package, including the four terminal/IDE captures, is available in the [Google Docs evidence report](https://docs.google.com/document/d/1qNiuSVb2z2RwFDB8u9a_m5jr9kOsDyOVnpcKqzrT_n8/edit).

## 5. Reproduction steps

```bash
offckb node
offckb accounts
pnpm run build
pnpm run deploy
```

The local node must remain running during the account, build, and deployment checks.

## 6. Deployment record

- Network: CKB local devnet
- Contract: `hello-world.bc`
- Node RPC: `http://127.0.0.1:8114`
- RPC proxy: `http://127.0.0.1:28114`
- Transaction hash: `0x717f98ebdc961a4a5daa2cdbff938c38a5e39f2260c73ba36f738c56916ae974`
- Generated records: `deployment.toml`, migration JSON, and `deployment/scripts.json`

## 7. Challenges and limitations

The initial OffCKB setup required downloading the CKB binary and debugger components. The evidence in this report confirms the local devnet, build, and deployment workflow; it does not claim Testnet/Mainnet deployment, production readiness, a security audit, or a passing automated test suite.

## 8. Next steps

Review the next beginner exercise in the handbook, retain evidence as it is produced, and publish the next contemporaneous weekly report in this repository.

## 9. Source

[CKB Builder Handbook](https://docs.google.com/document/d/1aFHXU1ZL1MyIbBAIVRjG6stqdWwPUPyHV90O1QNwY-M/edit?tab=t.0)
