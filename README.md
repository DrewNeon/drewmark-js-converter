<p align="center">
  <img src="images/drewmark-logo.svg" alt="DrewMark Logo">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="MIT License">
  <img src="https://img.shields.io/badge/Dependencies-0-success?style=flat-square" alt="Zero Dependencies">
  <img src="https://img.shields.io/badge/Vanilla-JS-F7DF1E?logo=javascript&logoColor=black&style=flat-square" alt="Vanilla JS">
  <img src="https://img.shields.io/badge/Size-%3C30KB-blue?style=flat-square" alt="Size">
  <img src="https://img.shields.io/badge/DM%20%E2%86%94%20MD%20%E2%86%94%20HTML-informational?style=flat-square" alt="Format Conversion">
</p>

# DrewMark JS Converter

A lightweight, zero-dependency JavaScript library that converts content between
**DrewMark**, **Markdown**, and **HTML**.

## Supported Conversions

| From     | To       |
| -------- | -------- |
| Markdown | DrewMark |
| DrewMark | Markdown |
| HTML     | DrewMark |
| HTML     | Markdown |

> **DrewMark → HTML** is not supported, please use the [DrewMark JS Parser](../../../../drewneon/drewmark-js-parser/) instead.
> **Markdown → HTML** is not supported, please use a dedicated Markdown parser instead.

## Quick Start

### Option 1: Bundled Projects (Node.js + Build Tools)

For projects using build tools such as Webpack, Vite, or Rollup.

**1. Install Dependencies**

```bash
npm install drewmark-converter
```

**2. Import and Use in Source Code**

Import the Converter and its stylesheet in your entry file or component, then call the initialization function:

```javascript
// Import the Converter
import { drewmarkConverter } from 'drewmark-converter';

const content = '# Heading\nThis is a **DrewMark** text.';
const result = drewmarkConverter({
    source_text:   content,
    source_format: 'drewmark',
    target_format: 'markdown',
  }); // the actuall value is '# Heading<br>This is a **DrewMark** text.'

// Render the result to the page or process it further
document.getElementById('output').innerHTML = html;

```

---

### Option 2: Direct Browser Usage (No Build Tools)

For plain HTML pages without a Node.js environment. When loaded via a `<script>` tag, the Converter will be mounted as a global variable.

**1. Download Library**

Download `js/drewmark-converter.min.js` and `css/drewmark-converter.min.css` from this repository into your project directory. You may skip this step if referencing directly via CDN.

**2. Include Scripts**

Choose one of the following two methods:

+ Reference the locally downloaded scripts:
```html
<head>
  <link rel="stylesheet" href="path/to/drewmark-converter.min.css">
</head>
<script src="path/to/drewmark-converter.min.js"></script>
```

+ Reference scripts directly from CDN (skips the download step):
```html
<head>
  <link rel="stylesheet" href="https://unpkg.com/drewmark-converter@latest/css/drewmark-converter.min.css">
</head>
<script src="https://unpkg.com/drewmark-converter@latest/js/drewmark-converter.min.js"></script>
```

**3. Load the Converter in the Specified Container Element**

```html
  <div id="my-converter"></div>
  <script>
    drewmarkConverter({ converter_id: 'my-converter' });
  </script>
```

---

## Documentation

See [`docs/doc.md`](docs/doc.md) for the full API reference.

中文文档: [docs/doc-cn.md](docs/doc-cn.md)

## Related Projects

* [DrewMark](../../../../drewneon/drewmark) (syntax specification)
* [DrewMark JS Parser](../../../../drewneon/drewmark-js-parser)
* [DrewMark JS Editor](../../../../drewneon/drewmark-js-editor) (WYSIWYG editor)

---

## License

MIT
