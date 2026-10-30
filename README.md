# A Taxonomy of Data Quality Issues for Process Mining on Unstructured Data

Companion materials for the paper: literature search and screening records, extracted evidence, definitions, and six taxonomy iterations. The final taxonomy contains **120 stage-specific assignments and 46 distinct category labels** across five pipeline stages and nine data quality dimensions.

Download the repository or individual workbooks and open the `.xlsx` and `.xls` files in a spreadsheet application. No installation or code execution is required. Clear existing filters to inspect all records; expand cells or use the formula bar to read long text. Worksheet names below refer to the English workbooks.

## Reviewer guide

| Review task | File | Location |
| --- | --- | --- |
| Inspect the final taxonomy | [taxonomy-development.xlsx](tables/taxonomy-development.xlsx) | `Iteration 6`, `A1:J35`; column A contains stage codes, columns B–J contain dimensions |
| Check category definitions and supporting quotations | [definitions.xlsx](tables/definitions.xlsx) | `Category definitions`: category B, researcher definition C, source quotation D, page E, DOI F; `DQD definitions` contains dimension definitions |
| Trace a category to extracted evidence | [full-text-analysis.xlsx](tables/full-text-analysis.xlsx) | `Extraction`, rows 2–928; filter category M and stage G–K, then inspect excerpt E, page D, and DOI C |
| Inspect the 154-publication corpus | [full-text-analysis.xlsx](tables/full-text-analysis.xlsx) | `Publications`, rows 2–155; title C, year D, DOI E |
| Inspect the queries actually used and selection counts | [screening-wos.xlsx](tables/screening-wos.xlsx) | `Search and counts`: queries `B2:B7`, retrieval counts `C2:C7`, overall selection counts `C95:C113` |
| Inspect individual screening decisions | [screening-wos.xlsx](tables/screening-wos.xlsx) | `All stages`, rows 2–1043; title M, DOI AH, decisions CB–CH; the six stage sheets retain their own decisions and summaries |
| Inspect citation searching | [snowballing.xlsx](tables/snowballing.xlsx) | `Seed publications`; `Combined candidates`, rows 2–122; source A, search direction B, title D, decisions H–M |
| Inspect category development | [taxonomy-development.xlsx](tables/taxonomy-development.xlsx) | `Iteration 1` through `Iteration 6` and the intervening `Changes …` sheets |
| Inspect search-vocabulary development | [search-terms.xlsx](tables/search-terms.xlsx) | `Terms`, `DQ search terms`, `IoT search terms`, stage sheets, and `Search queries` |

The search-development workbook differs from the executed search: its case-correlation query contains a data-quality block, and its preprocessing query uses `pre*process*`. The executed queries in `screening-wos.xlsx` omit that block for case correlation and use `pre$process*` for preprocessing. Query syntax is preserved exactly.

Extraction codes are more detailed than the final categories. Use the taxonomy iteration notes to follow merges and renamings when tracing a final category back to its evidence.

## Counts and interpretation

The February 2026 Web of Science search returned 1,042 stage-specific records. Screening retained 168 records representing 134 distinct titles. Citation searching considered 121 candidates and added 20 publications. The resulting corpus has 154 distinct titles and 927 extracted passages. The [selection flow](figures/prisma-flow.svg) preserves the counts and exclusions recorded in the source.

The sensitivity seed manuscript is a recorded exception to the peer-review criterion. Snowballing was not repeated to saturation; the corpus is bounded by the documented search and screening procedure.

| Stage | Workbook code | First affected representation | Distinct publications with positive-relevance evidence | Taxonomy assignments |
| --- | --- | --- | ---: | ---: |
| Preprocessing | PP | Raw observations | 113 | 36 |
| Abstraction | A/A; A&A in search development | Preprocessed observations | 2 | 11 |
| Case correlation | CC | Abstracted events | 18 | 15 |
| Process mining | PM | Event logs | 50 | 31 |
| Visualization | Vs; V in effects sheets | Process models and analytical results | 12 | 27 |

Acquisition is searched separately (`DC`) but is not a sixth taxonomy stage. Issues originating during acquisition are assigned to preprocessing. The inherited label “abstraction / aggregation” corresponds to the paper's abstraction stage. Visualization includes presentation, interpretation, conclusions, decisions, and predictions.

To reproduce the reported counts:

1. **Corpus:** count the 154 numbered records in `Publications`. Count each title once. Cross-stage retrieval records are not additional publications.
2. **Stage coverage:** in `Extraction`, interpret F numerically and retain values greater than zero. For each stage column G–K, select `v` and count distinct titles in B. A title can contribute to multiple stages. Three corpus titles have no positive-relevance stage assignment.
3. **Taxonomy:** in `Iteration 6`, count each populated category cell in B–J, excluding `x`. Sum by the stage in A to obtain 120 assignments. Trim surrounding whitespace before counting distinct labels to obtain 46. Repeated labels retain their separate stage assignments.
4. **Final-iteration stability:** compare `Iteration 5` and `Iteration 6`; their category assignments are unchanged.

