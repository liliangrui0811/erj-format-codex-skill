# economic-research-format

[中文说明](README.zh-CN.md)

Codex skill for preparing Chinese economics manuscripts for 《经济研究》 / Economic Research Journal submission.

It helps format and audit DOCX manuscripts: front matter, heading hierarchy, anonymous-review cleanup, citations, references, footnotes, figures, tables, and regression-table layout.

## Important Source Note

A current official downloadable Word template was not reliably found during the initial public search. This skill therefore includes a sample-derived guide from user-provided 《经济研究》 format screenshots plus a conservative rule set from publicly indexed submission guidance, historical formatting references, and common Economic Research Journal practice. If you have a current official guide or template from the journal submission system, provide it and treat it as controlling.

## Install

Copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R economic-research-format ~/.codex/skills/economic-research-format
```

Then restart or refresh Codex if needed.

## Use

```text
Use $economic-research-format to format this DOCX for 《经济研究》 submission.
```

For local helper scripts:

```bash
python scripts/apply_erj_docx_format.py input.docx --out output.docx
python scripts/audit_erj_docx.py output.docx
```

If your Word environment needs a specific Chinese font:

```bash
python scripts/apply_erj_docx_format.py input.docx --out output.docx --cjk-font 宋体 --abstract-font 仿宋 --table-font 仿宋 --figure-font 黑体
```

The audit script reports missing front matter, possible anonymous-review identity risks, and non-empty Word metadata. Review the reported contexts manually because some warnings may be intentional anonymous-version notices rather than real identity leaks.

## Contents

- `SKILL.md`: skill entrypoint.
- `README.zh-CN.md`: Chinese README for GitHub users.
- `PROMPTS.zh-CN.md`: Chinese prompt examples for common workflows.
- `references/user-provided-format-spec.md`: screenshot-derived 《经济研究》 format specification.
- `references/latex-template-comparison.md`: comparison with the GitHub `Chinese-ERJ` LaTeX template.
- `references/erj-format-rules.md`: conservative formatting and submission checks.
- `references/source-notes.md`: source caveats and public leads.
- `scripts/apply_erj_docx_format.py`: conservative DOCX formatting pass.
- `scripts/audit_erj_docx.py`: lightweight format audit.
