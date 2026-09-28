# Minor Revision Track

Use this track for `--minor` and as the second stage of `--both`. During the minor pass, read this file only; the major pass has its own guide.

**Scope.** Check grammar, spelling, notation, units, numbers, references, citations, word choice, captions, tables, and agreement between figures and text. Focus on individual sentences, symbols, and numbers.

**Outside this track.** Contribution framing, novelty, derivation soundness, claim support, narrative structure, and simulation sufficiency belong to the major pass. If you notice one of these during a minor pass, record it briefly and continue. In `--both`, the major review covers it; in `--minor` alone, put it under **Out-of-scope observations**.

**Required source.** Obtain the LaTeX source before starting. A PDF alone does not provide usable source locations for line-level corrections.

---

## Review in document order

Work through the manuscript from start to finish. At each subsection, or each chunk of about 40 LaTeX lines in a long subsection, apply all 14 checks. Separate whole-paper passes for grammar, notation, and units tend to miss scattered errors.

1. Make a `todo` queue in document order. Include the abstract, body, captions, table contents, algorithms, and appendices.
2. Apply the full checklist at each position.
3. Append findings to `review_minor.md` before moving on, then mark that position done.
4. Record positions with no findings as `swept, none found`.

In `--both`, first check the major review's **dead-zone list**. For a position slated for rewriting, record `skipped: slated for rewrite per major item N` and move on.

---

## Per-Position Checklist

Apply all 14 checks at each position. If a check has no relevant material at that position, move to the next one.

**1. Grammar**

- Check subject–verb agreement, articles, and singular/plural forms. Watch uncountable nouns (information, research, performance, hardware) and plurals such as matrices, indices, and criteria.
- Check tense within each section: present for established facts and what figures show; past for work performed.
- Check misplaced modifiers and parallel lists. In “Using the proposed method, the error decreases,” the opening phrase has no suitable subject.
- Check relative pronouns (`that`/`which`/`where`) and whether a clause is restrictive.

**2. Spelling and orthographic consistency**

- Correct misspellings and keep US or UK spelling consistent throughout (`optimize/optimise`, `behavior/behaviour`, `modeling/modelling`).
- Check hyphens in compound modifiers (`closed-form solution`, `low-complexity algorithm`, `real-time processing`) and their unhyphenated predicative forms.
- Keep capitalization of technical terms and the spelling of author and venue names consistent.

**3. Abbreviations**

- Expand each abbreviation at first use in the abstract and again at first use in the body. Do not expand it repeatedly later.
- Check that introduced abbreviations are reused and agree with the nomenclature table, if present.
- Form plurals without an apostrophe (`SNRs`). Choose articles by pronunciation (`an SNR`, `a MIMO system`).

**4. Equation punctuation and grammatical integration**

- Punctuate a displayed equation as part of its sentence, with a comma or period as needed.
- Check whether the text after the display continues the sentence or starts a new one. Keep `where` clauses consistent; do not capitalize `where` mid-sentence.
- Read the sentence with the equation in place. It should have a verb and remain grammatical.

**5. Symbol typesetting**

- Set scalar variables in italics. Apply the paper's chosen vector and matrix convention (such as bold-italic lowercase vectors and bold-upright uppercase matrices) consistently; do not switch a symbol between italic and upright.
- Keep operators and functions upright (`\log`, `\max`, `\min`, `\exp`, `\arg`, `\mathrm{tr}`, `\mathrm{diag}`, `\mathbb{E}`).
- Set descriptive subscripts upright and index subscripts italic (`P_{\mathrm{tx}}` versus `P_i`).
- Use one style for transpose, Hermitian, and conjugate marks (`^{\mathsf{T}}`, `^{\mathsf{H}}`, `^{*}`). Keep sets and fields in the paper's chosen blackboard-bold or calligraphic style. Use consistent delimiters for norms, absolute values, and inner products; size delimiters with `\left`/`\right` where needed.

**6. Units and numbers**

- Separate values and units with a nonbreaking thin space (`5\,\mathrm{GHz}`), apart from `%` and degrees where the field's style omits it.
- Check capitalization and meaning of units: GHz, dBm, ms; distinguish dB, dBm, dBi, and dBW.
- Keep significant figures, decimal marks, thousands separators, and scientific notation consistent. Avoid false precision.
- Use an en dash for ranges. Give units for physical quantities in tables and axis labels.

**7. Cross-reference mechanics**

- Use the paper's chosen forms consistently: `Fig.`/`Figure`, `Tab.`/`Table`, `Eq.`/`(N)`, `Sec.`/`Section`, and `Alg.`/`Algorithm`.
- Capitalize references to specific numbered objects; spell out sentence-initial forms where the venue requires it. Use `\eqref` and `\ref` consistently for equations.
- Confirm that every referenced object exists, has the stated number, and is in the section implied by the text. Check that figures and tables are first cited in numerical order.

