# Security policy

POLYDESK handles wallet keys and places real orders. If you find a way to weaken that —
key exposure, order manipulation, bypassing the risk limits, a tampered update — we
want to know **privately, first**.

## Reporting

- Preferred: **[Report a vulnerability](https://github.com/itereon-dev/polydesk-clicktrader-releases/security/advisories/new)** (GitHub
  private vulnerability reporting — only maintainers see it).
- Or email **admin@itereon.eu** with "SECURITY" in the subject.

Please include the POLYDESK version (*About*), your operating system, and steps to
reproduce. **Do not include private keys, API tokens, or wallet addresses** — describe
the issue, do not demonstrate it with your own credentials.

Please do **not** open a public issue for security problems.

## What to expect

- Acknowledgement within 3 business days.
- We keep you informed while we investigate and fix, and credit you in the release
  notes if you wish.
- Fixes ship as a regular release; installed apps receive them via the built-in,
  signature-verified updater.

## Scope

- The POLYDESK desktop application and the trading engine bundled inside it.
- Our update service and the integrity of published installers (every release carries
  `SHA256SUMS.txt`; updates are verified against a signing key embedded in the app).

Out of scope: Polymarket's own platform, APIs and smart contracts — report those to
Polymarket directly.
