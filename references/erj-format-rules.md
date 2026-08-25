# 《经济研究》格式规则

These rules are intended for conservative submission preparation. They combine publicly indexed 《经济研究》 submission guidance, historical electronic-manuscript requirements, and common economics-journal Word conventions. When a user provides a current official guide or template, that source overrides this file.

## Current-Source Caveat

As of the source check for this skill, a directly downloadable latest official Word format document was not reliably discoverable through public search. Publicly indexed materials point to the journal site and online submission system, but detailed Word typography rules are mostly visible through archived or third-party copies. Treat exact font size, margins, and line-count constraints as rules to confirm against the latest official submission system when the manuscript is actually submitted.

Useful public leads:

- Official site frequently referenced by public notices: `http://www.erj.cn/`
- Online submission system frequently referenced by public notices: `https://erj.ajcass.com/Admin/`
- Historical reference page often cited in forum archives: `http://www.erj.cn/cn/Info.aspx?m=20100913105301153616`
- LaTeX reference template: `https://github.com/EthanDeng/Chinese-ERJ`
- CSL reference style: `https://github.com/daidaishengweinan/Chinese-STD-GB-T-7714-related-csl`

## Manuscript Contents

Expected Chinese part:

- Chinese title.
- Author names and affiliations when preparing a non-anonymous full file; for anonymous review, remove or separate identifying information as required by the system.
- Content abstract, usually about 300 Chinese characters in public historical guidance.
- Keywords, usually 3-5.
- Main text.
- References.
- Chinese counterpart to the English Summary when requested by the journal or editor.

Expected English part:

- English title.
- Author names and affiliations when not anonymous.
- Summary, historically described as about 4500 English characters including digits and spaces.
- Key Words.
- JEL Classification.

## Page And Typography

Use A4 paper.

Conservative body setting:

- Chinese font: Songti.
- Western letters and numbers: Times New Roman.
- Body size: 五号 if following older electronic-manuscript guidance; 小四 or 12 pt only when matching a user-provided template.
- Line spacing: single line in older electronic-manuscript guidance; do not use double spacing unless the user-provided reference requires it.
- Page margins: keep all margins at least 2.54 cm in the conservative setting.
- Do not use multi-column layout.

If the user supplies a reference manuscript image or DOCX showing different typography, match that reference and document the source in the format report.

Rendering caveat: some LibreOffice-based renderers do not reliably display Chinese fonts even when the DOCX text is intact. If rendered PNGs show boxes or missing Chinese characters, verify by extracting DOCX text and by opening the file in Microsoft Word or WPS before treating it as a content-loss defect.

## Title, Abstract, Keywords

Title:

- Center align.
- Keep concise and academically descriptive.
- Use a larger Songti/Heiti title style only when the reference template supports it.

Abstract:

- Start with `内容提要：` or the exact label in the provided template.
- State the research question, method/data, main findings, policy implications, and contribution.
- Avoid vague claims that do not reveal the paper's result.

Keywords:

- Use `关键词：`.
- Keep 3-5 terms unless a current guide says otherwise.

English front matter:

- Use `Summary`, `Key Words`, and `JEL Classification` labels unless the user's template uses a different spelling.
- Do not mechanically translate the Chinese abstract into the Summary; the Summary is longer and should explain China-specific institutional context when relevant.

## Heading Hierarchy

Use Chinese journal numbering:

- 一级标题: `一、标题`
- 二级标题: `（一）标题`
- 三级标题: `1. 标题`
- 四级或 paragraph-level sequence: `（1）`

Older and third-party guidance commonly centers first-level headings and left-aligns lower-level headings. If exact alignment is uncertain, preserve a clean hierarchy and flag the item for final confirmation.

## Citations

For ordinary literature citation, use in-text author-year parenthetical citation rather than footnotes or endnotes.

Examples:

- `（张三，1987；李四，1990）`
- `张三（1990）已经有所论证`
- `（李四，1989，第34页）`
- `(David, 1985, p.55)` for foreign-language sources if the manuscript uses English punctuation in foreign citations.

Rules:

- Include year, not month, in normal in-text citations.
- Add page number when quoting or pointing to a specific page.
- Separate multiple citations with semicolons.
- For one author with multiple works in the same year, use suffixes such as `1991a` and `1991b`.
- Author self-citation still needs normal author-year citation.

## Footnotes

Use footnotes for substantive notes, author notes, project information, data notes, or clarifications, not for ordinary literature references.

Conservative setting:

- Footnotes restart each page when possible.
- Footnote text uses small Songti, commonly 六号 in templates.
- Author/project notes under the title may use a `*` marker when preparing the non-anonymous title page.

## Tables

Use publication-quality tables.

- Prefer three-line tables for regression and descriptive-statistics tables.
- Table titles should be numbered as `表 1`, `表 2`, and centered with clear titles.
- If a table has units, place the unit near the title or table top right according to the manuscript's convention.
- Use smaller font than body text for table content.
- Put notes directly below tables, including sample definitions and significance-star definitions.
- Keep short tables on one page; repeat header rows for long tables.
- Do not transpose regression tables so that variables become columns unless the user specifically asks for that layout.

## Figures

Use publication-quality figures.

- Prefer black-and-white or grayscale graphics.
- Avoid scanned, photographed, blurry, or color-dependent figures.
- Number captions as `图 1`, `图 2`, and keep captions adjacent to figures.
- Ensure labels, legends, and axis titles are readable when printed.

## Equations

Use Word's built-in equation editor or MathType-compatible equations when possible.

- Number important equations on the right as `(1)`, `(2)`, etc.
- Define variables directly below the equation.
- Keep formula symbols consistent with the text and regression tables.

## References

Reference-list heading: `参考文献`.

General order:

- Chinese references, including translated works, first.
- Foreign-language references second.
- Sort each group by the first author's surname.
- Do not number references unless a current template explicitly requires numbering.

Chinese examples:

- `张三，1989：《论市场》，《经济研究》第8期。`
- `李四，1991a：《论计划》，经济出版社。`
- `李四，1991b：《论计划与市场》，载于王五编《计划与市场》，经济出版社，第59—69页。`

Foreign-language examples:

- `John, D., 1956, “On Demand,” American Economic Review, Vol. 9, pp. 15—25.`
- `Krugman, P., 2006, “Title of the Article,” NBER Working Paper, No. 4567.`

Checks:

- Article titles use quotation marks in English references.
- Journal names are italicized when the output format supports italics.
- Page ranges use a long dash or journal-consistent dash.
- Keep Chinese punctuation in Chinese references and consistent English punctuation in foreign references.

## Anonymous Review Check

Before delivery, search for possible identity leaks:

- author names, initials, affiliations, email addresses, phone numbers, postal addresses;
- grant numbers or acknowledgements that identify the author when an anonymous file is requested;
- first-person references to the author's previous work such as `笔者曾`, `本人`, `课题组`;
- document properties and comments containing author metadata.

If identity information must be kept in a separate title page or submission form, do not place it in the anonymous manuscript body.
