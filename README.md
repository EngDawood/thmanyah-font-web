# خط ثمانية للويب — Thmanyah Font Web

**[🇸🇦 اقرأ التوثيق بالعربية](./README.ar.md)**

**A community‑maintained web package for the Thmanyah (ثمانية) font family — three families, five weights each.** Drop a single CSS file into your project and start using Thmanyah Sans, Thmanyah Serif Display, and Thmanyah Serif Text immediately.

> **Note:** This is an unofficial community package. The Thmanyah font family is designed and owned by [Thmanyah (ثمانية)](https://thmanyah.com). This repo simply repackages the fonts for easy web/npm/CDN usage.

---

## 📦 Package Information

[![NPM Version](https://img.shields.io/npm/v/@engdawood/thmanyah-font-web)](https://www.npmjs.com/package/@engdawood/thmanyah-font-web)
[![NPM Downloads](https://img.shields.io/npm/dt/@engdawood/thmanyah-font-web?label=npm%20downloads)](https://www.npmjs.com/package/@engdawood/thmanyah-font-web)
[![jsDelivr Hits](https://img.shields.io/jsdelivr/npm/hm/@engdawood/thmanyah-font-web)](https://www.jsdelivr.com/package/npm/@engdawood/thmanyah-font-web)
[![License](https://img.shields.io/badge/license-OFL--1.1-blue)](./LICENSE)
[![Font Weights](https://img.shields.io/badge/weights-300%20·%20400%20·%20500%20·%20700%20·%20900-blueviolet)](#font-families--weights)

## 📊 Repository Stats

[![GitHub Stars](https://img.shields.io/github/stars/engdawood/thmanyah-font-web)](https://github.com/engdawood/thmanyah-font-web/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/engdawood/thmanyah-font-web)](https://github.com/engdawood/thmanyah-font-web/network/members)
[![GitHub Issues](https://img.shields.io/github/issues/engdawood/thmanyah-font-web)](https://github.com/engdawood/thmanyah-font-web/issues)
[![Code Size](https://img.shields.io/github/languages/code-size/engdawood/thmanyah-font-web)](https://github.com/engdawood/thmanyah-font-web)
[![GitHub last commit](https://img.shields.io/github/last-commit/engdawood/thmanyah-font-web)](https://github.com/engdawood/thmanyah-font-web/commits)

## 🔄 Compatibility

[![Browsers](https://img.shields.io/badge/browsers-Chrome%20·%20Firefox%20·%20Safari%20·%20Edge-brightgreen)](#)
[![Platforms](https://img.shields.io/badge/platforms-Windows%20·%20Mac%20·%20Linux%20·%20Android%20·%20iOS-blue)](#)
[![Maintained](https://img.shields.io/badge/maintained%3F-yes-green.svg)](https://github.com/engdawood/thmanyah-font-web/graphs/commit-activity)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/engdawood/thmanyah-font-web/pulls)

---

## 🌍 Live Demo

🎉 **Check out the live demo here:**
🔗 [Thmanyah Font Demo](https://engdawood.github.io/thmanyah-font-web/examples/demo.html)

---

## 🔗 Official Thmanyah Links

| | Link |
|---|---|
| 🎨 **Try the font** | [font.thmanyah.com](https://font.thmanyah.com/) |
| 𝕏 **Announcement** | [Thmanyah on X](https://x.com/thmanyah/status/2046944611969487256?s=20) |
| 📜 **Font License** | [font.thmanyah.com/licenses](https://font.thmanyah.com/licenses) |

---

## 🚀 Quick Start

### Option 1 — CDN (Fastest)

Add a single `<link>` tag to your HTML. No build step, no install, no download.

**jsDelivr:**

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/@engdawood/thmanyah-font-web/index.css"
/>
```

**unpkg:**

```html
<link
  rel="stylesheet"
  href="https://unpkg.com/@engdawood/thmanyah-font-web/index.css"
/>
```

### Option 2 — Package Manager

```bash
npm install @engdawood/thmanyah-font-web
```

Then import the CSS in your project:

```css
/* In your CSS */
@import "@engdawood/thmanyah-font-web";
```

```js
// Or in your JS/TS entry point
import "@engdawood/thmanyah-font-web";
```

### Option 3 — Manual Download

1. Download this repository
2. Copy the `fonts/` directory and `index.css` to your project
3. Link `index.css` in your HTML:

```html
<link rel="stylesheet" href="path/to/index.css" />
```

---

## 🔤 Font Families & Weights

| Family                   | CSS `font-family`            | Weights                              |
| ------------------------ | ---------------------------- | ------------------------------------ |
| **Thmanyah Sans**        | `"Thmanyah Sans", sans-serif` | Light 300 · Regular 400 · Medium 500 · Bold 700 · Black 900 |
| **Thmanyah Serif Display** | `"Thmanyah Serif Display", serif` | Light 300 · Regular 400 · Medium 500 · Bold 700 · Black 900 |
| **Thmanyah Serif Text**  | `"Thmanyah Serif Text", serif` | Light 300 · Regular 400 · Medium 500 · Bold 700 · Black 900 |

---

## 💡 Usage Examples

### Direct CSS Properties

```css
body {
  font-family: "Thmanyah Sans", sans-serif;
  font-weight: 400;
  direction: rtl;
}

h1,
h2,
h3 {
  font-family: "Thmanyah Serif Display", serif;
  font-weight: 700;
}

article p {
  font-family: "Thmanyah Serif Text", serif;
  font-weight: 400;
}
```

### Utility Classes

The package ships ready-made utility classes:

```html
<!-- Family classes -->
<p class="font-thmanyah-sans">ثمانية سانس</p>
<h1 class="font-thmanyah-serif-display">ثمانية سيريف ديسبلاي</h1>
<p class="font-thmanyah-serif-text">ثمانية سيريف تكست</p>

<!-- Weight classes -->
<p class="font-thmanyah-sans font-weight-light">وزن خفيف — 300</p>
<p class="font-thmanyah-sans font-weight-regular">وزن عادي — 400</p>
<p class="font-thmanyah-sans font-weight-medium">وزن متوسط — 500</p>
<p class="font-thmanyah-sans font-weight-bold">وزن سميك — 700</p>
<p class="font-thmanyah-sans font-weight-black">وزن أسود — 900</p>
```

### Utility Classes Reference

| Class                          | Effect                                      |
| ------------------------------ | -------------------------------------------- |
| `.font-thmanyah-sans`          | `font-family: "Thmanyah Sans", sans-serif`   |
| `.font-thmanyah-serif-display` | `font-family: "Thmanyah Serif Display", serif` |
| `.font-thmanyah-serif-text`    | `font-family: "Thmanyah Serif Text", serif`  |
| `.font-weight-light`           | `font-weight: 300`                           |
| `.font-weight-regular`         | `font-weight: 400`                           |
| `.font-weight-medium`          | `font-weight: 500`                           |
| `.font-weight-bold`            | `font-weight: 700`                           |
| `.font-weight-black`           | `font-weight: 900`                           |

---

## 📁 Repository Structure

```
thmanyah-font-web/
├── fonts/
│   ├── thmanyah-sans/
│   │   ├── woff2/          ← Primary web format
│   │   └── otf/            ← Fallback / desktop
│   ├── thmanyah-serif-display/
│   │   ├── woff2/
│   │   └── otf/
│   └── thmanyah-serif-text/
│       ├── woff2/
│       └── otf/
├── examples/
│   └── demo.html           ← Live demo page (GitHub Pages)
├── index.css                ← All @font-face declarations + utility classes
├── package.json
├── LICENSE                  ← OFL-1.1
└── README.md
```

---

## ⚙️ Technical Details

- **Primary format:** WOFF2 (compressed, best browser support)
- **Fallback format:** OTF/OpenType (desktop compatibility)
- **`font-display: swap`** — text is visible immediately, font loads in background
- **`unicode-range`** — covers Arabic (U+0600–06FF, U+0750–077F, U+08A0–08FF, U+FB50–FDFF, U+FE70–FEFF) and Basic Latin (U+0020–02AF)
- **RTL-ready** — designed and optimized for right-to-left layouts

---

## 📄 License

The Thmanyah font family is licensed under the **[SIL Open Font License, Version 1.1](./LICENSE)**.

- ✅ Free to use in personal and commercial projects
- ✅ Can be bundled with any software
- ✅ Can be modified and redistributed
- ❌ Cannot be sold by itself

**Font design & copyright © [Thmanyah (ثمانية)](https://thmanyah.com)** — all rights to the font belong to them.
**Community web package by [@engdawood](https://github.com/engdawood)** — this repo only repackages the fonts for web usage.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request
