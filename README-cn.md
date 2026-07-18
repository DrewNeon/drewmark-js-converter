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

* 不支持 **DrewMark → HTML** 转换，请使用 [DrewMark JS 解析器](https://gitee.com/drewneon/drewmark-js-parser/)。
* 不支持 **Markdown → HTML** 转换，请使用专门的 Markdown 解析器。

## 快速开始

### 方式一：工程化项目（Node.js + 构建工具）

适用于使用 Webpack、Vite、Rollup 等构建工具的项目。

**1. 安装依赖**

```bash
npm install drewmark-converter
```

**2. 在源码中导入并使用**

在入口文件或组件中导入转换器及样式文件，并调用初始化函数：

```javascript
// 导入转换器
import { drewmarkConverter } from 'drewmark-converter';

const content = '# 标题\n这是一段**朱码**文本。';
const result = drewmarkConverter({
    source_text:   content,
    source_format: 'drewmark',
    target_format: 'markdown',
  }); // 实际值为：'# 标题<br>这是一段**朱码**文本。'

// 将结果渲染到页面或进行后续处理
document.getElementById('output').innerHTML = html;
```

---

### 方式二：浏览器直接调用（无构建工具）

适用于纯 HTML 页面，无需 Node.js 环境，通过 `<script>` 标签加载后，转换器会以全局变量的形式挂载。

**1. 下载依赖**

从本仓库下载 `js/drewmark-converter.min.js`、`css/drewmark-converter.min.css` 和 `lang/zh-cn.json` 至项目目录，如通过 CDN 直接引用则可跳过此步骤。

**2. 引用脚本**

两种方法二选一：

+ 引用下载到本地的脚本：
```html
<head>
  <link rel="stylesheet" href="path/to/drewmark-converter.min.css">
</head>
<script src="path/to/drewmark-converter.min.js"></script>
```

+ 从 CDN 直接引用脚本（跳过下载步骤）：
```html
<head>
  <link rel="stylesheet" href="https://unpkg.com/drewmark-converter@latest/css/drewmark-converter.min.css">
</head>
<script src="https://unpkg.com/drewmark-converter@latest/js/drewmark-converter.min.js"></script>
```

**3. 在指定容器元素中加载转换器**

```html
  <div id="my-converter"></div>
  <script>
    drewmarkConverter({ converter_id: 'my-converter' });
  </script>
```

---

## 文档

完整文档请参阅 [`docs/doc-cn.md`](docs/doc-cn.md)。

English docs: [docs/doc.md](docs/doc.md)

## 相关项目

* [朱码](https://gitee.com/drewneon/drewmark)（语法规范）
* [朱码 JS 解析器](https://gitee.com/drewneon/drewmark-js-parser)
* [朱码 JS 编辑器](https://gitee.com/drewneon/drewmark-js-editor)（所见即所得编辑器）

---

## 许可证

MIT
