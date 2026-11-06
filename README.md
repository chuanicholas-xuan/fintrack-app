# FinTrack

A personal finance app for Android, iOS and the web that syncs across devices. It supports multiple accounts and currencies, shared trips, and receipt scanning.

> The source code is private. This repo holds the description, download links and releases.

## Try it

| Platform | Link |
|---|---|
| Web | **[fintrack-phi-eight.vercel.app](https://fintrack-phi-eight.vercel.app)** |
| Android | APK coming soon on the [Releases page](../../releases) |

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
