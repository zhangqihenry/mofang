<div align="center">

# 墨方 MoFang

一个纯静态、单文件的 Markdown 编辑器
A purely static, single-file Markdown editor

</div>

墨，谐音 Markdown 的首音。方，取方案之意。墨方即一种 Markdown 解决方案。
墨 (mò) means ink and echoes the first sound of _Markdown_. 方 (fāng) means
_solution_. Together: a Markdown solution.

墨方是一个 Markdown 编辑器。整个应用是一个静态 HTML 文件，下载后用浏览器打开即可使用。没有后端，无需登录，离线可用。
MoFang is a Markdown editor. The entire application is a single static HTML
file: download it and open it in a browser. No backend, no login, works
offline.

## 为什么开发墨方 / Why MoFang

Markdown 编辑器数量众多。墨方与其他编辑器的区别如下：
Markdown editors are plentiful. These are MoFang's distinguishing choices:

- **单文件运行**。整个应用打包为一个 HTML 文件，没有服务器、没有账号、没有安装过程。文稿与配置均保存在本地浏览器中。

- **网页内容粘贴后自动转换**。从网页复制的带格式内容粘贴进编辑器后，标题、加粗、链接、列表、表格会转换为对应的 Markdown 语法，而非退化为纯文本。

- **修正中文加粗的渲染问题**。`**加粗**` 紧邻中文字符时，CommonMark 判定强调符号的规则时常失效，导致 `**` 按原样显示而非渲染为粗体。墨方在解析前进行一次预处理以规避该问题。

- **Runs as a single file**. The whole application is bundled into one HTML
  file, with no server, no account and no installation step. Documents and
  settings are stored in the local browser.

- **Pasted web content is converted automatically**. Formatted content copied
  from a web page is converted on paste: headings, bold, links, lists and
  tables become the corresponding Markdown syntax rather than degrading to
  plain text.

- **CJK bold rendering is corrected**. When `**bold**` sits flush against
  Chinese characters, CommonMark's emphasis flanking rules frequently fail and
  the literal `**` is rendered instead of bold text. MoFang preprocesses the
  source to avoid this.

其它常规能力：

- Markdown 实时预览
- 数学公式（MathJax）
- Mermaid 流程图
- PlantUML 时序图（通过 `plantuml.com` 的公共服务渲染，需要联网）
- GFM 警告块、Ruby 注音、信息图、代码高亮
- 导出 Markdown / HTML / PDF / 长图
- 图床（GitHub、S3、OSS、七牛云、MinIO、Cloudflare R2 等）与 AI 辅助写作（DeepSeek、OpenAI、通义千问等）需自行填写相应服务商的密钥，密钥仅保存在本地浏览器中。
- 支持简体中文、繁體中文、English、日本語

Other standard capabilities:

- Live Markdown preview
- Math formulas (MathJax)
- Mermaid diagrams
- PlantUML diagrams (rendered through the public `plantuml.com` service, which
  requires a network connection)
- GFM alert blocks, Ruby annotations, infographics, syntax highlighting
- Export to Markdown / HTML / PDF / long image
- Image hosts (GitHub, S3, OSS, Qiniu, MinIO, Cloudflare R2, etc.) and
  AI-assisted writing (DeepSeek, OpenAI, Qwen, etc.) require credentials from
  the respective providers; credentials are stored only in the local browser.
- Available in 简体中文, 繁體中文, English and 日本語

## 在线体验 / Try it online

无需下载，直接在浏览器中打开：**[zhangqihenry.github.io/mofang](https://zhangqihenry.github.io/mofang/)**
Try it directly in your browser, no download needed:
**[zhangqihenry.github.io/mofang](https://zhangqihenry.github.io/mofang/)**

## 使用 / Usage

下载本仓库中的 [`mofang.html`](./mofang.html)，用浏览器打开即可，无需安装。
Download [`mofang.html`](./mofang.html) from this repository and open it in a
browser. No installation required.

## 注意事项 / Notes

- 未配置图床时，插入的图片以 base64 编码直接嵌入文档。该方式会显著增加文档体积。配置任一图床后即改为上传并引用链接。
- With no image host configured, inserted images are embedded directly in the
  document as base64 data URLs, which increases file size substantially.
  Configuring any image host switches to uploading and linking instead.

## 致谢 / Credits

墨方的主要灵感来自 [doocs/md](https://github.com/doocs/md)（WTFPL）。

网页内容粘贴后自动转换为 Markdown 的思路来自 [arya](https://github.com/nicejade/markdown-online-editor)（MIT）。

MoFang's main inspiration is [doocs/md](https://github.com/doocs/md) (WTFPL).

The idea of converting pasted web content into Markdown comes from
[arya](https://github.com/nicejade/markdown-online-editor) (MIT).

## License

[MIT](./LICENSE)