**8. Citation mechanics**

- Check citation placement relative to punctuation and the order and grouping of multiple citations (for example, `[3], [5], [9]` versus `[3,5,9]`). Where the venue disallows a citation as a noun, use wording such as “as shown in [5]” rather than “as [5] shows.” Keep the chosen form consistent.
- Resolve every `\cite` key. Check whether a cited preprint has a published version.
- Inspect the **TeX-compiled bibliography** as well as the `.bib` or `\bibitem` source. The bibliography style controls author truncation, quotation marks, italics, abbreviations, punctuation, and field order.
- Check each entry for the fields appropriate to its type. Journal articles need journal, volume/issue, pages, and date; conference papers need proceedings, location, year, and pages when available; books need title, publisher location, publisher, and year; arXiv preprints need year and identifier. Check DOI and page-number treatment for consistency.
- Report missing, misplaced, or inconsistent fields with the reference number and `.bib` key or `\bibitem` line. Use the following IEEE-style entries as format examples, subject to the target venue's rules and verified metadata:

  - **Journal:** F. Liu et al., “Integrated sensing and communications: Toward dual-functional wireless networks for 6G and beyond,” IEEE J. Sel. Areas Commun., vol. 40, no. 6, pp. 1728–1767, Jun. 2022.
  - **Conference:** H. Lu, C. Vattheuer, B. Mirzasoleiman, and O. Abari, “NeWRF: A deep learning framework for wireless radiation field reconstruction and channel prediction,” in Proc. Int. Conf. Mach. Learn. (ICML), Vienna, Austria, 2024, pp. 33147–33159.
  - **Book:** C. A. Balanis, Antenna Theory: Analysis and Design. Hoboken, NJ, USA: Wiley, 2016.
  - **arXiv preprint:** S. Rangan, “Generalized approximate message passing for estimation with random linear mixing,” 2010, arXiv:1010.5141.

Do not copy an example's metadata or author-list length into another entry.

**9. Word-choice register**

Flag informal or vague wording when a more precise term fits the context:

- `get` → obtain/achieve; `do` → perform/conduct; `look at` → examine/analyze.
- `a lot of`/`lots of` → numerous/considerable; `big`/`small` → large/large-scale or small-scale as context requires; `things`/`stuff` → components/factors.
- `good`/`bad` → favorable/degraded or a quantitative statement; `pretty`/`quite`/`very` → delete or quantify; `a bit` → slightly.
- `show` → demonstrate/indicate/report when the logic calls for one; `so` → therefore/consequently; `nowadays` → currently or delete; `kind of`/`sort of` → delete.
- `huge`/`tremendous`/`dramatic` → quantify; `obviously`/`clearly`/`of course` → delete unless the point is genuinely trivial.
- Remove stacked hedges (“may possibly be able to”). If words such as “always,” “never,” or “guarantees” overstate the technical claim, escalate rather than silently soften them.

**10. Non-native-English patterns**

Check these recurring constructions without treating every occurrence as an error:

- Empty openers: “As we all know” or unsupported “It is well known that” (delete or cite); “In order to” where “To” works.
- Missing articles before singular countable nouns, especially at sentence start. Place `respectively` at the end of a sentence with parallel lists; do not attach it to a single item.
- Check sentence-initial `And`, `But`, `So`, and `Because`; flag awkward or inappropriate uses. Flag legal phrasing such as `the said`, `aforesaid`, or `hereinafter`.
- Unpack stacks of four or more nouns with prepositions; flag incorrect plurals (`researches`, `informations`, `equipments`).
- Incorrect prepositions (`discuss about`, `emphasize on`, `investigate about`); inconsistent `compared with`/`compared to`.
- Ambiguous `since` (time or cause), `while` used for contrast where `whereas` is clearer, and excessive paragraph-opening `moreover`/`furthermore`/`besides`. Check `Besides` when the intended meaning is `In addition`.
- Double comparatives (`more better`, `most optimal`, `more superior`) and `the proposed` used without a noun (“the proposed outperforms” → “the proposed method outperforms”).

**11. Figure-reference phrasing**

- Prefer direct descriptions such as “Fig. X shows/compares/reports/plots ...” over “Fig. X tells us ...,” “Fig. X answers how ...,” “Fig. X reveals the question of ...,” or “Let us see from Fig. X.”
- Check that results text reports what the figure shows—values, trends, or crossings—and then gives a short interpretation. Flag repetition of the method or long passages that add no finding.
- Do not impose a paragraph count. Put optional compression under **Optional polish**; if the paper exceeds its page limit, state that directly.
- Escalate a judgement that lacks the mechanism or evidence needed to support it.

**12. Captions**

