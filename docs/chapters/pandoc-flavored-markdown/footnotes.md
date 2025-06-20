### 脚注

#### 扩展：`footnotes`

Pandoc 的 Markdown 允许使用脚注，使用以下语法：

```markdown
![[ ../../examples/pandoc-flavored-markdown/footnotes.md ]]
```

脚注引用中的标识符不得包含空格、制表符、换行符或字符 `^`、`[`、 或 `]`。这些标识符仅用于将脚注引用与注释本身关联起来；在输出中，脚注将按顺序编号。

脚注本身不必放在文档末尾。它们可以出现在除其他块元素（列表、块引用、表格等）之外的任何位置。每个脚注都应与周围内容（包括其他脚注）用空行分隔。

#### 扩展：`inline_notes`

行内脚注也是允许的（不过，与常规注释不同，行内脚注不能包含多个段落）。语法如下：

```markdown
![[ ../../examples/pandoc-flavored-markdown/footnotes-inline.md ]]
```

行内脚注和常规脚注可以自由混合。