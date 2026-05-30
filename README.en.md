# خط ثمانية للويب — Thmanyah Font Web

![خط ثمانية — أصيل. حديث. مرن. حي.](./public/image.png)

**[🇸🇦 اقرأ التوثيق بالعربية](./README.md)**

A community-maintained web package for the Thmanyah (ثمانية) font family — three families, five weights each. Drop a single `<link>` or CSS import into your project and start using the fonts immediately. No font files are bundled — fonts are served via jsDelivr CDN from this repository.

> The Thmanyah font family is designed and owned by [Thmanyah (ثمانية)](https://thmanyah.com). This is a community package that provides a convenient CSS wrapper for web usage.

---

[![NPM Version](https://img.shields.io/npm/v/@engdawood/thmanyah-font-web)](https://www.npmjs.com/package/@engdawood/thmanyah-font-web)
[![NPM Downloads](https://img.shields.io/npm/dt/@engdawood/thmanyah-font-web?label=npm%20downloads)](https://www.npmjs.com/package/@engdawood/thmanyah-font-web)
[![jsDelivr Hits](https://img.shields.io/jsdelivr/npm/hm/@engdawood/thmanyah-font-web)](https://www.jsdelivr.com/package/npm/@engdawood/thmanyah-font-web)
[![License](https://img.shields.io/badge/license-Thmanyah%20Font%20License-blue)](#license)

---

## Quick Start

### CDN — no install needed

**All three families:**
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@engdawood/thmanyah-font-web/index.css" />
```

**Sans only:**
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@engdawood/thmanyah-font-web/sans.css" />
```

**Serif Display only:**
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@engdawood/thmanyah-font-web/serif-display.css" />
```

**Serif Text only:**
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@engdawood/thmanyah-font-web/serif-text.css" />
```

### npm

```bash
npm install @engdawood/thmanyah-font-web
```

```js
// All families
import "@engdawood/thmanyah-font-web";

// Or import only what you need
import "@engdawood/thmanyah-font-web/sans.css";
import "@engdawood/thmanyah-font-web/serif-display.css";
import "@engdawood/thmanyah-font-web/serif-text.css";
```

```css
/* In CSS */
@import "@engdawood/thmanyah-font-web";
@import "@engdawood/thmanyah-font-web/sans.css";
```

---

## Font Families & Weights

| Family | CSS `font-family` | Weights |
|--------|-------------------|---------|
| **Thmanyah Sans** | `"Thmanyah Sans", sans-serif` | 300 · 400 · 500 · 700 · 900 |
| **Thmanyah Serif Display** | `"Thmanyah Serif Display", serif` | 300 · 400 · 500 · 700 · 900 |
| **Thmanyah Serif Text** | `"Thmanyah Serif Text", serif` | 300 · 400 · 500 · 700 · 900 |

---

## Usage

### CSS

```css
body {
  font-family: "Thmanyah Sans", sans-serif;
  font-weight: 400;
  direction: rtl;
}

h1 {
  font-family: "Thmanyah Serif Display", serif;
  font-weight: 700;
}

article p {
  font-family: "Thmanyah Serif Text", serif;
  font-weight: 400;
}
```

### Utility Classes

```html
<!-- Family -->
<p class="font-thmanyah-sans">ثمانية سانس</p>
<h1 class="font-thmanyah-serif-display">ثمانية سيريف ديسبلاي</h1>
<p class="font-thmanyah-serif-text">ثمانية سيريف تكست</p>

<!-- Weight -->
<p class="font-thmanyah-sans font-weight-light">300</p>
<p class="font-thmanyah-sans font-weight-regular">400</p>
<p class="font-thmanyah-sans font-weight-medium">500</p>
<p class="font-thmanyah-sans font-weight-bold">700</p>
<p class="font-thmanyah-sans font-weight-black">900</p>
```

| Class | Value |
|-------|-------|
| `.font-thmanyah-sans` | `font-family: "Thmanyah Sans", sans-serif` |
| `.font-thmanyah-serif-display` | `font-family: "Thmanyah Serif Display", serif` |
| `.font-thmanyah-serif-text` | `font-family: "Thmanyah Serif Text", serif` |
| `.font-weight-light` | `font-weight: 300` |
| `.font-weight-regular` | `font-weight: 400` |
| `.font-weight-medium` | `font-weight: 500` |
| `.font-weight-bold` | `font-weight: 700` |
| `.font-weight-black` | `font-weight: 900` |

---

## Official Thmanyah Links

| | Link |
|---|---|
| Try the font | [font.thmanyah.com](https://font.thmanyah.com/) |

---

## License

The Thmanyah font family is designed and owned by [Thmanyah (ثمانية)](https://thmanyah.com). Font license details at [font.thmanyah.com/licenses](https://font.thmanyah.com/licenses).

> **⚠️ License Notice:** The Thmanyah font license permits **personal use only**.
> Self-hosting, redistributing, or serving the font files from your own server or CDN is **not permitted** under the official license.
> Download the font directly from [font.thmanyah.com](https://font.thmanyah.com) for use on your own devices and projects.
> For enterprise or extended licensing, contact Thmanyah at [Ask@thmanyah.com](mailto:Ask@thmanyah.com).

This package (CSS wrapper + CDN setup) is maintained by [@engdawood](https://github.com/engdawood).
