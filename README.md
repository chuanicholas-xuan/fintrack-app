# FinTrack

A personal finance app for Android, iOS and the web that syncs across devices. It supports multiple accounts and currencies, shared trips, and receipt scanning.

> The source code is private. This repo holds the description, download links and releases.

## ✨ Vibe coded

FinTrack is a **vibe-coded** app: I built it by directing an AI coding agent ([Claude Code](https://claude.com/claude-code)) rather than typing most of the code myself. My job was the product: deciding what to build, writing the requirements, reviewing the agent's work, testing every feature on a real phone and in the browser, and making the calls when things went wrong.

**From idea to a shipped app in about 10 weeks** (Aug 22 – Nov 3, 2026):

| | |
|---|---|
| Lines of TypeScript | ~37,000 |
| Commits | 38 (33 co-authored with Claude) |
| Database migrations | 26 SQL files |
| Unit test files | 19 |
| Languages in the app | 8 |
| Platforms | Android, iOS, web, from one codebase |

**How I worked with the AI**
- **Specs before code.** I had a requirements doc (SRS), high- and low-level design docs, and a roadmap written first, then built against them phase by phase.
- **Big decisions stayed mine.** For example, I moved the app from local-only storage to a Supabase cloud backend so it could sync between the phone and the web. I also turned down bundling bank logos because of trademark risk.
- **I checked the work instead of trusting it.** Features were tried out in the browser and on my phone through installable builds. Money-handling code has its own unit tests, and real-time sync was checked with two devices open side by side.
- **Guardrails for the agent.** A rules file in the project tells the agent how to work, e.g. "money is always stored as whole cents."

## Try it

| Platform | Link |
|---|---|
| Web | **[fintrack-phi-eight.vercel.app](https://fintrack-phi-eight.vercel.app)** |
| Android | **[Download the latest APK](../../releases/latest)** |

Sign up with email/password or Google. Your data syncs between the app and the website.

### Installing the APK on Android
1. Open the link above on your phone and download the `.apk`.
2. When Android asks, allow your browser to install unknown apps.
3. Open the file and tap **Install**.

## Features

- **Accounts**: bank, e-wallet, cash and credit accounts, with net worth split into assets and debt. You can archive old accounts.
- **Multi-currency**: each account has its own currency, and totals convert to your base currency using historical exchange rates.
- **Transactions**: add, edit, split, search and filter by date. You can transfer between accounts and attach photos.
- **Receipt & screenshot scanning**: snap a receipt or a payment screenshot and the app fills in the transaction for you (AI-powered).
- **Recurring payments & subscriptions**: recurring rules with service logos, reminders the day before a charge, and recurring-spend insights.
- **Budgets & goals**: budgets per category with an over-budget warning, and savings goals you fund with real transactions.
- **Trips**: shared trip pools with friends, so you can track who paid what.
- **Reports**: a category donut, a six-month trend, month-over-month change, plus PDF and CSV statements.
- **Sync & backup**: changes appear on your other devices in real time. You can also back up to and restore from a file.
- **Polish**: light and dark themes, in-app tutorials, bill reminders, and a hide-balances privacy toggle.

## What I built it with

- Expo / React Native + TypeScript (one codebase for Android, iOS and web)
- Supabase: Postgres, auth, real-time sync, and row-level security so each user sees only their own data
- Server-side Postgres functions so a balance update never half-applies
- An Edge Function using Claude for receipt scanning
- EAS Build for Android, Vercel for the web version, Sentry for crash reporting
- Unit-tested money logic (every amount is stored as whole cents, so no rounding errors)

## Screenshots

<!-- Add screenshots to a /screenshots folder and list them here, e.g.
<img src="screenshots/home.png" width="250"> -->
