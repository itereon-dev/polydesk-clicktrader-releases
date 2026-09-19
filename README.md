<p align="center">
  <img src="assets/social-preview.png" width="100%" alt="POLYDESK clicktrader — one-click ladder trading desktop app, compatible with Polymarket">
</p>

# POLYDESK clicktrader - ladder trading desktop app for Polymarket

**Website: [www.tradepolydesk.com](https://www.tradepolydesk.com)**

[![Latest release](https://img.shields.io/github/v/release/itereon-dev/polydesk-clicktrader-releases?label=download&sort=semver)](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases/latest)

polydesk clicktrader is a desktop trading cockpit for [Polymarket](https://polymarket.com):
a one-click price ladder in the style of exchange trading tools, plus a Grid view over all
outcomes of a market — quick take, quick cancel, size presets on hotkeys, hedge and cash-out
figures, position and P&L tracking. Built for traders who want to click on a price, not fill
in a form.

It runs on **your** computer. Your signer key and funds never touch our infrastructure;
nobody places orders on your behalf. polydesk clicktrader is independent software by
itereon GmbH and is **not affiliated with or endorsed by Polymarket**.

> **Open beta.** The app is in public beta and still moves fast — features and limits can
> change between releases. During the beta every installation has all **Plus** features at no
> builder fee; the end of the beta is announced at least 30 days in advance.

This repository is the official **download and support** channel. The application itself is
closed-source — there is no source code here, only releases, checksums, and a place to ask
questions and report problems.

---

## What's in the cockpit

- **Ladder** — one outcome, full depth. Columns for price, ASK, BID, MINE and HEDGE. Click an
  ASK cell to take, click a price or BID cell to leave a resting bid, click a blue MINE chip
  to cancel that order. The ladder auto-centres on the mid price and each panel carries a
  depth minimap, so a fast market does not run off the screen.
- **Grid** — every outcome of a market on one row: ask cells left, size in the middle, bid
  cells right, your position on the right edge, four to twelve levels per side. Clicks stage
  into the PLACE BETS ticket and are confirmed there — the map next to the ladder's scalpel.
- **Hedging and cash-out** — the HEDGE column shows the live profit or loss of closing at that
  level, computed across outcomes. **F** hedges every position at the best bid.
- **Keyboard-driven** — size presets on **1**–**8**, hedge on **F**, cancel every working
  order on **Esc**.
- **Always in view** — active positions, working orders, fills log and session tiles in the
  bottom panel; engine and price-feed status in the footer.
- **Paper mode** — the full cockpit against live market data with simulated fills. Free, no
  time limit, no wallet and no funds required.
- **ARMED / DISARMED** — the app starts disarmed; DISARM blocks all order placement instantly,
  **Esc** or **CANCEL ALL** pulls every working order at once.

Guides on the website: [tutorial](https://www.tradepolydesk.com/tutorial) ·
[ladder trading](https://www.tradepolydesk.com/ladder-trading) ·
[the Grid](https://www.tradepolydesk.com/grid-trading) ·
[learn](https://www.tradepolydesk.com/learn) ·
[FAQ](https://www.tradepolydesk.com/faq) ·
[changelog](https://www.tradepolydesk.com/changelog)

---

## Download

These links always point at the **current stable version**:

| System | Download | Also on the release page as |
|---|---|---|
| **Windows 10 / 11** (64-bit) | [polydesk-windows-x64-setup.exe](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases/latest/download/polydesk-windows-x64-setup.exe) — recommended | `polydesk_<version>_x64-setup.exe` |
| Windows (IT-managed installs) | [polydesk-windows-x64.msi](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases/latest/download/polydesk-windows-x64.msi) | `polydesk_<version>_x64_en-US.msi` |
| **macOS** (Apple Silicon — M1 or newer) | [polydesk-macos-arm64.dmg](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases/latest/download/polydesk-macos-arm64.dmg) | `polydesk_<version>_aarch64.dmg` |
| Checksums | [SHA256SUMS.txt](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases/latest/download/SHA256SUMS.txt) | |

All versions, release notes and older downloads:
**[Releases](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases)**.
Each release carries every installer twice — under the fixed name above and under a
versioned name; the files are identical.

Not available: Intel Macs, Linux. Pre-releases (`-beta`) are marked as such and never
served by the links above — use them only if you were asked to test.

### Installing (unsigned builds — read this once)

The installers are not yet code-signed, so both operating systems warn on first launch.
This is expected and not a sign of a bad download — **verify the checksum** (next
section) and then:

- **macOS:** open the `.dmg`, drag **polydesk** to *Applications*. On first launch
  Gatekeeper reports *"polydesk.app is damaged and can't be opened"* — that is the
  quarantine flag on an unsigned app, not damage. Run once in Terminal:
  `xattr -cr /Applications/polydesk.app` — then open the app normally.
- **Windows:** SmartScreen shows *"Windows protected your PC"* → **More info** →
  **Run anyway**.

### Verify your download

Every release ships a `SHA256SUMS.txt` generated by our build pipeline from the exact
files published (it lists both the fixed and the versioned file names — same hash).
Compare its line for your file with the hash of what you downloaded:

```powershell
# Windows (PowerShell)
Get-FileHash .\polydesk-windows-x64-setup.exe -Algorithm SHA256
```

```bash
# macOS (Terminal)
shasum -a 256 ~/Downloads/polydesk-macos-arm64.dmg
```

If the hash differs, delete the file and download again from this page only.

---

## First start

1. **Paper mode starts by itself.** The trading engine ships inside the app and comes up in
   paper mode with zero configuration — no wallet, no funds, no purchase. A short setup guide
   walks you through the cockpit; you can re-run it any time from the account menu.
2. **Learn the ladder there first.** Paper fills are simulated against the real market, so
   nothing is at risk while you get used to one-click entry and cancelling.
3. **Going live** takes two steps: **⚙ Settings → ACCOUNT** to store the key of your
   **dedicated trading wallet**, then the **PAPER / LIVE** pill in the top bar. Fund that
   wallet only with what you are willing to risk; never import your main wallet.
4. The in-app **? GUIDE** (footer, English and German) explains every element of the cockpit:
   markets, ladder, Grid, stakes, tickets, hedging, positions, odds formats, shortcuts.

## Plans

| | **Free** | **Plus** | **Pro** |
|---|---|---|---|
| Price | €0, no licence | flat, monthly or yearly — *to be announced* | on request |
| Trading | paper **and** live | paper and live | paper and live |
| Risk caps | $25 stake · $100 exposure per market · 5 open orders per market | set your own | set your own |
| Ladders | one at a time | Grid with unlimited ladders | unlimited |
| Sessions | current trading day | all sessions | all sessions |
| Builder fee | none | none | none |
| Support | GitHub | priority by email | priority by email |
| Setup | local | local, licence bound to one of your wallets | set up once on your own server |

Live trading is included in Free — no purchase needed to place a real order. **During the open
beta every installation runs with all Plus features at no builder fee.** Plus and Pro are
offered in unrestricted jurisdictions only. Current details:
[pricing](https://www.tradepolydesk.com/#pricing).

## How your keys and money are protected

- **Non-custodial.** Your signer key is generated and stored on your machine — in your
  operating system's keychain (macOS Keychain / Windows Credential Manager), never in a plain
  file, never sent anywhere. Orders are signed on your device by the engine inside the app,
  and no polydesk server sits in the order path. We cannot access, move or freeze your funds.
- **Risk caps.** Maximum stake per order, maximum open orders and maximum exposure per market
  are enforced by the engine itself, not by the interface.
- **Kill switch.** The app starts **disarmed**; DISARM blocks placement instantly, and
  *CANCEL ALL* / **Esc** cancel every working order.
- **Releases contain no credentials.** Everything personal is entered by you at first run and
  stays on your device.

## Requirements

- Windows 10/11 64-bit, or macOS on Apple Silicon.
- For live trading: a Polymarket account you set up yourself, with funds in its deposit
  wallet, and a dedicated trading wallet whose key you store in POLYDESK. Paper mode needs
  neither.
- An internet connection **from a jurisdiction where Polymarket permits trading**. Polymarket
  decides this from your connection, not the app; in restricted regions functionality can be
  limited to closing positions. Do **not** use a VPN or proxy to work around this — it
  violates Polymarket's terms and can cost you your account. Checking that your use is legal
  where you are is your responsibility.

## Updates

POLYDESK updates itself: shortly after launch it checks for a new version and shows an
**⬆ UPDATE** button in the footer when one is ready. Every update is cryptographically
verified before it installs, so it can only come from us. You can check manually via account
menu → *About → CHECK FOR UPDATES*. Beta builds ship often — best practice is to update
between sessions, not while orders are working.

## Privacy

The app runs locally and talks directly to Polymarket's public services for markets, prices
and your positions, plus our update server to check for new versions. **No usage telemetry and
no trading data** — no orders, positions, market data or wallet information — is collected.
Technical error and crash diagnostics can be sent to help us fix problems; they contain no key
material, balances or trading data. Details:
[privacy policy](https://www.tradepolydesk.com/privacy) and the in-app guide.

## Help, questions, bug reports

- **Bugs:** [open an issue](https://github.com/itereon-dev/polydesk-clicktrader-releases/issues/new/choose) — the template asks for the
  version (*About*), your system, mode, and the text from the 🔔 notification bell. Before
  reporting, check that the footer shows **ENGINE READY** and **PRICES LIVE** and that you are
  on the latest release. **Never post private keys, API tokens or wallet addresses.** Redact
  them from logs and screenshots before uploading.
- **Questions & how-to:** [Discussions → Q&A](https://github.com/itereon-dev/polydesk-clicktrader-releases/discussions/categories/q-a)
- **Ideas:** [Discussions → Ideas](https://github.com/itereon-dev/polydesk-clicktrader-releases/discussions/categories/ideas)
- **Release announcements:** [Discussions → Announcements](https://github.com/itereon-dev/polydesk-clicktrader-releases/discussions/categories/announcements), each
  [release](https://github.com/itereon-dev/polydesk-clicktrader-releases/releases), and
  [@tradepolydesk](https://x.com/tradepolydesk) on X.
- **Licensing, billing, privacy, Pro setup:** office@itereon.eu — see
  [support](https://www.tradepolydesk.com/support).
- **Security issues:** please report privately — see [SECURITY.md](SECURITY.md).

## Disclaimer

> POLYDESK is trading software you install and run yourself, on your own device or
> server. It is non-custodial: your keys and funds never leave your control, and we
> never place orders on your behalf or operate the software for you. It connects to
> third-party platforms with which we are not affiliated and by which we are not
> endorsed. Availability and legality vary by jurisdiction: confirming that your use
> is permitted where you are, and complying with each platform's terms, is your
> responsibility. The software must not be used to circumvent any platform's access
> restrictions. Trading involves risk of loss; nothing here is financial advice; the
> software is provided as-is, without guarantee of execution, latency, uptime or data
> accuracy.

## Legal

© 2026 itereon GmbH, Vienna. All rights reserved. POLYDESK is proprietary software; use is
governed by the [terms of service](https://www.tradepolydesk.com/terms) and the licence
agreement shown at installation. Polymarket is a trademark of its respective owner; its use
here is descriptive only. Licence notices for the open-source components POLYDESK is built
with ship inside the application (*About → Third-party licenses*).
