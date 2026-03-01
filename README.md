# ₿ Bitcoin Fee Heatmap

A GitHub-contribution-style calendar heatmap of Bitcoin transaction fees over the past 365 days. Built as a single static HTML file — no backend, no build step, no dependencies to install.

![Bitcoin Fee Heatmap](https://img.shields.io/badge/data-mempool.space-orange?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

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