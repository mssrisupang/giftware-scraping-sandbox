# GiftWare Trade Supply — scraping sandbox

Static teaching sandbox for a data-science in-class activity.
Catalogue derived from the UCI **Online Retail II** dataset
(Chen, D., 2019 — https://archive.ics.uci.edu/dataset/502/online+retail+ii),
a real UK gift-ware wholesaler's transactions, Dec 2009 – Dec 2011.

## Structure

| Path | What it is |
|---|---|
| `index.html` | landing page |
| `products/page-1.html` … `page-27.html` | catalogue, 25 listings per page, `.page-next` links |
| `product/<sku>.html` | 625 detail pages with a `table.trade-stats` |
| `data/txn-<sku>.json` | per-product transaction history (loaded client-side) |
| `.nojekyll` | disables Jekyll on GitHub Pages — do not delete |

675 listings total; a correct clean yields 625 rows.

## Deploying

**GitHub Pages**

```bash
git init && git add -A && git commit -m "sandbox site"
git branch -M main
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```
Then: repo → Settings → Pages → Source: `main`, folder: `/ (root)` → Save.
Live at `https://<you>.github.io/<repo>/` in 1–2 minutes.

**Netlify Drop** — drag this folder onto https://app.netlify.com/drop for an instant URL.

## Note

`fetch()` is blocked on `file://`, so the transaction tables only work when the
site is served over HTTP. To preview locally:

```bash
python3 -m http.server 8000
```
