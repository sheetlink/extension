# Privacy Policy

**Effective Date:** March 2026
**Version:** 0.5.6

SheetLink is committed to protecting your privacy. This policy explains how we collect, use, and safeguard your data when you use the SheetLink Chrome extension.

## Google API OAuth Compliance Summary

SheetLink's use and transfer of information received from Google APIs adheres to [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

### Disclosure Requirements

**What data does SheetLink access?**
- Google user identity (email, profile) for authentication
- Google Sheets access to write transaction data
- Google Drive access to create and manage spreadsheets
- Google Apps Script access for recipe installation (optional)

**How is Google data used?**
- User identity: Authentication and account management only
- Spreadsheets API: Writing bank transaction data to your chosen sheets
- Drive API: Creating new sheets when requested
- Apps Script API: Installing recipe templates (only when you use the recipe feature)

**How is Google data shared?**
- SheetLink does NOT share your Google data with third parties
- Transaction data flows directly from Plaid to your Google Sheets
- Your Google email is stored securely for account management only

**Retention and deletion:**
- Google tokens are stored encrypted in our database
- You can revoke access anytime via [Google Account permissions](https://myaccount.google.com/permissions)
- Deleting your SheetLink account removes all stored Google tokens

## Data Collection and Usage

### 1. Bank Transaction Data (via Plaid)

**What we collect:**
- Transaction details: date, amount, merchant, category
- Account information: account type, balance, institution name
- This data comes from Plaid's API when you connect your bank

**How we use it:**
- Transactions are passed through to your Google Sheets in real-time
- Transaction data exists on our servers for less than 1 second during sync
- Pass-through architecture means your data is immediately discarded after sync

**Why we collect it:**
To provide the core functionality of syncing bank transactions to your spreadsheets.

### 2. Plaid Access Tokens

**What we collect:**
- Encrypted Plaid access tokens that allow us to fetch your transaction data

**How we use it:**
- Tokens are encrypted using Fernet encryption (AES-128-CBC + HMAC)
- Stored securely in our database
- Used only to fetch transactions when you trigger a sync

**Why we collect it:**
To maintain the connection between your bank and SheetLink so you can sync transactions.

### 3. Google User Information

**What we collect:**
- Google user ID
- Email address
- OAuth tokens for Google Sheets, Drive, and Apps Script APIs

**How we use it:**
- User identification and authentication
- Google tokens stored encrypted in our database
- Used to write data to your Google Sheets

**Why we collect it:**
To authenticate you and write transaction data to your Google Sheets.

### 4. Subscription Information

**What we collect:**
- Stripe customer ID
- Subscription tier (FREE or PRO)
- Billing email

**How we use it:**
- Manage your subscription status
- Determine which features you can access (7 days vs 2 years of history)

**Why we collect it:**
To provide subscription management and enforce plan limits.

## Data Storage and Security

- All sensitive data (Plaid tokens, Google tokens) encrypted at rest
- HTTPS/TLS encryption for all data in transit
- Transactions exist in memory for less than 1 second, then discarded
- Database hosted on secure infrastructure (Railway with PostgreSQL)
- JWT tokens: 60-minute expiry, browser-only (not stored on servers)

## Third-Party Services

### Plaid
- Used for bank authentication and transaction retrieval
- Your bank credentials go directly to Plaid - SheetLink never sees them
- Review Plaid's privacy policy: https://plaid.com/legal/#end-user-privacy-policy

### Google
- Used for authentication and spreadsheet access
- Review Google's privacy policy: https://policies.google.com/privacy

### Stripe
- Used for subscription payments (PRO tier only)
- Review Stripe's privacy policy: https://stripe.com/privacy

## Your Rights

You have the right to:
- **Access**: Request a copy of your data by emailing support@sheetlink.app
- **Deletion**: Delete your account and all associated data through the extension
- **Portability**: Your transaction data is already in your Google Sheets
- **Revocation**: Revoke Google or Plaid access anytime

## Data Retention

- Account data: Retained while your account is active
- After account deletion: All data permanently deleted within 30 days
- Transaction data: Not retained (pass-through only)

## Changes to This Policy

We may update this policy periodically. Changes will be posted to this page with an updated effective date.

## Contact

Questions about privacy? Email us at support@sheetlink.app

## Compliance

SheetLink complies with applicable data protection regulations including Google's API Services User Data Policy.
