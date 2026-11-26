# CKBuilder Weekly Report — Week 11

**Author:** Tuan Ngo<br>
**Reporting date:** 26 November 2026<br>
**Status:** MVP completed<br>
**Project:** [CKB Upgrade Watch](https://github.com/vantuann205/ckb-upgradew_v1)

## Project Scope

This week I built a read-only CKB holder tool that checks how a Script refers
to code and what upgrade evidence can be verified from chain data. The MVP is
implemented as an Astro application with server-side API routes for CKB RPC
and indexer requests.

The project is a script and code-reference checker. It does not calculate
arbitrary token balances, connect a wallet, sign or submit transactions, prove
real-world ownership, monitor in the background, or send alerts.

## MVP Features

- Scan a mainnet or testnet CKB address for live Cells, capacity, Lock Scripts,
  and Type Scripts.
- Accept Script JSON with `code_hash`, `hash_type`, and `args`, including
  `data`, `data1`, `data2`, and `type` references.
- Treat data references as fixed code hashes and resolve Type references by
  searching live Type ID code Cells.
- Show the current code Cell, its lock evidence, block snapshot, and bounded
  replacement history with transaction links.
- Keep a local browser watchlist with manual re-analysis.
- Mark capped scans, missing history, ambiguous matches, unknown locks, and
  provider failures instead of turning incomplete evidence into a risk score.

## Technical Work

The API exposes `POST /api/scan` for address lookups and `POST /api/analyze`
for Script analysis. Inputs are validated server-side, requests are limited to
16 KB, provider calls have a timeout, and mainnet/testnet are selected
explicitly. Address scans stop at 500 Cells; Type ID searches stop at 2,000
live Cells; history follows at most 25 versions and 100 transaction lookups.

The analyzer distinguishes a fixed data hash from a Type ID reference. For a
Type reference it finds a unique live code Cell, reads the controlling lock,
and follows predecessor transactions when the evidence is sufficient. Multiple
matches and incomplete chains remain explicitly ambiguous or partial.

## Verification

The project source is at commit `07665c0` (`Fix Railway build and start`).
From the project directory:

```text
npm test       -> parser, address scan, chain analysis, history, ambiguity,
                 and provider-error checks passed
npm run build  -> Astro server build completed with @astrojs/node
```

The test suite uses fake RPC responses to exercise complete, empty, ambiguous,
capped, invalid-input, and provider-error paths. The production build creates
the server output successfully.

## Limitations and Next Steps

The MVP uses public CKB RPC/indexer endpoints by default and bounded searches;
a capped result is not proof that no other match exists. The current Railway
URL still serves the previous prototype, so this project has not been claimed
as a live deployment. A later phase can add provider configuration, live
deployment, integration tests against verified testnet examples, and Playwright
coverage after the MVP behavior is reviewed.

See the [Week 11 evidence index](../evidence/week-11/README.md).
