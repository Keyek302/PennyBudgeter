# Penny Budgeter

<img src="icons/icon-192.png" alt="Penny the coin" width="96" align="right">

Enter your monthly pay and bills, and Penny shows you where the money goes.

## Features

- **Four views of your budget:** bar, donut chart, balance scale, and jar. Switch between them with one tap.
- **Daily spending allowance:** your leftover money spread over the days left in the month.
- **Bill calendar:** see which days your bills are due.
- **Taxes menu:** enter the percentage taken out of each check to see your take-home pay.
- **Savings goal tracker:** shows progress and how many months it takes at your current leftover.
- **Budget health meter:** Penny the coin character goes from thrilled to stressed as bills approach your pay.
- **Installable and offline:** works as an app on your phone or desktop. No accounts, no ads, no tracking. Your numbers stay in your browser.

## Run it

It is a plain static site: `index.html`, a manifest, a service worker, and icons. No build step.

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000. The service worker and install prompt only work over `http://localhost` or `https`.

## Deploy with GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. Your app appears at `https://<your-username>.github.io/<repo-name>/` after a minute or two.

## Install it

- **iPhone or iPad (Safari):** Share, then **Add to Home Screen**.
- **Android (Chrome):** menu, then **Install app**.
- **Desktop (Chrome or Edge):** click the install icon in the address bar.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: layout, styles, and logic |
| `manifest.webmanifest` | Name, colors, and icons for installing |
| `sw.js` | Service worker that caches the app for offline use |
| `icons/` | App icon as SVG and PNG, including a maskable version for Android |

## Notes

- Taxes are a single flat percentage, so the result is a rough estimate.
- The Nunito font loads from Google Fonts when online. Offline, the app falls back to your system font.
- When you change the app files, bump `CACHE` in `sw.js` (for example to `penny-v2`) so installed copies update.

## License

MIT
