<p align="center">
  <img src="images/logo.png" alt="DrewMark Logo">
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

```html
<link rel="stylesheet" href="css/drewmark-converter.min.css">
<div id="my-converter"></div>
<script src="js/drewmark-converter.min.js"></script>
<script>
  drewmarkConverter({ converter_id: 'my-converter' });
</script>
```

## Headless Usage

```javascript
var result = drewmarkConverter({
  source_text:   '# Hello **World**',
  source_format: 'markdown',
  target_format: 'drewmark',
});
// result: '# Hello **World**'
```

## Documentation

See [`docs/doc.md`](docs/doc.md) for the full API reference.

中文文档: [docs/doc-cn.md](docs/doc-cn.md)

## Related Projects

[DrewMark](../../../../drewneon/drewmark) (syntax specification)
[DrewMark JS Parser](../../../../drewneon/drewmark-js-parser)
[DrewMark JS Editor](../../../../drewneon/drewmark-js-editor) (WYSIWYG editor)

---

## License

MIT
