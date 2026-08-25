# 《经济研究》格式化 Codex Skill

本skill用于将 Word / DOCX 论文整理为《经济研究》投稿格式，并生成格式审查提示。

## 重要说明

因《经济研究》官网没有直接给出官方 Word 模板。因此，本 skill 采用以下材料作为格式依据：

-《经济研究》官网提供的格式样张，已整理为 `references/user-provided-format-spec.md`。
- 公开可检索的历史投稿说明和保守格式规则，整理在 `references/erj-format-rules.md`。
- GitHub 上的 `Chinese-ERJ` LaTeX 模板，对照说明见 `references/latex-template-comparison.md`。

如果你有从《经济研究》投稿系统下载的最新版官方模板或格式说明，应以官方文件为最高优先级。

## 功能

- 将 DOCX 论文按《经济研究》样张规则做保守格式化。
- 检查中文摘要、关键词、English Summary、Key Words、JEL Classification。
- 检查表题、图题、公式编号和参考文献标题。
- 检查匿名审稿风险，包括邮箱、手机号、基金项目、致谢和 Word 元数据。
- 清空输出文件中的核心 Word 元数据，降低匿名投稿风险。
- 对表格做保守三线表处理，并保持回归表方向不乱转置。

## 安装

将整个文件夹复制到 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R economic-research-format ~/.codex/skills/economic-research-format
```

然后重启或刷新 Codex。

## 使用方式

在 Codex 中可以这样说：

```text
使用 $economic-research-format，把这个 DOCX 论文整理成《经济研究》投稿格式，并输出修改版和格式审查报告。
```

也可以直接运行脚本：

```bash
python scripts/apply_erj_docx_format.py input.docx --out output.docx
python scripts/audit_erj_docx.py output.docx --json
```

如果需要指定中文字体：

```bash
python scripts/apply_erj_docx_format.py input.docx --out output.docx --cjk-font 宋体 --abstract-font 仿宋 --table-font 仿宋 --figure-font 黑体
```

## 样张规则摘要

- 标题：宋体三号或小三，居中。
- 作者姓名：宋体小四，居中。
- 内容摘要：`内容摘要：`，仿宋五号。
- 关键词：`关键词：`，紧接摘要。
- 一级标题：`一、标题`，宋体四号，居中。
- 二级标题：`（一）标题`，前空 2 格。
- 公式：Word 自带公式或 MathType，编号右置，`其中` 前空两格。
- 脚注：每页重新编号，内容前空 2 格，宋体六号。
- 表格：建议仿宋，字号小于正文；表下注释比表格正文小 1 号。
- 图题：黑体小五，居中，尽量使用黑白图。
- 参考文献：宋体六号，不标序号，每条前空 2 格，英文和数字使用 Times New Roman。

## 文件结构

- `SKILL.md`：skill 入口说明。
- `README.md`：英文 README。
- `README.zh-CN.md`：中文 README。
- `PROMPTS.zh-CN.md`：中文提示词示例。
- `references/user-provided-format-spec.md`：根据用户样张整理的格式说明。
- `references/latex-template-comparison.md`：与 GitHub `Chinese-ERJ` LaTeX 模板的对照。
- `references/erj-format-rules.md`：保守格式规则和投稿检查。
- `references/source-notes.md`：来源说明。
- `scripts/apply_erj_docx_format.py`：DOCX 格式化脚本。
- `scripts/audit_erj_docx.py`：格式审查脚本。

## 注意事项

这个 skill 不会自动判断论文质量，也不会替代作者对参考文献、图表清晰度和投稿系统要求的最终核对。对于参考文献作者缩写、英文题名大小写、期刊斜体和页码范围，脚本只能提示检查，不能保证逐条完全正确。

如果 LibreOffice 渲染出的页面图片中中文显示为方框，通常是渲染环境缺少中文字体，不一定表示 DOCX 内容丢失。最终投稿前建议使用 Microsoft Word 或 WPS 打开检查首页、表格页、图页和参考文献页。
