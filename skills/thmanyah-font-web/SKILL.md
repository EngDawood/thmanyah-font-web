---
name: thmanyah-font-web
description: Add the Thmanyah (ثمانية) Arabic font family to web projects via the @dawod/thmanyah-font-web npm package or CDN links. Use when the user mentions Thmanyah, ثمانية, @dawod/thmanyah-font-web, or wants Arabic webfonts (Thmanyah Sans, Thmanyah Serif Display, Thmanyah Serif Text) installed or used in HTML, CSS, React, Vue, Next.js, or any frontend stack.
---

# Thmanyah Font Web

Community web package for the Thmanyah (ثمانية) Arabic font family: **3 families × 5 weights** (300/400/500/700/900), distributed as plain CSS `@font-face` rules. Font binaries stream from the jsDelivr CDN at runtime — there are no font files to download, copy, or bundle.

- npm package: `@dawod/thmanyah-font-web` (CSS only: `index.css`, `sans.css`, `serif-display.css`, `serif-text.css`)
- Live demo / visual reference: https://engdawod.github.io/thmanyah-font-web/

## Quick start (CDN — no install)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@dawod/thmanyah-font-web/index.css" />
```

`index.css` loads all three families. To load only one family, swap the filename: `sans.css`, `serif-display.css`, or `serif-text.css`. unpkg also works: `https://unpkg.com/@dawod/thmanyah-font-web/index.css`.

## Install with a package manager

```bash
npm install @dawod/thmanyah-font-web
```

```js
// JS/TS entry (Vite, webpack, Next.js, …) — all families
import "@dawod/thmanyah-font-web";

// or just one family
import "@dawod/thmanyah-font-web/sans.css";
```

```css
/* Inside a CSS file */
@import "@dawod/thmanyah-font-web";
```

## Using the fonts

Font-family names — always quoted (they contain spaces), always with a fallback:

| Family | CSS `font-family` | Best for |
| --- | --- | --- |
| Thmanyah Sans | `"Thmanyah Sans", sans-serif` | UI, body text |
| Thmanyah Serif Display | `"Thmanyah Serif Display", serif` | Headlines, large titles |
| Thmanyah Serif Text | `"Thmanyah Serif Text", serif` | Long-form reading |

Weights: `300` Light · `400` Regular · `500` Medium · `700` Bold · `900` Black. Set them numerically (`font-weight: 500`) — the keywords `normal`/`bold` only reach 400/700.

```css
body {
  font-family: "Thmanyah Sans", sans-serif;
  font-weight: 400;
}
h1, h2 {
  font-family: "Thmanyah Serif Display", serif;
  font-weight: 700;
}
article p {
  font-family: "Thmanyah Serif Text", serif;
}
```

## Utility classes (available once the CSS is loaded)

- Families: `.font-thmanyah-sans`, `.font-thmanyah-serif-display`, `.font-thmanyah-serif-text`
- Weights: `.font-weight-light` (300), `.font-weight-regular` (400), `.font-weight-medium` (500), `.font-weight-bold` (700), `.font-weight-black` (900)

```html
<h1 class="font-thmanyah-serif-display font-weight-black">عنوان رئيسي</h1>
```

## Arabic / RTL checklist

- Set `lang="ar"` and `dir="rtl"` on `<html>` (or `direction: rtl` in CSS) for Arabic content.
- The CSS already includes `font-display: swap` and Arabic + Latin `unicode-range` — no extra configuration.
- Never construct font-file URLs yourself; the package's CDN-pinned `@font-face` rules handle that.

## Verify it works

1. Load the page → devtools Network tab → filter `woff2`: requests to `cdn.jsdelivr.net` should return 200.
2. Inspect rendered text: the computed `font-family` should be the Thmanyah family, not the fallback.

## License — flag this to the user

The Thmanyah font license (https://font.thmanyah.com/licenses) permits **personal use only**; self-hosting or redistributing the font files is not permitted. This package streams fonts from a CDN instead of bundling them, but for **commercial or enterprise use** tell the user to contact Thmanyah (Ask@thmanyah.com) — do not make that call silently.
