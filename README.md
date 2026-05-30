<div dir="rtl" align="right">

# خط ثمانية للويب — Thmanyah Font Web

![خط ثمانية — أصيل. حديث. مرن. حي.](./public/image.png)

**حزمة مجتمعية لعائلة خطوط ثمانية للويب — ثلاث عائلات، خمسة أوزان لكل عائلة.** أضف ملف CSS واحد لمشروعك وابدأ باستخدام ثمانية سانس، ثمانية سيريف ديسبلاي، وثمانية سيريف تكست فورًا.

> **ملاحظة:** خط ثمانية من تصميم وملكية [ثمانية](https://thmanyah.com). هذا المستودع حزمة مجتمعية تعيد تجميع الخطوط لتسهيل استخدامها على الويب عبر npm و CDN.

**[🇬🇧 Read in English](./README.en.md)**

---

## 📦 معلومات الحزمة

<div dir="ltr" align="left">

[![NPM Version](https://img.shields.io/npm/v/@engdawood/thmanyah-font-web)](https://www.npmjs.com/package/@engdawood/thmanyah-font-web)
[![Font Weights](https://img.shields.io/badge/weights-300%20·%20400%20·%20500%20·%20700%20·%20900-blueviolet)](#عائلات-الخطوط-والأوزان)

</div>

---

## 🌍 تجربة حية

🔗 [عرض خط ثمانية](https://engdawood.github.io/thmanyah-font-web/examples/demo.html)

---

## 🔗 روابط ثمانية الرسمية

| | الرابط |
|---|---|
| 🎨 **جرّب الخط** | [font.thmanyah.com](https://font.thmanyah.com/) |
| 𝕏 **إعلان الخط** | [ثمانية على X](https://x.com/thmanyah/status/2046944611969487256?s=20) |
| 📜 **ترخيص الخط** | [font.thmanyah.com/licenses](https://font.thmanyah.com/licenses) |

---

## 🚀 البداية السريعة

### الطريقة ١ — CDN (الأسرع)

أضف وسم `<link>` واحد لصفحتك. بدون تثبيت، بدون تحميل، بدون أي إعدادات.

<div dir="ltr" align="left">

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

</div>

### الطريقة ٢ — مدير الحزم

<div dir="ltr" align="left">

```bash
npm install @engdawood/thmanyah-font-web
```

```css
/* CSS */
@import "@engdawood/thmanyah-font-web";
```

```js
// JS / TS
import "@engdawood/thmanyah-font-web";
```

</div>

### الطريقة ٣ — التحميل اليدوي

انسخ مجلد `fonts/` وملف `index.css` لمشروعك، ثم اربطه في صفحتك:

<div dir="ltr" align="left">

```html
<link rel="stylesheet" href="path/to/index.css" />
```

</div>

---

## 🔤 عائلات الخطوط والأوزان

<div dir="ltr" align="left">

| Family | CSS `font-family` | Weights |
| --- | --- | --- |
| **Thmanyah Sans** | `"Thmanyah Sans", sans-serif` | 300 · 400 · 500 · 700 · 900 |
| **Thmanyah Serif Display** | `"Thmanyah Serif Display", serif` | 300 · 400 · 500 · 700 · 900 |
| **Thmanyah Serif Text** | `"Thmanyah Serif Text", serif` | 300 · 400 · 500 · 700 · 900 |

</div>

---

## 💡 أمثلة الاستخدام

### خصائص CSS مباشرة

<div dir="ltr" align="left">

```css
body {
  font-family: "Thmanyah Sans", sans-serif;
  font-weight: 400;
  direction: rtl;
}

h1, h2, h3 {
  font-family: "Thmanyah Serif Display", serif;
  font-weight: 700;
}

article p {
  font-family: "Thmanyah Serif Text", serif;
  font-weight: 400;
}
```

</div>

### الأصناف الجاهزة (Utility Classes)

<div dir="ltr" align="left">

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
| --- | --- |
| `.font-thmanyah-sans` | `font-family: "Thmanyah Sans", sans-serif` |
| `.font-thmanyah-serif-display` | `font-family: "Thmanyah Serif Display", serif` |
| `.font-thmanyah-serif-text` | `font-family: "Thmanyah Serif Text", serif` |
| `.font-weight-light` | `font-weight: 300` |
| `.font-weight-regular` | `font-weight: 400` |
| `.font-weight-medium` | `font-weight: 500` |
| `.font-weight-bold` | `font-weight: 700` |
| `.font-weight-black` | `font-weight: 900` |

</div>

---

## 📄 الترخيص

خط ثمانية من تصميم وملكية [ثمانية](https://thmanyah.com). تفاصيل الترخيص في [font.thmanyah.com/licenses](https://font.thmanyah.com/licenses).

> **⚠️ تنبيه بشأن الترخيص:** ترخيص خط ثمانية مخصص للاستخدام **الشخصي فقط**.
> **لا يُجيز** الترخيص الرسمي استضافة ملفات الخط أو إعادة توزيعها أو تقديمها من خادمك الخاص أو CDN.
> للحصول على الخط، زُر الموقع الرسمي مباشرةً: [font.thmanyah.com](https://font.thmanyah.com)
> للاستخدام المؤسسي أو ترخيص موسّع، تواصل مع ثمانية على [Ask@thmanyah.com](mailto:Ask@thmanyah.com).

حزمة الويب (إعداد CSS و CDN) بواسطة [@engdawood](https://github.com/engdawood).

</div>