The nine dimensions are currentness, accuracy, credibility, consistency, usefulness, precision, semantics, understandability, and completeness. Positive property labels, such as reliability, denote insufficient quality in that property. Erroneous, incorrect, and inaccurate data remain distinct categories.

In extraction, `v` marks a stage assignment; relevance values are 0, 0.5, and 1 (114, 607, and 206 passages respectively). These are recorded coding values, not probabilities. In the final taxonomy, `x` denotes an unassigned stage–dimension combination. In historical framework matrices, `x` instead marks a recorded relationship. Empty cells and `x` in citation fields retain their source meaning; no missing DOI has been inferred.

## Original database exports

These six `.xls` files retain the original bytes, including bibliographic metadata and English database field names.

| Search | Export | Records excluding header |
| --- | --- | ---: |
| Data acquisition | [wos-data-acquisition.xls](tables/wos-exports/wos-data-acquisition.xls) | 542 |
| Preprocessing | [wos-preprocessing.xls](tables/wos-exports/wos-preprocessing.xls) | 217 |
| Abstraction / aggregation | [wos-abstraction.xls](tables/wos-exports/wos-abstraction.xls) | 30 |
| Case correlation | [wos-case-correlation.xls](tables/wos-exports/wos-case-correlation.xls) | 91 |
| Process mining | [wos-process-mining.xls](tables/wos-exports/wos-process-mining.xls) | 56 |
| Visualization | [wos-visualization.xls](tables/wos-exports/wos-visualization.xls) | 106 |

## Figures

SVG files are editable vector figures; PNG files are previews. All nine source figures have English replacements with the same labels, counts, and connections.

| Figure | SVG | PNG |
| --- | --- | --- |
| Literature selection | [SVG](figures/prisma-flow.svg) | [PNG](figures/prisma-flow.png) |
| Transformation pipeline | [SVG](figures/transformation-pipeline.svg) | [PNG](figures/transformation-pipeline.png) |
| Taxonomy overview | [SVG](figures/taxonomy-overview.svg) | [PNG](figures/taxonomy-overview.png) |
| Preprocessing taxonomy | [SVG](figures/taxonomy-preprocessing.svg) | [PNG](figures/taxonomy-preprocessing.png) |
| Abstraction taxonomy | [SVG](figures/taxonomy-abstraction.svg) | [PNG](figures/taxonomy-abstraction.png) |
| Case-correlation taxonomy | [SVG](figures/taxonomy-case-correlation.svg) | [PNG](figures/taxonomy-case-correlation.png) |
| Process-mining taxonomy | [SVG](figures/taxonomy-process-mining.svg) | [PNG](figures/taxonomy-process-mining.png) |
| Visualization taxonomy | [SVG](figures/taxonomy-visualization.svg) | [PNG](figures/taxonomy-visualization.png) |
| Historical design-science process | [SVG](figures/design-science-research.svg) | [PNG](figures/design-science-research.png) |

## Historical framework materials

The source repository accompanied a master's thesis with a broader framework scope. The following files are retained in English to preserve that record. Their effect links and requirement scores are not causal validation or an independent evaluation of the taxonomy in the current paper.

| Material | Files | Contents |
| --- | --- | --- |
| Extracted effects | [effects.xlsx](tables/effects.xlsx) | `Effects`: source quotation D, researcher summary E, source-stage coding F–L, affected-stage coding M–S, other effects T, notes U |
| Framework development | [Iteration 2](tables/framework-iteration-2.xlsx), [3](tables/framework-iteration-3.xlsx), [4](tables/framework-iteration-4.xlsx), [5](tables/framework-iteration-5.xlsx) | `DQI matrix`; iterations 3–5 also contain `DQD matrix` and `DQD-to-stage matrix` |
| Framework revision notes | [framework-changes-for-iteration-5.xlsx](tables/framework-changes-for-iteration-5.xlsx) | `DQD changes`, `DQI changes`, `Stage changes` |
| Framework requirement assessment | [evaluation.xlsx](tables/evaluation.xlsx) | `Evaluation`, seven requirements in rows 2–8; scores in D |

## Provenance and limitations

Translated from [dqp-prozessanalyse, commit 7744664d12c87e55b65ba10d0d1fb1cda9654870](https://github.com/KaD816/dqp-prozessanalyse/tree/7744664d12c87e55b65ba10d0d1fb1cda9654870). The transfer includes all 13 workbooks (53 worksheets), six database exports, and nine figures. The original README is replaced by this guide.

German researcher-authored text and worksheet names are translated. Existing English quotations, publication titles, author names, identifiers, numerical values, formulas, and search expressions are preserved. Official bibliographic names remain as recorded. The workbooks retain cell coordinates and native formatting. The [provenance manifest](docs/provenance.json) maps every source file to its English counterpart and records SHA-256 hashes.

The materials document the original single-researcher coding. Translation does not constitute independent recoding, a new literature search, a formal study-quality appraisal, or empirical validation of effects. Full publication PDFs are not included. Read the [source notes](docs/source-notes.md) before interpreting inherited definitions and effect summaries.
