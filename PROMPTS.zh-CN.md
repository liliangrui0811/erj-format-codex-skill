# 中文使用提示词

下面是一些适合直接复制到 Codex 中使用的提示词。

## 一键格式化

```text
使用 $economic-research-format，把这个 DOCX 论文整理成《经济研究》投稿格式。请保留原文内容，输出一个新的修改版 DOCX，并附一份格式审查报告。
```

## 匿名审稿检查

```text
使用 $economic-research-format，检查这个 DOCX 是否适合匿名投稿《经济研究》。重点检查作者姓名、单位、邮箱、手机号、基金项目、致谢、Word 元数据和正文中的自我引用风险。
```

## 只做格式审查

```text
使用 $economic-research-format，只审查这个 DOCX 是否符合《经济研究》格式，不要修改正文。请列出标题、摘要、关键词、图表、公式、脚注、参考文献和英文 Summary/JEL 的问题清单。
```

## 根据样张格式修改

```text
使用 $economic-research-format，优先按照 references/user-provided-format-spec.md 中的样张规则修改这篇论文，包括标题、作者、摘要、关键词、一级标题、二级标题、表格、图题、脚注和参考文献格式。
```

## 参考文献专项检查

```text
使用 $economic-research-format，专项检查这篇论文的参考文献格式。请关注：是否不标序号、每条前是否空 2 格、中文文献是否在前、英文作者写法、英文题名大小写、期刊名斜体、页码范围和正文引用是否匹配。
```

## 图表专项检查

```text
使用 $economic-research-format，专项检查这篇论文的表格和图形格式。请关注：表题和图题编号是否连续，表格是否适合三线表，表下注释是否完整，图是否为黑白图，图题是否黑体小五并居中。
```

## 输出 GitHub Skill 包前检查

```text
请检查这个 economic-research-format skill 包是否可以上传 GitHub：运行官方 quick_validate，检查 README、中文 README、提示词文件、references 和 scripts 是否完整，并确认压缩包里没有 __pycache__ 等缓存文件。
```
