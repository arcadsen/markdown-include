### 元数据块 Metadata Blocks

#### 扩展：`pandoc_title_block`

```markdown
% title
% author(s) (separated by semicolons)
% date
```

将被解析为书目信息，而不是常规文本。（例如，它将用于独立的 LaTeX 或 HTML 输出的标题。）该块可以只包含标题、日期和作者，或者包含所有三个元素。

#### 扩展：`yaml_metadata_block`

顶部的三个连字符---和底部的三个连字符---或三个点...的行分隔。 YAML 元数据块可能出现在文档中的任何位置，但如果它不在文档开头，则必须以前方存在空白行

元数据可以包含列表和 YAML 对象，Pandoc 将忽略名称以下划线结尾的字段，如果两个元数据块尝试设置相同的字段，则将采用第一个块中的值。

必须遵循 YAML 转义规则,标题包含冒号，则必须引用它。垂直符|在缩进行的行首，该行将按字面解释，无需转义。当文本中包含空行或块级样式时，必须遵守以上规则