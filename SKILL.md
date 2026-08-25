---
name: economic-research-format
description: Format Chinese economics manuscripts for submission to 《经济研究》 / Economic Research Journal, especially DOCX papers requiring journal-style typography, anonymous-review cleanup, Chinese/English front matter, citations, references, footnotes, figures, tables, and regression-table checks. Use when asked to make a manuscript match 《经济研究》 format or audit whether it is submission-ready; do not use for estimating models or rewriting the paper's substantive contribution unless separately requested.
---

# 《经济研究》投稿格式 Skill

Use this skill when the user asks to format, audit, or prepare a Chinese economics manuscript for 《经济研究》 submission.

## Source Priority

Prefer sources in this order:

1. A user-provided current 《经济研究》 template, editorial instruction, downloaded submission guide, or already accepted manuscript sample.
2. The bundled sample-derived guide in [references/user-provided-format-spec.md](references/user-provided-format-spec.md), organized from the user's 《经济研究》 format screenshots where red text marks formatting requirements.
3. The official journal site or online submission system when accessible.
4. The conservative rules in [references/erj-format-rules.md](references/erj-format-rules.md), which consolidate publicly indexed materials and common Economic Research Journal practice.
5. Third-party templates only as aids, never as proof of current requirements.

If no current official Word template or author guide is available, say so in the final response and mark uncertain items in the format report.

For conflicts between the bundled screenshot-derived Word rules and the GitHub LaTeX template, read [references/latex-template-comparison.md](references/latex-template-comparison.md). In short: use the LaTeX template only as supplementary evidence for structure and bibliography conventions; do not import its page headers, logo, or working-paper layout into Word submissions.

## Workflow

Preserve the user's source manuscript. Write a new DOCX, and keep the original unchanged.

Before changing layout, inspect the manuscript for:

- title, author block, affiliation, fund note, acknowledgements, contact details;
- Chinese title, content abstract, keywords, main text, references;
- English title, Summary, Key Words, JEL Classification, and any Chinese counterpart to the Summary;
- heading hierarchy, equations, footnotes, tables, figures, appendices, and regression tables;
- literature citations in the text and matching reference-list entries;
- identity leaks that violate anonymous review.

For ordinary DOCX formatting, use the deterministic helper as a starting point:

```bash
python scripts/apply_erj_docx_format.py input.docx --out output.docx
```

Use `--cjk-font`, `--western-font`, and `--table-font` when the user's environment or template requires a specific font. The conservative defaults are Chinese Songti and Western Times New Roman.

The helper now encodes the screenshot-derived roles where they can be applied safely: title as Songti 三号/小三 equivalent, author line as Songti 小四, Chinese abstract and keywords as 仿宋五号, first-level headings as Songti 四号 centered, table body as 仿宋 smaller than body, figure captions as 黑体小五, references as Songti 六号, and metadata scrubbing for anonymous review.

Then inspect and adjust manually for paper-specific problems such as wide regression tables, multi-page tables, formulas, figure placement, or special front matter.

After formatting, run:

```bash
python scripts/audit_erj_docx.py output.docx --json
```

Use the audit output as a warning list, not as a final verdict. Read identity-risk contexts manually because phrases such as "anonymous review version" can intentionally mention author, fund, or acknowledgement fields without leaking the author's real identity.

## Formatting Duties

Apply the concrete screenshot-derived rules in [references/user-provided-format-spec.md](references/user-provided-format-spec.md) first, then use [references/erj-format-rules.md](references/erj-format-rules.md) for supplementary conservative checks. Keep changes conservative when a rule's current status cannot be verified from an official source.

For regression tables:

- keep rows as variables/statistics such as coefficient, standard error, controls, fixed effects, sample size, and R-squared;
- keep columns as model specifications, dependent variables, sample groups, or robustness variants;
- use a clean three-line table unless the user explicitly asks to preserve grid borders;
- keep titles, units, notes, and significance-star definitions adjacent to the table.

For citations and references:

- do not turn literature citations into footnotes;
- use author-year parenthetical citations in the text;
- ensure every in-text citation appears in the references and every reference is cited;
- keep Chinese references before foreign references when both exist, and sort each group by the first author's surname.

## Deliverables

When possible, return:

- the formatted DOCX;
- a brief format report listing completed changes, uncertain rules, and items requiring author confirmation;
- a warning list for missing author information, missing Summary/JEL, inconsistent citations, table/figure quality, identity leaks, or references that cannot be safely normalized.

If the Documents skill render workflow is available, render the final DOCX and visually inspect representative pages before delivery. If rendering is unavailable, state that visual layout verification was not completed.

If rendering succeeds but Chinese characters appear as boxes or disappear, treat that as a renderer font-support limitation unless DOCX text extraction also shows missing text. In that case, disclose the limitation and ask the user to visually confirm the DOCX in Microsoft Word or WPS.