- Check that captions make sense without the body text. Fragments are acceptable if used consistently.
- Keep grammar, final punctuation, and terms consistent across captions, legends, and body text.
- Follow the venue's placement convention: figure captions below figures and table captions above tables.
- Use subfigure labels consistently (for example, “Fig. 3(a)”). Match caption parameter values to the parameter table.
- Escalate a caption conclusion that the figure does not show.

**13. Figures and tables as objects**

- Match legend and axis-label terms to the body text. Put units on axes.
- Mark the best value in each comparison consistently (for example, bold or underline), including comparisons where the proposed method loses.
- Apply one table-rule style, usually booktabs without vertical rules if the venue permits it. Align numeric columns consistently, preferably by decimal point.
- Use `N/A`, an em dash, or a blank consistently for missing values. Keep row and column order consistent across comparable tables.
- Check that figure text remains legible at print size.

**14. Visual figure-to-text consistency**

- View every figure and subfigure at readable resolution in the rendered paper or original image file, alongside the LaTeX source. Captions, OCR, and source text alone do not count as a visual check.
- Compare visible modules, connections, arrow directions, processing order, branches, and input/output relationships with the body text.
- Match symbols, subscripts, superscripts, vector/matrix styling, labels, and legend encodings to the definitions, equations, and prose.
- Inspect each figure at its place in the queue. When it is mentioned again, refer back to that inspection.
- For a mismatch, give the figure/subfigure number, the specific visual element, and the relevant source lines. Suggest a correction only if the intended meaning is clear.
- Put meaning-changing structural or symbol conflicts under **Escalations**. If a figure is missing, unreadable, or inaccessible, mark it **not visually verified** and say what is needed.

## Do Not Flag

Avoid findings based only on personal preference:

- A style choice used consistently, such as `Fig.` versus `Figure`, citation grouping, or bold-italic versus bold-upright matrices.
- Passive voice or first-person plural when clear and appropriate.
- A long sentence that is grammatical and clear.
- Established terms such as pilot contamination, water-filling, or beam squint.
- The author's professional voice; sentence-initial “However,” with a comma; or “Fig. 1 shows” versus “As shown in Fig. 1.”
- A defect already logged at another position. Use a recurring-pattern entry instead.
- Text in a dead zone during `--both`.

Put defensible but optional rewrites in **Optional polish**, not the main errata.

---

## Recurring Patterns

For a repeated error, write one entry with:

- the correction rule (for example, `get` → `obtain`);
- every location and line number;
- the total count; and
- a global replacement if it works in every context, or a note that each occurrence needs individual judgement.

Do not write “and similar issues elsewhere,” “et passim,” “throughout the paper,” or “numerous other instances.” The author needs the full location list.

---

## Escalations

A finding that changes technical meaning needs a separate decision. Examples include a wrong symbol in an equation; a value that contradicts the conclusion; a sign, subscript, or transpose error; an implausible unit; an axis label that names the wrong quantity; a caption claiming a result absent from the figure; or a definition that conflicts with later use.

Put these findings at the top of `review_minor.md`, above the errata. For each one, state what the paper says, why it conflicts with other material, and what needs checking. Suggest a correction only if the intended meaning is unambiguous. In `--both`, cross-reference the relevant major item.

---

## Output Format

Write `review_minor.md` incrementally as positions are reviewed. Use these sections:

**Calibration.** In one or two sentences, give the mode, source file, venue, any inferred style conventions, and whether a dead-zone list applies.

**Escalations.** List meaning-changing findings first. Write “None” if there are none.

**Errata by position.** Use one block per queued position, in document order:

> **`4.2 (lines 210–248)**
>
> | Line | Category | Current text | Suggested | Note |
> |------|----------|--------------|-----------|------|

- Quote enough current text verbatim to locate the issue.
- Label the category `M1`–`M14` and its short name (for example, `M6 units`).
- Put the actual replacement in `Suggested`. If the figure itself needs editing, describe the specific edit there.
- For `M14`, give the figure/subfigure and visual element with the source line; quote visible labels exactly. Record every figure as visually checked, skipped under the dead-zone rule, or not visually verified, with a reason for any gap.
- Use `Note` only when the reason is not obvious.
- Include every queued position, even `swept, none found` and `skipped: dead zone`.

**Recurring patterns.** Give the rule, complete location list, count, and replacement note.

**Optional polish.** Use the same table format, separate from errors.

**Consistency decisions needed from the author.** For valid alternatives used inconsistently—US/UK spelling, `Fig.`/`Figure`, matrix convention, citation grouping—give the count for each form and a recommendation.

**Out-of-scope observations.** In `--minor` alone, list structural, novelty, or evidence concerns briefly and suggest a major pass. Omit this section in `--both`.

**Statistics.** Report positions swept, positions with findings, total errata, recurring patterns, and escalations.

This pass does not give a verdict, acceptability recommendation, or rejection-risk assessment. If the user asks for one, run the major track.
