# CKBuilder Programme

Personal development log and CKB JavaScript smart-contract workspace for the CKBuilder Programme.

## Repository purpose

This repository records practical learning, reproducible development steps, source code, and evidence from the CKB JavaScript VM track. The current work covers the OffCKB quick-start workflow on a local CKB devnet.

## Current report

- Reporting date: 2026-09-09
- Handbook area: `Introduction → Getting started on CKB → Quick start`
- Status: Completed on local devnet
- Weekly report: [2026-09-09 OffCKB Quick Start](reports/2026-09-09-offckb-quick-start.md)
- Evidence report: [Google Docs evidence report](https://docs.google.com/document/d/1qNiuSVb2z2RwFDB8u9a_m5jr9kOsDyOVnpcKqzrT_n8/edit)
- Source handbook: [CKB Builder Handbook](https://docs.google.com/document/d/1aFHXU1ZL1MyIbBAIVRjG6stqdWwPUPyHV90O1QNwY-M/edit?tab=t.0)

## Project scope

- Start a local CKB devnet with OffCKB.
- Inspect pre-funded development accounts.
- Build a TypeScript CKB JavaScript VM contract.
- Deploy the compiled contract to the local devnet.
- Preserve deployment metadata and migration artifacts.

## Repository structure

```text
contracts/       Smart-contract source code
deployment/      Deployment configuration and migration artifacts
reports/         Date-based CKBuilder development reports
scripts/         Build, deployment, and project utility scripts
tests/           Contract test sources
package.json     Project scripts and dependencies
```

## Reproducible workflow

Prerequisites: Node.js 20+, pnpm, and OffCKB.

```bash
pnpm install
offckb node
offckb accounts
pnpm run build
pnpm run deploy
```

Keep the `offckb node` process running while building or deploying to the local devnet. The deployment script targets the devnet by default and writes artifacts under `deployment/`.

## Scope note

This repository documents local-devnet work only. It is not evidence of Testnet/Mainnet deployment, production readiness, a security audit, or a passing automated test suite.

## License

MIT
