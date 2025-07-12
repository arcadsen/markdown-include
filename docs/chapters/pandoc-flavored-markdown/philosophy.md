### 设计哲学 Philosophy

[John Gruber] 将 Markdown 设计为易于编写，并且更重要的是易于阅读：

> Markdown 格式的文档应该可以直接发布为纯文本，而不应看起来像是被标签或格式化指令标记过。

在 HTML 中，元素主要分为两类：块级元素（Block Elements）和内联元素（Span Elements，也称为行内元素）。这两类元素在页面布局和行为上有显著区别。

Markdown 基本语法包括：

- 块级元素（Block elements）： paragraphs、 line breaks、 headers、 blockquotes、 lists、 code blocks、 horizontal rules；
- 内联元素（Span elements）： links、 emphasis、 code、 images；
- 其它元素（Miscellaneous）：backslash escape、 automatic links。

Pandoc 中支持扩展修订版本的 Markdown 语法。Markdown 的设计哲学指导了 Pandoc 在寻找表格、脚注和其他扩展的语法时所做的决定。然而，Pandoc 的目标与 Markdown 最初的目标不同。虽然 Markdown 最初是为生成 HTML 而设计的，但 Pandoc 是为多种输出格式而设计的。因此，虽然 Pandoc 允许嵌入原始 HTML，但它并不鼓励这样做，并提供了其他非 HTML 方式来表示定义列表、表格、数学和脚注等重要文档元素。

- 使用 Pandoc 中支持的 Markdown 语法用 `-f markdown`
- 使用标准 Markdown 语法用 `-f markdown_strict`
  
Pandoc 所支持的语法各种对标准 Markdown 语法的扩展可以通过在格式后以 `+EXTENSION` 添加或`-EXTENSION` 去除，如：

- `-f markdown-footnotes` 表示识别除了 `footnotes` 扩展之外的所有 pandoc Markdown 语法
- `-f markdown_strict+footnotes+pipe_tables` 表示识别标准 Markdown 语法加上 `footnotes` 和 `pipe_tables` 扩展语法。
