# SheetLink Chrome Extension

Official Chrome extension for [SheetLink](https://sheetlink.app) - Sync real bank transactions directly into Google Sheets. Privacy-first. Powered by Plaid.

## Overview

SheetLink connects your bank accounts to Google Sheets through a secure Chrome extension. Get real transaction data automatically synced to your spreadsheets - perfect for budgeting, financial tracking, and analysis.

## Features

- **Real Bank Data**: Connect to 11,000+ financial institutions via Plaid
- **Direct Sync**: Transactions flow directly to your Google Sheets
- **Privacy-First**: Pass-through architecture - transactions are never stored on our servers
- **Automatic Updates**: Set sync schedules or sync manually anytime
- **Multi-Bank Support**: Connect multiple institutions to the same sheet
- **Recipe System**: Pre-built templates for budgeting, net worth tracking, and more

## Plans

### FREE
- 7 days of transaction history
- Manual and scheduled syncing
- Multiple bank accounts
- Full recipe library access

### PRO
- Full Plaid transaction history (up to 2 years)
- All FREE features included

## Installation

Install from the [Chrome Web Store](#) (coming soon)

## How It Works

1. Install the extension and sign in with Google
2. Connect your bank account through Plaid
3. Create or select a Google Sheet
4. Transactions sync directly to your sheet

## Privacy & Security

- Bank credentials never touch SheetLink servers - authentication handled entirely by Plaid
- Access tokens encrypted with Fernet (AES-128-CBC + HMAC)
- Pass-through architecture - transactions go directly from Plaid to your Google Sheets
- Minimal permissions - extension only requests storage and alarms
- Open authentication flow - review the security documentation

See [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md) for complete details.

## Support

- Website: [sheetlink.app](https://sheetlink.app)
- Issues: Report bugs or request features via GitHub Issues
- Email: support@sheetlink.app

## License

This repository contains release documentation only. Extension binaries are distributed under the MIT License.

For questions about the source code or commercial licensing, contact support@sheetlink.app.
