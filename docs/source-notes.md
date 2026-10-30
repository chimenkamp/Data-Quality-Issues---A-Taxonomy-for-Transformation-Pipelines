# Source notes

The English workbooks preserve the source record, including development notes and unresolved interpretations. Cell coordinates are unchanged. A researcher summary is distinct from its adjacent source quotation.

## Interpretation of inherited material

| Location | Source issue | How to read it |
| --- | --- | --- |
| `definitions.xlsx`, `Category definitions`, C75 and D75 | The researcher definition describes multiple representations of one system state; the quoted passage describes different real states mapped to one information-system state. | The translation retains both statements. Do not treat C75 as an equivalent paraphrase of D75. |
| `effects.xlsx`, `Effects`, E258 | The source summary describes noise as reducing “bias/reliability.” | This wording is retained. Read the excerpt in D258 before interpreting direction or mechanism. |
| `effects.xlsx`, `Effects`, rows 288–294 | Notes about missing-data visualization include adverse interpretations of imputation and presentation. | Check the quotations in D against the summaries in E. The summaries are recorded interpretations, not independently verified effect estimates. |
| `taxonomy-development.xlsx`, `Iteration 6` | One occurrence of `Interpretability` has trailing whitespace inherited from the source. | Trim surrounding whitespace for distinct-label counts. Do not count it as a separate category. |
| `search-terms.xlsx`, `Search queries`, versus `screening-wos.xlsx`, `Search and counts` | Development and executed queries differ for preprocessing and case correlation. | Use the screening workbook to identify the actual search; preserve wildcards and the omitted quality block exactly. |

The paper reports 120 stage-specific taxonomy assignments. Historical framework matrix marks are a different unit. For example, `framework-iteration-5.xlsx` has 241 `x` marks in `DQI matrix`, 148 in `DQD matrix`, and 52 in `DQD-to-stage matrix`. These must not be reported as taxonomy category counts or independently established causal relationships.

The seven framework requirement scores in `evaluation.xlsx` are 1, 1, 1, 1, 0.5, 0.5, and 1. They belong to the earlier framework assessment. The current paper's taxonomy ending assessment is described in the manuscript; this workbook is not a substitute for it.

## Preserved evidence and translation conventions

- German labels, definitions, screening reasons, notes, and worksheet names are translated; existing English source quotations and database search syntax are unchanged.
- Publication titles, author names, DOIs, database identifiers, and official series names remain as recorded. The series title `Technologien fur die intelligente Automation` means “Technologies for Intelligent Automation”; its original metadata spelling is retained.
- DQI means data quality issue; DQD means data quality dimension. The German DQP abbreviation is translated as DQI in descriptive text. Stage codes remain those used in the source worksheets.
- The source uses some positive property labels for deficiencies. The translation preserves distinctions such as erroneous, incorrect, and inaccurate data rather than merging them.
- No missing data, quotations, identifiers, publications, or effect links were supplied during translation. Existing blanks, markers, scores, and formulas are retained.
- The source figures were raster images. Their English counterparts are newly drawn SVGs and PNG previews. Layout, font, and line wrapping may differ; labels, numerical counts, and connections are preserved. The pipeline retains the source representation label “process instances.” The design-science figure retains the thesis scope.

## Transfer checks

The English workbooks were compared with all source cells and worksheet structures. The comparison covered translated text, unchanged numerical values and formulas, sheet order, merged cells, frozen panes, filters, number formats, validation rules, and conditional formatting. Original workbook package parts were preserved except for shared text and worksheet-name metadata; unchanged rich-text quotations retain their original XML.

The six raw `.xls` exports have matching source and destination SHA-256 hashes. The final taxonomy was recounted by stage and distinct trimmed label; corpus and extraction counts were recalculated from the workbooks. All nine SVGs were rendered to PNG and inspected against the source figures. These checks establish transfer consistency. They do not independently validate the original coding or demonstrate native Excel rendering on every platform.
