# Garment Order Manager — first version

## Included
- Customer and vendor records (GSTIN, contact, address, category, transport, follow-up)
- Order register (customer, product, quantity, rate, GST %, advance, due date, status, product photo)
- Dispatch register (order, transport, LR/AWB, boxes, dispatch and delivery dates, status, photo)
- Search, edit, delete, dashboard and JSON backup/restore
- Offline app shell after first successful load

## Important storage note
This starter version stores records in the browser's IndexedDB on the iPhone. It does not sync to iCloud, Google Sheets, or another device. Export a backup regularly using More → Export backup. Avoid clearing Safari website data. This version has no login or server-side security; keep the phone locked and do not share the hosted app URL if that matters to your business.

## Free iPhone installation (GitHub Pages)
1. On a computer, create/sign in to a free GitHub account at github.com.
2. Create a new **public** repository named `garment-order-manager`.
3. Upload all five files from this folder: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.
4. In the repository, open **Settings → Pages**. Under Build and deployment choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish. The URL will look like `https://YOUR-USERNAME.github.io/garment-order-manager/`.
6. On your iPhone, open that URL in **Safari** (not an in-app browser). Tap Share → **Add to Home Screen** → Add.
7. Launch the new home-screen icon. Add a test customer and order, then use More → Export backup.

GitHub Pages hosting is free for a public repository. The repository contains the app code, not your business records. Records are stored locally in Safari on the iPhone.

## Notes
- Use GST % as the rate applicable to the order; this is a follow-up register, not GST invoicing/accounting software.
- AWB/LR are stored as text; this starter version does not automatically query courier tracking websites.
- Product/dispatch photos are stored locally with the record. Large photos can use substantial iPhone storage; each upload is limited to 5 MB.
