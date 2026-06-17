# SheetLink Chrome Extension

**[Available now in the Chrome Web Store](https://chromewebstore.google.com/detail/sheetlink-sync-bank-trans/niehncndbonfankgokhandgbaebdbpch)**

Official Chrome extension for [SheetLink](https://sheetlink.app) - Sync real bank transactions directly into Google Sheets. Privacy-first. Powered by Plaid.

## Overview

SheetLink connects your bank accounts to Google Sheets through a secure Chrome extension. Sync real transaction data into your spreadsheets on demand - perfect for budgeting, financial tracking, and analysis. Your bank data flows straight from Plaid to your sheet and is never stored on our servers.

## Features

- **Real Bank Data**: Connect to 12,000+ financial institutions via Plaid
- **Direct Sync**: Transactions flow straight to your Google Sheets
- **Privacy-First**: Pass-through architecture - transactions are never stored on our servers
- **You Control Sync**: On-demand sync via the extension popup - it only runs when you click
- **Smart Features**: Transaction deduplication, delta sync, Plaid AI categories
- **Recipe System**: Pre-built templates for budgeting, net worth tracking, and more

## Plans

### FREE
- **7 days** of transaction history per institution
- All 34 transaction fields
- **1 bank connection**
- On-demand sync
- Recipe library access
- **Free forever**

### PRO
- **730 days (2 years)** of transaction history per institution
- **Unlimited bank connections**
- **Excel add-in** (Microsoft AppSource)
- Historical backfill + priority support
- All FREE features included

### MAX
- Everything in Pro, plus:
- **CLI** (`sheetlink sync`) for unattended automation on your own machine (cron)
- **API keys** for programmatic access
- Output to **JSON, CSV, Postgres, and SQLite**
- **Claude / MCP** integration
- For power users piping bank data into their own systems

## Installation

- **Chrome (Google Sheets):** [Add to Chrome](https://chromewebstore.google.com/detail/sheetlink-sync-bank-trans/niehncndbonfankgokhandgbaebdbpch)
- **Excel (Pro and MAX):** [Get it on Microsoft AppSource](https://marketplace.microsoft.com/en-us/product/office/WA200010463)

## Quick Start

1. **Install Extension** - Click the "Add to Chrome" link above
2. **Sign in with Google** - Authorize Google Sheets access (write-only)
3. **Connect Your Bank** - Select from 12,000+ institutions via Plaid
4. **Link a Google Sheet** - Paste any Google Sheets URL you own
5. **Click "Sync Now"** - Your last 7 days of transactions will appear

**Need help?** Visit our guide: [sheetlink.app/get-started](https://sheetlink.app/get-started)

## Privacy & Security

- Bank credentials never touch SheetLink servers - authentication handled entirely by Plaid
- Access tokens encrypted with Fernet (AES-128-CBC + HMAC)
- Pass-through architecture - transactions go directly from Plaid to your Google Sheets
- Minimal permissions - extension only requests `storage` and `identity`
- No transaction data stored - pass-through only (less than 1 second in transit)
- JWT authentication with 60-minute expiry

See [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md) for complete details.

## Auditable & Verifiable

We publish the complete, shipped extension so anyone can verify exactly what it does:

- **Release builds** in [GitHub Releases](https://github.com/sheetlink/extension/releases) are the same packages published to the Chrome Web Store. Download a release, load it unpacked, and inspect the manifest, permissions, and code yourself.
- **Privacy and security documentation** ([PRIVACY.md](PRIVACY.md), [SECURITY.md](SECURITY.md)) describes exactly what we access and when.
- **Chrome Web Store review** independently verifies the published package.

Our developer tools are fully open source as well: the [CLI](https://github.com/sheetlink/cli), the [MCP server](https://github.com/sheetlink/mcp), and the [recipe library](https://github.com/sheetlink/sheetlink-recipes).

For security audits or commercial licensing questions, contact support@sheetlink.app.

## Support

- Website: [sheetlink.app](https://sheetlink.app)
- Issues: Report bugs or request features via GitHub Issues
- Email: support@sheetlink.app

## License

MIT License - See [LICENSE](LICENSE) for details.
