---
name: thmanyah-font-web
description: Add the Thmanyah (ثمانية) Arabic font family to web projects via the @dawod/thmanyah-font-web npm package or its jsDelivr CDN stylesheet. Use when the user mentions Thmanyah, ثمانية, @dawod/thmanyah-font-web, or wants Arabic webfonts (Thmanyah Sans, Serif Display, Serif Text) used in HTML, CSS, React, Vue, Next.js, or any frontend stack.
---

# Thmanyah Font Web

Community web package for the Thmanyah (ثمانية) Arabic font family: 3 families × 5 weights = 15 fonts (300/400/500/700/900), shipped as plain CSS `@font-face` rules. The font files stream from the jsDelivr CDN at runtime, so there is nothing to download or bundle.

- npm package: `@dawod/thmanyah-font-web`
- Live demo: https://engdawood.github.io/thmanyah-font-web/

## License note (tell the user)

The font is designed and owned by Thmanyah. Its license (https://font.thmanyah.com/licenses) permits personal use and does not authorize redistribution. This package is a community effort. Before using it in a commercial or client project, tell the user to check that license. Do not copy or host the font files for the user.

## Quick start (CDN, no install)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@dawod/thmanyah-font-web/index.css" />
```

`index.css` loads all three families. To load one family, use `sans.css`, `serif-display.css`, or `serif-text.css` instead.

## Install with a package manager

```bash
npm install @dawod/thmanyah-font-web
```

```js
// JS/TS entry (Vite, webpack, Next.js, ...) - all families
import "@dawod/thmanyah-font-web";

// or one family
import "@dawod/thmanyah-font-web/sans.css";
```

```css
@import "@dawod/thmanyah-font-web";
```

## Using the fonts

Always quote the family name and add a fallback.

| Family | CSS `font-family` | Best for |
| --- | --- | --- |
| Thmanyah Sans | `"Thmanyah Sans", sans-serif` | UI, body text |
| Thmanyah Serif Display | `"Thmanyah Serif Display", serif` | Headlines |
| Thmanyah Serif Text | `"Thmanyah Serif Text", serif` | Long-form reading |

Weights: 300 Light, 400 Regular, 500 Medium, 700 Bold, 900 Black. Set them numerically (`font-weight: 500`); the keywords `normal` and `bold` only reach 400 and 700.

```css
body { font-family: "Thmanyah Sans", sans-serif; font-weight: 400; }
h1, h2 { font-family: "Thmanyah Serif Display", serif; font-weight: 700; }
article p { font-family: "Thmanyah Serif Text", serif; }
```

## Utility classes (available once the CSS is loaded)

- Families: `.font-thmanyah-sans`, `.font-thmanyah-serif-display`, `.font-thmanyah-serif-text`
- Weights: `.font-weight-light`, `.font-weight-regular`, `.font-weight-medium`, `.font-weight-bold`, `.font-weight-black`

```html
<h1 class="font-thmanyah-serif-display font-weight-black">عنوان رئيسي</h1>
```

## Arabic / RTL checklist

- Set `lang="ar"` and `dir="rtl"` on `<html>` (or `direction: rtl` in CSS).
- The package CSS already sets `font-display: swap` and an Arabic + Latin `unicode-range`. Do not hand-write `@font-face` rules.

## Verify it works

1. Open devtools, Network tab, filter `woff2`: requests to `cdn.jsdelivr.net` should return 200.
2. Inspect the text: the computed `font-family` should be the Thmanyah family, not the fallback.
3. Switch weights 300 to 900 and confirm the rendering changes.
