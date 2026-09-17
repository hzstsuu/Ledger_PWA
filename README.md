# Ledger — PWA version

This folder keeps the existing Ledger HTML application and adds the files needed
to run it as an installable web app.

Files:
- index.html — your Ledger application
- manifest.webmanifest — app name, icon, install behavior
- sw.js — offline caching/service worker
- icon.svg — Ledger app icon

IMPORTANT:
A service worker requires a secure web context (normally HTTPS) or localhost.
Do not test the installable PWA by double-clicking index.html with file://.

Recommended local test:
1. Open this folder in VS Code.
2. Start a local web server (for example, VS Code Live Server).
3. Open the localhost address in Chrome/Edge.
4. Test the Ledger normally.
5. On a supported browser, use the browser's Install/Add to Home Screen option.

For phone use:
Deploy the folder to an HTTPS static host, open the HTTPS URL on your phone,
then choose Add to Home Screen / Install App.

The app's existing localStorage + IndexedDB data model is retained. This means
data remains device/browser-local; installing the PWA does NOT automatically
synchronize data between your laptop and phone.
