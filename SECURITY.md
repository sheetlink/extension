# Security Policy

SheetLink takes security seriously. This document outlines our security measures and how to report vulnerabilities.

## Security Architecture

### Pass-Through Design
- Bank transactions flow directly from Plaid to your Google Sheets
- Transaction data exists on our servers for less than 1 second during sync
- Your data remains under your control in your Google account

### Authentication & Authorization

**Bank Authentication (Plaid)**
- Your bank credentials go directly to Plaid - SheetLink never sees them
- Plaid handles all bank authentication securely
- Industry-standard OAuth 2.0 flow

**Google Authentication**
- Standard Google OAuth 2.0 implementation
- Minimal scope requests (only Sheets, Drive, and optional Apps Script)
- You control access via Google Account permissions

### Data Encryption

**In Transit**
- All API communication uses HTTPS/TLS encryption
- Extension to API: TLS 1.2+
- API to Google/Plaid: TLS 1.2+

**At Rest**
- Plaid access tokens encrypted with Fernet (AES-128-CBC + HMAC)
- Google OAuth tokens encrypted in database
- Transaction data never stored

### Extension Permissions

The Chrome extension requests minimal permissions:
- `storage` - Store encrypted tokens and user preferences locally
- `identity` - Google OAuth authentication
- `alarms` - Schedule automatic syncs (optional)

No permissions for:
- Reading browsing history
- Accessing other websites
- Reading clipboard
- Accessing camera/microphone

## What We Store

| Data Type | Stored? | Encrypted? | Purpose |
|-----------|---------|------------|---------|
| Bank credentials | NO | N/A | Handled by Plaid only |
| Transaction data | NO* | N/A | Pass-through to Sheets (< 1 second) |
| Plaid tokens | YES | YES | Fetch transactions |
| Google tokens | YES | YES | Write to Sheets |
| Email address | YES | NO | Account identification |
| User preferences | YES | NO | Extension settings |

*Transaction data exists in memory for less than 1 second during sync, then discarded

## Security Best Practices

### For Users

1. **Review Permissions**: Check what access you're granting in Google and Plaid flows
2. **Revoke Access**: You can revoke access anytime at [Google Account permissions](https://myaccount.google.com/permissions)
3. **Monitor Activity**: Review your Google Sheets for unexpected changes
4. **Report Issues**: See below for how to report security concerns

### For Developers

This repository contains release documentation only. Security-sensitive source code is maintained in a private repository.

## Reporting a Vulnerability

We take all security reports seriously. If you discover a security vulnerability:

**Please DO:**
- Email security concerns to: security@sheetlink.app
- Provide detailed information about the vulnerability
- Allow reasonable time for us to investigate and fix the issue
- Keep the vulnerability confidential until we've addressed it

**Please DO NOT:**
- Publicly disclose the vulnerability before we've had a chance to fix it
- Attempt to access other users' data
- Perform attacks that could harm the service or other users

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested fixes (if applicable)

### Response Timeline

- **24 hours**: Initial response acknowledging receipt
- **7 days**: Initial assessment and severity classification
- **30 days**: Target resolution for critical vulnerabilities
- **90 days**: Target resolution for non-critical vulnerabilities

## Security Updates

Security updates will be released through:
1. Chrome Web Store (automatic updates)
2. GitHub Releases (this repository)
3. Security advisories (for serious vulnerabilities)

## Third-Party Security

We rely on industry-leading security providers:

- **Plaid**: SOC 2 Type II certified, bank-level security
- **Google**: Industry-leading OAuth and API security
- **Stripe**: PCI DSS Level 1 certified payment processing

## Compliance

- Google API Services User Data Policy compliance
- HTTPS/TLS for all communications
- Principle of least privilege for all permissions
- Regular security audits and updates

## Contact

Security concerns: security@sheetlink.app
General support: support@sheetlink.app
