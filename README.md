# CKBuilder Programme

Personal CKBuilder development log for learning and building on Nervos CKB.

## Repository standard

This repository follows the programme requirements: one contemporaneous report per week, published on GitHub on a fixed reporting day, with honest learnings, progress, blockers, and supporting evidence.

## Weekly navigation

| Week | Focus | Status | Report |
| --- | --- | --- | --- |
| Week 1 | CKB fundamentals, local environment, and first contract | In progress | [Week 1 report](reports/week-01.md) |

Future weeks will use the same structure: `reports/week-XX.md`, `notes/week-XX/`, and `evidence/week-XX/`.

## Week 1 scope

Week 1 follows the [CKB Builder Handbook](https://docs.google.com/document/d/1aFHXU1ZL1MyIbBAIVRjG6stqdWwPUPyHV90O1QNwY-M/edit?tab=t.0):

`Introduction → Introduction to Nervos CKB → Getting started on CKB → Quick start`

It also covers the handbook's Introduction to Script material and the required start of CKB Academy Lessons 1 and 2. The [CKBuilder Terms and Conditions](https://docs.google.com/document/d/1NVnc0HPuYsFNL8dxLiLJIVoPRStYFP7xoCEO2VJ5K-s/edit?tab=t.0) require weekly GitHub reporting, course progress, scores where applicable, key learnings, and evidence.

## Repository structure

```text
contracts/       CKB JavaScript VM contract source
deployment/      Deployment configuration and migration artifacts
evidence/        Evidence grouped by onboarding or programme week
notes/           Study notes grouped by programme week
reports/         One dated report per programme week
scripts/         Build and deployment utilities
tests/           Contract test sources
```

## Development workflow

```bash
pnpm install
offckb node
offckb accounts
pnpm run build
pnpm run deploy
```

The existing [onboarding evidence report](reports/2026-09-09-offckb-quick-start.md) records the local devnet, build, and deployment completed before Week 1 began. It is supporting evidence, not a replacement for the Week 1 report.

## Scope and integrity

The repository documents local-devnet work only. It does not claim Testnet/Mainnet deployment, production readiness, security audit completion, or a passing automated test suite unless separately evidenced.
