# SheetLink Chrome Extension

**[Available now in the Chrome Web Store](https://chromewebstore.google.com/detail/sheetlink-sync-bank-trans/niehncndbonfankgokhandgbaebdbpch)**

Official Chrome extension for [SheetLink](https://sheetlink.app) - Sync real bank transactions directly into Google Sheets. Privacy-first. Powered by Plaid.

## Overview

SheetLink connects your bank accounts to Google Sheets through a secure Chrome extension. Get real transaction data automatically synced to your spreadsheets - perfect for budgeting, financial tracking, and analysis.

## Features

- **Real Bank Data**: Connect to 12,000+ financial institutions via Plaid
- **Direct Sync**: Transactions flow directly to your Google Sheets
- **Privacy-First**: Pass-through architecture - transactions are never stored on our servers
- **Manual Sync**: On-demand sync via extension popup
- **Multi-Bank Support**: Connect unlimited bank accounts
- **Smart Features**: Transaction deduplication, delta sync, Plaid AI categories
- **Recipe System**: Pre-built templates for budgeting, net worth tracking, and more

## Plans

### FREE
- **7 days** of transaction history per institution
- All 34 transaction fields
- Manual sync
- Unlimited bank accounts
- Recipe library access
- **FREE forever**

### PRO
- **730 days (2 years)** of transaction history per institution
- All 34 transaction fields
- All FREE features included

## Installation

**[Add to Chrome](https://chromewebstore.google.com/detail/sheetlink-sync-bank-trans/niehncndbonfankgokhandgbaebdbpch)**

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
- Minimal permissions - extension only requests `storage`, `identity`, and `alarms`
- No transaction data stored - pass-through only (less than 1 second in transit)
- JWT authentication with 60-minute expiry

See [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md) for complete details.

## Support

- Website: [sheetlink.app](https://sheetlink.app)
- Issues: Report bugs or request features via GitHub Issues
- Email: support@sheetlink.app

## License

This repository contains release documentation only. Extension binaries are distributed under the MIT License.

For questions about the source code or commercial licensing, contact support@sheetlink.app.
