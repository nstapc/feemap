# ₿ Bitcoin Fee Heatmap

A GitHub-contribution-style calendar heatmap of Bitcoin transaction fees over the past 365 days. Built as a single static HTML file — no backend, no build step, no dependencies to install.

![Bitcoin Fee Heatmap](https://img.shields.io/badge/data-mempool.space-orange?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

---

## Features

- 🟠 **365-day heatmap** — GitHub-style calendar showing daily median fee rates (sat/vByte)
- 💵 **USD mode** — Toggle to estimated USD cost per average transaction
- 📊 **Live stats** — Current fee, 7-day avg, 30-day avg, yearly peak, BTC price
- 🔍 **Hover tooltips** — Date, fee rate, and block count on every cell
- ⚡ **Zero build step** — Pure HTML/CSS/JS, single file
- 🌐 **Live data** — Fetches directly from [mempool.space](https://mempool.space) public API

---

## Deploy to Vercel (60 seconds)

### Option A — Vercel CLI
```bash
npm i -g vercel
vercel
```

### Option B — GitHub Import
1. Push this repo to GitHub
2. Go to [vercel.com/new](https://vercel.com/new)
3. Import your repo → click **Deploy**

No config needed. Vercel detects the static file automatically.

---

## Run Locally

```bash
# Any static server works
npx serve .
# or
python3 -m http.server 8080
```

Then open `http://localhost:8080`

---

## Data Sources

| Data | Endpoint |
|------|----------|
| Historical fee rates | `https://mempool.space/api/v1/mining/blocks/fee-rates/all` |
| Current recommended fees | `https://mempool.space/api/v1/fees/recommended` |
| BTC price (USD) | `https://mempool.space/api/v1/prices` |
| Recent blocks fallback | `https://mempool.space/api/v1/blocks` |

All data is fetched client-side. No server, no API key required.

---

## Customization

Edit the CSS variables at the top of `index.html`:

```css
:root {
  --bg:     #0c0c0c;   /* page background */
  --orange: #f7931a;   /* Bitcoin orange accent */
  /* fee heat scale: --c0 (low) through --c6 (high) */
}
```

---

## License

MIT — fork it, ship it, do whatever.
