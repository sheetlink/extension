# Google OAuth Permissions Reference

## Actual Permissions Used by SheetLink Extension

Based on Google Cloud Console OAuth configuration (as of March 2026):

### 1. See your profile info
- **Scope**: `https://www.googleapis.com/auth/userinfo.email`
- **Classification**: Non-sensitive
- **Purpose**: User authentication and account identification
- **User-facing description**: "See your profile info"

### 2. Google Sheets
- **Scope**: `https://www.googleapis.com/auth/spreadsheets`
- **Classification**: Sensitive (requires approval)
- **Purpose**: Write transaction data to user's Google Sheets
- **User-facing description**: "See, edit, create, and delete all your Google Sheets spreadsheets"

### 3. Google Drive (File-level only)
- **Scope**: `https://www.googleapis.com/auth/drive.file`
- **Classification**: Non-sensitive
- **Purpose**: Create and manage specific spreadsheets used with SheetLink
- **User-facing description**: "See, edit, create, and delete only the specific Google Drive files you use with this app"

### 4. Google Apps Script Projects
- **Scope**: `https://www.googleapis.com/auth/script.projects`
- **Classification**: Sensitive (requires approval)
- **Purpose**: Install recipe templates (optional feature)
- **User-facing description**: "Create and update Google Apps Script projects"

## Notes for Website Documentation

When updating website pages (sheetlink.app/privacy, /security, /get-started, /user-guide):

- Use these 4 permissions as the authoritative source
- These match what users see in their Google Account permissions page
- Do NOT include Chrome extension permissions (`storage`, `identity`) in OAuth scopes documentation
- Chrome extension permissions are separate from Google OAuth scopes

## Chrome Extension Permissions (separate from OAuth)

The extension manifest requests:
- `storage` - Store encrypted tokens and user preferences locally
- `identity` - Google OAuth authentication flow

These are NOT Google OAuth scopes and should be documented separately.
