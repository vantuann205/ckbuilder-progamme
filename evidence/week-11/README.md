# Week 11 Evidence Index

**Evidence date:** 26 November 2026

These records document the CKB Upgrade Watch MVP at source commit `07665c0`.
The checks were run locally from the project repository with Node.js 24 and
the checked-in npm lockfile.

| Evidence | Activity | Result |
| --- | --- | --- |
| [Project source](https://github.com/vantuann205/ckb-upgradew_v1/tree/07665c0533ae461224b8aac0cfdf22c8c44d8695) | Inspect the MVP implementation | Astro app, server API routes, CKB inspector, local watchlist, and bounded evidence states are present |
| `npm test` | Run `scripts/check-upgrade-watch.mjs` | Parser, address scan, chain analysis, history, ambiguity, and provider-error checks passed |
| `npm run build` | Build the Astro Node server | Production server build completed with `@astrojs/node` |

## Acceptance Scope

Week 11 acceptance covers the read-only MVP source, unit-style fake-RPC checks,
and the production build. It does not claim a live Railway deployment, a full
mainnet/testnet integration run, arbitrary token balance support, or Playwright
E2E coverage.

## Reproduction

```text
cd ckb-upgradew_v1
npm ci
npm test
npm run build
```

`npm ci` completed, but npm reported 23 audit findings in the installed
dependency tree (17 low and 6 high). Dependency remediation is outside this
Week 11 MVP report.
