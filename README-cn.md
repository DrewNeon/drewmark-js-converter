<p align="center">
  <img src="images/logo.png" alt="朱码标志">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="MIT 许可证">
  <img src="https://img.shields.io/badge/Dependencies-0-success?style=flat-square" alt="零依赖">
  <img src="https://img.shields.io/badge/Vanilla-JS-F7DF1E?logo=javascript&logoColor=black&style=flat-square" alt="Vanilla JS">
  <img src="https://img.shields.io/badge/Size-%3C30KB-blue?style=flat-square" alt="体积">
  <img src="https://img.shields.io/badge/DM%20%E2%86%94%20MD%20%E2%86%94%20HTML-informational?style=flat-square" alt="格式转换">
</p>

# 朱码 JS 转换器

轻量级、无依赖的 JavaScript 库，支持 **DrewMark**、**Markdown** 和 **HTML** 三种格式之间的互相转换。

## 支持的转换方向

| 源格式    | 目标格式 |
| -------- | -------- |
| Markdown | DrewMark |
| DrewMark | Markdown |
| HTML     | DrewMark |
| HTML     | Markdown |

* 不支持 **DrewMark → HTML** 转换，请使用 [DrewMark JS 解析器](/drewneon/drewmark-js-parser/)。
* 不支持 **Markdown → HTML** 转换，请使用专门的 Markdown 解析器。

## 快速入门

```html
<link rel="stylesheet" href="css/drewmark-converter.min.css">
<div id="my-converter"></div>
<script src="js/drewmark-converter.min.js"></script>
<script>
  drewmarkConverter({ converter_id: 'my-converter' });
</script>
```

## 无界面模式

```javascript
var result = drewmarkConverter({
  source_text:   '# 欢迎 **朱码**',
  source_format: 'markdown',
  target_format: 'drewmark',
});
```

## 文档

完整文档请参阅 [`docs/doc-cn.md`](docs/doc-cn.md)。

English docs: [docs/doc.md](docs/doc.md)

## 相关项目

[朱码](/drewneon/drewmark)（语法规范）
[朱码 JS 解析器](/drewneon/drewmark-js-parser)
[朱码 JS 编辑器](/drewneon/drewmark-js-editor)（所见即所得编辑器）

---

## 许可证

MIT
