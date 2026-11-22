# JUGNU Mineral Water – Mineral Water Supply Management

A simple, free web app for a home to keep track of 19-litre drinking-water bottle supplies, monthly billing and payments, and to send updates and orders to the supplier on WhatsApp. Works on Android phones and computers, with no login and no server.

Created by **Jugnu Technology**.

## Features
- **Dashboard** – this month's bottles, amount, payments, balance, current price, last supply.
- **Supplies** – add, edit and delete supplies. Each supply keeps the price that applied on its date, so a later price change never alters old records.
- **Payments** – full or partial payments per month with Paid / Partially Paid / Unpaid status.
- **Order** – send a bottle order (with the orderer's name and mobile number) to the supplier; edit or delete placed orders.
- **Reports** – daily supplies, monthly consumption and expenditure, payment history, outstanding balances, price history; print and CSV export.
- **WhatsApp** – text and colourful image updates through WhatsApp click-to-chat / the phone share menu (no WhatsApp API needed).
- **Settings** – bottle price history, supplier details, JSON backup / restore, and a **QR code** to share the app link (PNG, PDF, WhatsApp, copy, print).
- Works offline after the first visit and can be installed to the phone home screen.

## Files
| File | Purpose |
|---|---|
| `index.html` | The complete application (HTML, CSS and JavaScript in one file) |
| `manifest.webmanifest`, `icons/` | Home-screen install (name, colours, icons) |
| `sw.js` | Service worker: opens the app when offline, always loads the newest version when online |
| `_headers` | Optional security/cache headers for Cloudflare hosting (ignored by GitHub Pages) |

## Run locally
Open `index.html` in Chrome or Edge. (Offline mode, install and the share menu need the app to be served over `https://`.)

## Publish with GitHub Pages (free)
1. Create a repository on GitHub and upload all these files (keep the `icons` folder).
2. Repository **Settings → Pages → Build and deployment → Source: Deploy from a branch**, choose branch `main` and folder `/ (root)`, then **Save**.
3. After a minute the app is live at `https://<your-username>.github.io/<repository-name>/`.
4. Open it on the phone in Chrome → menu (⋮) → **Add to Home screen**.

## Publish with Cloudflare
Upload the same files (as a folder or zip with `index.html` at the top level) to Cloudflare Workers & Pages.

## Data and backup
All records are stored in the browser (IndexedDB) of the device and address where the app is opened. A new web address starts empty. To move data: **Settings → Backup (JSON)** on the old address, then **Settings → Restore** on the new one. Back up regularly.

## QR code link
The QR code in **Settings → Share App (QR Code)** is pre-set to `https://jugnu-mineralwater.jugnutech.workers.dev`. If you publish at another address, type that address in the link field in the same card and press **Save Link**.
