# Loan Tracker PWA

A secure, offline-first Progressive Web App (PWA) to track personal loans and debts. Built with vanilla HTML/JS and Bootstrap 5.

## Features

-   **Secure**: All data is encrypted locally using AES-GCM with a user-defined PIN.
-   **Offline First**: Works completely offline using a Service Worker.
-   **Multi-Ledger**: Create separate ledgers for different groups (e.g., Personal, Work).
-   **Cloud Sync**: Optional backup/sync to GitHub Gists (requires a Personal Access Token).
-   **PWA**: Installable on Android and iOS. Includes shortcuts for "Borrow" and "Repay".
-   **Native Feel**: persistent login, and smooth navigation.
-   **Theming**: Light and Dark mode support.

## Usage

1.  **First Run**: Set a 6-digit PIN. This PIN is used to encrypt your data. **Do not forget it.**
2.  **Dashboard**:
    *   Add people you lend to or borrow from.
    *   Switch or manage ledgers using the top controls.
3.  **Transactions**:
    *   Click on a person to view their history.
    *   Use "Borrow" (Red) when you take money.
    *   Use "Repay" (Blue) when you pay back or lend money.
4.  **Settings**:
    *   Change currency symbol (default: $).
    *   Toggle themes.
    *   Setup GitHub Sync.
    *   Export/Import backups manually.
    *   Reset App (Wipe Data).

## Installation

### Local Development
1.  Clone the repository.
2.  Serve the folder using a local web server (e.g., `python3 -m http.server` or VS Code Live Server).
    *   *Note: Service Workers require HTTPS or localhost.*

### Production
Deploy the files to any static host:
-   GitHub Pages
-   Netlify
-   Vercel

## Technical Details

-   **Framework**: Vanilla JS, Bootstrap 5.3.
-   **Storage**: `localStorage` (encrypted JSON blob).
-   **Encryption**: Web Crypto API (PBKDF2 + AES-GCM).
-   **Routing**: Multi-page with `sessionStorage` for persistent authentication.

## Resetting

If you forget your PIN, you must reset the app, which **deletes all local data**.
-   Click "Forgot PIN? Reset App" on the lock screen.
-   Or navigate to `/reset.html` manually.
