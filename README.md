# Data Formatter

> A zero-dependency, single-file data formatter that runs entirely in the browser.  
> 零依赖、单文件、纯浏览器运行的数据格式化工具。

![Version](https://img.shields.io/badge/version-1.3-6c6ef5)
![License](https://img.shields.io/badge/license-MIT-4ecca3)
![No Dependencies](https://img.shields.io/badge/dependencies-none-success)

---

## ✨ Features / 功能亮点

| Feature | Description |
|---|---|
| 🎨 **Multi-format** | JSON · XML · HTML · SQL · YAML · CSV · KV Headers |
| 🔧 **Auto-repair** | Fixes malformed JSON (missing brackets, trailing commas, unquoted keys, single quotes) and broken XML |
| 🌈 **Syntax highlighting** | Input panel highlights in real-time as you type |
| 🔗 **Bracket matching** | Click any bracket/tag to highlight its matching pair, color-coded by nesting depth |
| 🌙 **Dark / Light theme** | Slide toggle, transitions smoothly |
| 🌐 **EN / ZH language** | Full UI localization, slide toggle |
| 📦 **Compress & Restore** | One-click minify for input or output; restore formatted view at any time |
| 📋 **Copy & Download** | Copy raw or compressed output; download with the correct file extension |
| ⚡ **Auto-format on paste** | Paste → instantly formatted; Enter key also triggers format |
| 📱 **Responsive** | Works on mobile (stacked layout below 700 px) |

---

## 🚀 Usage / 使用方法

No installation needed. Just open `index.html` in any modern browser.

```bash
# Clone and open
git clone https://github.com/Flywe/data-formatter.git
cd data-formatter
open index.html   # macOS
start index.html  # Windows
```

Or use it directly via **GitHub Pages** — [Live Demo](https://flywe.github.io/data-formatter/)

---

## 📸 Screenshot

| Dark Theme | Light Theme |
|---|---|
| *(paste data, see instant highlight and format)* | *(toggle the ☀️ switch in the header)* |

---

## 🗂️ Supported Formats

### JSON
- Standard JSON formatting with 4-space indent
- **Auto-repair**: trailing commas, unquoted keys, single-quoted strings, unclosed brackets, missing opening `{` or `[`

### XML
- Full pretty-print with attribute highlighting  
- Auto-wraps structurally broken XML in a root element to recover content

### HTML
- Formats full documents and fragments  
- Browser's DOMParser handles unclosed tags gracefully

### SQL
- Breaks major clauses (`SELECT`, `FROM`, `WHERE`, `JOIN`, `GROUP BY` …) onto new lines  
- Highlights keywords, functions, strings, and numbers

### YAML
- Key highlighting with comment support

### CSV
- Auto-detects delimiter (`,` `\t` `;`)  
- Renders as an aligned ASCII table with a header divider

### KV (HTTP Headers / Config pairs)
- Detects `[key=value;key=value;…]` style data (e.g. API request headers)  
- Formats as a padded key = value table; long values (tokens, JWTs) shown in a distinct color

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|---|---|
| `Enter` | Format |
| `Shift + Enter` | Insert newline |
| `Ctrl / ⌘ + Enter` | Format (alternative) |

---

## 📋 Changelog

### v1.3 · 2026-06-04
- Dark / Light theme toggle with slide animation
- EN / ZH language toggle with slide animation
- Auto-repair non-standard formats: malformed JSON (missing opening bracket, trailing commas, unquoted keys), broken XML
- New **KV** format detection and formatting for HTTP-header-style data

### v1.2 · 2026-06-03
- 4-space indentation
- Input-side compress / restore
- Rainbow bracket coloring by nesting depth; click to highlight matching pair

### v1.1 · 2026-06-01
- JSON, XML, HTML, SQL, YAML, CSV formatting
- Enter to format · Shift+Enter for newline

---

## 🛠️ Technical Notes

- **Pure HTML / CSS / JS** — one file, no build step, no framework, no CDN
- All parsing uses browser-native APIs: `JSON.parse`, `DOMParser`
- Input highlight layer is a `<div>` positioned under a transparent `<textarea>`, keeping cursor alignment pixel-perfect
- Bracket IDs are assigned in a pre-pass so matching is O(n) with no DOM queries at click time

---

## 📄 License

MIT © 2026 [Flywe](https://github.com/Flywe) — free to use, modify, and distribute.
