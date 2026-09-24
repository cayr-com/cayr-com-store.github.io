# CAYR-COM — Smartphone Storefront

Modern, responsive static catalog for **CAYR-COM**, built with HTML, CSS and JavaScript. Browse iPhone, Samsung Galaxy, Google Pixel, OnePlus, Xiaomi and Nothing devices. Includes 22 catalog entries, brand filters, search, price sorting, external product-photo links where available, reference pricing and an inquiry list.

## Quick start

Open `index.html` in a browser. No Node.js dependencies or build step. To use a local server: `python -m http.server 8000`. Deploy the **contents of this folder**, not the ZIP itself, to a GitHub repository. In Settings → Pages, publish the `main` branch from `/(root)`.

## Important before publishing

- Replace both example contact numbers in `index.html`: +1 (202) 555-0143 and +1 (202) 555-0158. These are **reserved fictional numbers**, not real support lines. Do not present them as active.
- Prices are **historical published reference prices in USD**, checked 2026-09-24; they do not represent current CAYR-COM inventory or guaranteed sale prices. Verify and set your own prices, stock, shipping and tax details. Source links are attached to each listing and documented in `SOURCES.md`.
- Product photos use external third-party image URLs where available. They are **not embedded in this ZIP** because their license/host permissions have not been verified and network retrieval was unavailable. Most products show an obvious local illustrated fallback until model-specific licensed images are supplied. For reliable production display, obtain permission/license and download the correct photo of **each model** into `assets/products/`, then update the `image` field in `js/products.js` and `js/products.json`. Avoid using another model's photo.
- This is a **catalog and inquiry-list demo**, not a live store. No working checkout, payment, customer account, shipping or automatic messaging is implemented. The inquiry-list button copies products to your clipboard.
- Brand marks belong to their respective owners. The CAYR-COM logo is original SVG artwork contained in `assets/logo.svg`.

## Files

```text
index.html
README.md
SOURCES.md
assets/logo.svg
assets/image-fallback.svg
css/style.css
js/products.js
js/products.json
js/app.js
```

## Updating products

Edit product data in `js/products.js`, which is loaded directly by the page and works on `file://` and GitHub Pages. Update `js/products.json` too if maintaining a machine-readable copy. Valid categories are `iPhone`, `Samsung`, `Google Pixel`, `Other Android`. Each item has `name`, `brand`, `storage`, `price`, `source`, `image`, `tag`, `spec` and `blurb`. Edit the example numbers in `index.html` once your verified business lines are active.

## GitHub Pages URL

With owner `cayr-com` and repository `cayr-com-store.github.io`, the expected project address after publishing is `https://cayr-com.github.io/cayr-com-store.github.io/`. To use the short root domain, the repository must instead be called `cayr-com.github.io`.

© 2026 CAYR-COM. All rights reserved.
