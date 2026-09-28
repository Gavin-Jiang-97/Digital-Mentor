# Major Revision Track

Loaded for `--major` and for the first stage of `--both`. Do not load `minor-track.md` in the same pass.

**Scope of this track.** Everything that could cause rejection, leave a stated claim unsupported, or block a reviewer from understanding or reproducing the work. Grammar, spelling, notation typesetting, units, citation formatting, and word-choice register are **out of scope** — they belong to the minor track and reach it via the handoff list.

**Every item in this file's output is a Major item.** There is no Minor section here. This is deliberate: in the previous single-pass design, findings that failed the Major bar sank into a Minor block and disappeared from the author's attention. Here, a finding that fails the Major bar goes to **Handoff to minor pass** as a one-liner. Nothing is deleted for failing to clear the bar; it is routed.

## Phase 1 sequence

1. Read the entire manuscript.
2. Run the three pre-judgment audits (below). Track them with `todo`.
3. Assess the manuscript across the major-track dimensions.
4. Apply the severity model, including the **promotion check**.
5. Produce the output (see Output Format).
6. **Stop and wait for user confirmation before any edits.**

## Pre-Judgment Audits

These are constructive, not evaluative: you build an artifact, then read defects off it. This is why they precede the dimensions, which are judgment-based and satisfied by spot-checking. Each catches a defect class that reading-and-judging reliably misses.

### Audit A — Derivation chain

Walk the method section equation by equation and tabulate:

| Eq. | Purpose | Consumes | Introduces | All symbols defined earlier? | Approximation invoked | Links to next step? |
|-----|---------|----------|------------|------------------------------|----------------------|---------------------|

- Any row with **"defined earlier? = No"** is a definition-order defect. A quantity discussed, rescaled, or absorbed into another quantity before that quantity is defined is unreadable even when the mathematics is correct. Report the fix as reordering or forward-declaring, not as adding text.
- Any **approximation with no stated assumption**: name the assumption the step silently requires.
- For every random quantity in the "Introduces" column, record whether its **distribution is stated**. Where a random quantity is transformed — normalized, divided through, weighted, projected, stacked — the distribution of the transformed quantity must be restated, not inherited silently. A transformation that changes a noise term's covariance while the paper continues to assert the original one is a model-level defect, not a notational slip.
- The **"Links to next step?"** column feeds D4 (cohesion). Fill it for every row; do not report it here.
- Re-derivation and sign/dimension verification belong to D7; use this table as its worklist so no step is skipped.

### Audit B — Symbol ledger

For every symbol: where defined, times used, dimension, collisions.

- **Defined but never used again** is as much a defect as undefined. Flag it.
- Flag two symbols carrying overlapping information with no stated relation, and any quantity whose value is never given anywhere.
- Where two quantities are physically linked, ask whether one can be expressed as a function of the other with a single new factor rather than both introduced independently. Fewer independent symbols is better; free factors belong in the simulation section.
- If ≥3 symbol defects exist, output a **proposed notation table** (current → proposed → rationale). A defect list alone leaves the author to redesign the notation unaided.
- **Typesetting of symbols is not this audit's concern** — italic/roman/bold consistency goes to handoff. This audit is about identity, uniqueness, dimension, and economy.

### Audit C — Claim-to-evidence matrix

List every claim, including those implied by the title, the abstract, and each contribution bullet; map each to its support (specific figure, table, equation, proof, or citation).

- Claims with no support are the only legitimate basis for requesting new evidence.
- For each, give both remedies: **obtain the evidence**, or **narrow the claim** (including changing a word in the title). The second is usually correct at Letter length. Where the cheap remedy belongs in the review and the expensive one does not, route them separately per Output Format.
- Figures or tables supporting no claim are candidates for removal — say so, since page budget is usually the binding constraint.
- This matrix is the precondition for the severity self-checks: without it, "name the claim this Major invalidates" is satisfiable by inventing a claim after the fact.

## Review Dimensions

Work through these in order. **Each dimension must produce a coverage receipt in the output** — either its findings, or an explicit "checked, no findings" with one clause of evidence for what you checked. Silence on a dimension is not permitted; it is the mechanism by which a dimension gets skipped without anyone noticing.

Four dimensions belong entirely to this track: **D3, D4, D7, D8**. Eight are shared with the minor track but ask a different question here — for those, the scope line states what is yours and what is handoff. D13 (language) has no major-track component at all.

### D1 — Target journal positioning and style fit

*Major scope: genre and evidence-level mismatch. Handoff: page count, formatting, template compliance.*

- Assess against the venue fixed in Phase 0. If none was provided, apply generic standards for a rigorous archival journal and say so.
- Does the paper match the expected balance of theory, system discussion, methodology detail, and empirical evidence for that venue?
- Flag venue mismatch, such as magazine-style exposition submitted as a theory-heavy paper, or transaction-style derivation submitted where broader system insight is expected.
- Check your own recommendations against the page budget. If everything you ask for cannot fit, name what should be compressed to make room, and move whatever the venue does not require to the reviewer's notes.

### D2 — Problem setting, system scenario, and assumptions

*Major scope: assumptions that change the problem. Handoff: assumptions that are merely undisclosed and fixable in one sentence.*

- Is the scenario clearly defined: topology, channel conditions, resources, information availability, mobility, hardware, coordination?
- Are core assumptions explicit, internally consistent, practically meaningful, and realistic for the claimed deployment?
- Flag hidden assumptions, overly idealized premises, missing operational constraints, or assumptions that make the formulation unrealistic or trivial.
- Separate two distinct cases: an assumption that **makes the problem easier than the one claimed to be solved** is a substantive defect and stays here; an assumption that merely **simplifies exposition** is a disclosure issue — one sentence plus a limitation note — and goes to handoff.

### D3 — Contributions and boundaries

*Entirely major-track.*

- Are contributions, novelty, scope, and boundary conditions clearly stated?
- Flag vague contribution claims, insufficient differentiation from prior work, or potential stated as established fact.
- When the method combines existing components, require the author to state the technical increment explicitly. Reviewers ask this first, and it must be answered in the paper rather than left to inference.
- Read each contribution bullet against Audit C: a bullet asserting more than one thing needs each part supported, not just the part the author had evidence for.

### D4 — Logical structure and narrative thread

*Entirely major-track.*

- Do title, abstract, introduction, body, and conclusion form a coherent storyline?
- Does the abstract contain background, gap, method, main conclusions, and significance?
- Does the introduction establish motivation? Does the conclusion summarize with honest boundaries rather than repeating earlier content?
- **Assess cohesion at subsection level, not only section level.** For the method section in particular, state explicitly whether its subsections read as one developing argument or as separately drafted blocks; use Audit A's "Links to next step?" column as the evidence. Fragmentation inside a complete section is easy to miss when other sections are absent — check for it deliberately.
- Flag isolated paragraphs, loose structure, logical jumps, or incomplete story arcs.

### D5 — Terminology, symbols, and conceptual accuracy

*Major scope: undefined, colliding, or dimensionally wrong symbols; invented terminology; anything blocking comprehension. Handoff: italic/roman/bold consistency, subscript styling, abbreviation expansion mechanics.*

- Verify terminology is accurate and standard for the field. Flag invented terms where an established one exists, and require any new term to be positioned against the existing taxonomy so it does not read as renaming prior work.
- Check that concepts, variables, sets, indices, matrices, dimensions, and operators are defined before use and used consistently.
- Apply **symbol economy**: reuse an existing symbol where possible; express a new quantity as a function of existing ones rather than as an independent definition; push free factors to the simulation section. Report this as a positive instruction, not only as defect detection.
- Draw on Audit B. Flag symbol reuse, overloaded notation, missing definitions, unused definitions, dimension inconsistencies, reversed causality, and ambiguous statements.

### D6 — Internal consistency and definition order

*Major scope: model-versus-method disagreement, definition-order inversion, implementation leakage. Handoff: numeric or naming mismatches across sections that do not change any claim.*

A paper is written for a reader, not as a transcription of the authors' code. Where a simplification aids comprehension, prefer it over fidelity to the implementation; the checks below are its specific consequences.

- **Model versus method agreement.** If the method operates on a quantity, structure, or perturbation the model does not contain, that is an inconsistency. The default remedy is to **amend the earlier model so it covers the later usage**, since the method reflects what the work actually does. Do not default to demanding experiments that justify the mismatch.
- **Forward references.** Any quantity discussed, absorbed, rescaled, or bounded before it is defined must be reported, with the fix stated as reordering or forward-declaring.
- **Implementation leakage.** Preprocessing, normalization, clipping, or discretization that is semantically part of the model but appears only in the simulation section belongs in the model section, because it determines the domain of the modeled quantities and the units of the metrics. Conversely, flag genuinely implementation-level detail sitting in the model section.
- **Numeric and verbal consistency.** Cross-check values, method names, and condition labels across abstract, body, figures, tables, captions, and algorithm blocks. A divergence that changes what a result asserts stays here; one that is merely inconsistent labelling goes to handoff.

### D7 — Method soundness and theoretical guarantees

*Entirely major-track.*

- Is the method specified at the level needed for scrutiny and reproduction?
- **Require a numbered algorithm block** for any procedure that is multi-stage, iterative, or branching and is currently carried by prose alone. The test is whether a reader can implement every step uniquely from the text. In particular, any **selection, pruning, thresholding, or candidate-retention criterion must be given as a formula with its threshold or retained count** — a qualitative description ("identifies values that produce strong alignment") is an algorithm-definition gap, not a missing detail, and is Major whenever it blocks reproduction.
- For iterative, optimization-based, or learning-based methods: are convergence, stability, and stopping conditions addressed where relevant?
- **Computational complexity is a default expectation for any paper whose contribution is an algorithm, not a conditional one.** The complete absence of a complexity statement (an expression, an operation count, or a measured runtime) is itself reportable — do not wait for the paper to make a cost claim before raising it.
- **If the paper claims lower cost than an alternative, require an explicit cost accounting** in whatever unit governs the comparison. A cost claim without a cost measurement is unsupported, and its absence also makes the reported comparison unverifiable as fair.
- If optimality, near-optimality, or performance guarantees are claimed, are they proved, with assumptions explicit?
- If a guarantee is absent, judge whether the paper is honest about it. When authors disclose that a borrowed result's guarantees do not transfer, that is correct practice — but a bare disclaimer is insufficient. Direct them to state which approximations are made, which properties are retained, and how the gap is compensated empirically. Reframe such passages as a labelled remark rather than leaving them as self-negation.
- Using Audit A's table as the worklist, independently re-derive each step: verify signs, dimensions, transposes, and that any quantity claimed consistent with an earlier result actually is. Check whether two equations encode the same information twice, or a coefficient appears in one equation and is silently rescaled in another. **Report confirmations as well as contradictions** — the author needs to know which parts are safe to build on.

### D8 — Claims versus evidence

*Entirely major-track.*

- Draw on Audit C. Flag overstatements, absolutized conclusions, and claims exceeding evidence.
- Flag trend-based judgments presented as certainties, and potential capabilities presented as verified ones.
- For each unsupported claim, offer both remedies: obtain evidence, or narrow the claim.

### D9 — Simulation design, parameterization, and result sufficiency

*Major scope: reproducibility gaps, missing central comparisons, unexplained anomalies. Handoff: parameter-table formatting, trial-count phrasing.*

- Are settings, baselines, metrics, datasets or channel models, parameter ranges, noise and mobility assumptions, and randomization protocols specified well enough to reproduce? Reproducibility is not negotiable at any venue and any missing item here is a legitimate finding regardless of page limit.
- Do the simulations validate the stated contributions, rather than showing generic aggregate gains?
- Are parameter settings reasonable, practically motivated, and consistent with the system model?
- **Scale evidence expectations to the venue.** At Letter length, the bar is that each main claim has direct support. Ablations, sensitivity sweeps, robustness studies, and extra baseline families are **desirable, not mandatory**: unless Audit C shows a specific stated claim has no other support, they do not belong in the review — put them in the reviewer's notes. Do not chain "no theoretical guarantee" into a mandatory full experimental battery.
- **Where a comparison is central to the paper's argument, missing it is a Major item; where it would merely broaden the evidence, it goes to the reviewer's notes.** Judge which by asking whether a reviewer could accept the paper's main conclusion without it.
- Check baseline **intelligibility**: every compared scheme must be identifiable from its name and description. Naming a scheme only by what it lacks ("without X") fails this test whenever the reader cannot then determine what it actually does — name the concrete method instead. Unintelligible condition naming stays here when it blocks reproduction; otherwise it is handoff.
- Check metric interpretability: if metrics are computed in a transformed or normalized domain, is that domain stated, and is at least one metric physically meaningful for the application?
- Check aggregation and dispersion: are results averaged over enough trials, is variability reported, and is the aggregation rule stated?
- If methods being compared consume different computational budgets, that must be disclosed alongside the accuracy comparison.
- **Counter-intuitive results must be explained or self-audited.** Flag any result that violates an obvious plausibility ordering: a method using strictly more information performing strictly worse than one using less; error increasing as SNR, bandwidth, sample count, or observation length increases; performance dropping when a module is added. Reviewers read an unexplained inversion as baseline mis-tuning or an implementation error, and that doubt propagates to every reported gain, not just the anomalous curve. Require either a mechanistic explanation tied to the scenario, or a stated self-check of the affected implementation.

### D10 — Redundancy, repetition, and over-detail

*Major scope: over-detail that weakens the main thread; structural duplication. Handoff: repeated sentences, wordiness.*

- Flag unnecessary technical detail accumulation and content repeated across sections.
- For repeated content, keep the best-placed instance and compress or remove the rest.
- Flag long paragraphs that pile up concepts without explanation.
- Recommend compression where over-detail weakens the main thread — and name which passages to cut when you are also asking for new content.

### D11 — Literature review and related work

*Major scope: missing reference categories, selective comparison, misrepresented prior work. Handoff: preprint-versus-published, citation formatting.*

- Is related work representative, well-categorized, and fair?
- Flag missing reference **categories** rather than prescribing a count. If you do suggest a target count, label it as an assumption about venue norms unless you can verify it, and prefer asking the user when they know the venue.
- Flag one-sided or inaccurate summaries of prior work.
- Where the paper does not compare against an apparently relevant prior method, require either the comparison or an explicit stated reason — otherwise it reads as selective comparison.

### D12 — Figures, tables, and key module quality

*Major scope: visual evidence not matching the claimed object of study; figures that do not support their argument; title accuracy. Handoff: caption grammar, significant figures, best-value marking, table rule styling.*

- Is the title accurate and concise? Does every title word have support (see Audit C)?
- Do figures and tables genuinely support the arguments? Are captions consistent with body text in substance?
- Does the visual evidence match the paper's claimed object of study? A paper claiming a structure-level result that only shows point-level examples has a visualization gap.

## Severity Model

Every finding in this track is a Major item. The question is not what severity to assign but whether the finding belongs here at all.

**Major bar** — would cause rejection on its own, OR leaves a stated claim unsupported, OR blocks a reviewer from understanding or reproducing the work.

Run these checks before output.

**Demotion checks** (route out of this file):

1. For each candidate item, name the claim it invalidates or the comprehension it blocks. If you cannot, route it to **Handoff to minor pass**.
2. For each requested experiment, state the claim it rescues (from Audit C) and its rough cost. If either is missing, move it to **Reviewer's notes**.
3. If an issue is fixable by rewording, reordering, or renaming, that alone does not disqualify it — effort is not the criterion. It stays if it blocks comprehension.
4. Missing-but-known-missing content (sections the author has not written yet) is not a Major issue. Collapse it into one checklist item.

**Promotion check** (route into this file):

5. For each item you are about to send to handoff or reviewer's notes, ask once: does it leave a stated claim unsupported, or does it block reproduction? If yes, it is Major regardless of how mechanical it looks. A wrong subscript inside a governing equation and a mislabelled axis on the figure carrying the main result are both "typos" by appearance and Major by consequence.

This check exists because the four demotion checks above are all one-directional. Without it, the pass systematically loses the class of findings that look small and matter greatly.

## Output Format

Produce ONLY the outline in Phase 1; no edits. Write to `review_major.md`, appending as each block completes.

**Calibration** — one or two sentences: mode, target venue, assumed norms (labelled as assumptions), manuscript stage, intended use of the review.

**Top Issues** — the issues that decide the paper's fate, one line each, in priority order. **No cap.** List as many as genuinely qualify; typically 3 to 8, but do not pad to reach a floor or truncate to respect a ceiling. Nothing new appears here; each line points to a numbered item below.

**Overall Assessment** — 1 to 2 paragraphs on strengths, weaknesses, and venue fit. State what you verified mechanically (re-derivations that checked out, consistency confirmed) alongside what is wrong; the author needs to know which parts are safe to build on. Where the Major count is high, say whether the causes are **concentrated** (one section needing a rewrite) or **spread** across the manuscript — that judgement is more useful than a count.

**Major Revision Items** — numbered, no cap. Do not merge distinct defects to hit a target count. Each item:

- **Issue**: description
- **Why it matters**: which claim it invalidates or which comprehension it blocks
- **Revision direction**: how to fix, cheapest adequate remedy first
- **Affected part**: specific section, subsection, paragraph, equation, or sentence

**Dimension Coverage** — a compact table with one row per dimension (D1-D12): dimension / item numbers raised / or "checked, no findings" plus a clause naming what was checked. This is the receipt that no dimension was skipped.

Address these four checkpoints explicitly even when the paper handles them well — "currently adequate, no action needed" is a valid and useful finding:

1. system scenario and assumption realism,
2. symbol-system consistency,
3. theoretical guarantees or their absence,
4. sufficiency and reasonableness of the simulation setup.

**Suggested Revision Order** — grouped by dependency and by whether new experiments are needed, so rewriting can proceed in parallel with experiments.

**Acceptability for the Target Journal After Revision** — accept / minor revision / major revision / reject, with the one or two conditions that determine which. This is the verdict on the whole manuscript; do not conflate it with per-item severity.

**Most Likely Rejection Reasons If Submitted Now** — numbered. For a draft, retitle this as risks at submission time after completion, and exclude items that are merely unwritten.

**Dead zones** (only in `--both`) — sections, subsections, or paragraphs slated for rewrite, deletion, or merging. The minor pass will not proofread inside these. One line each.

**Handoff to minor pass** — mechanical items noticed during this pass, one line each with location, no elaboration. In a `--major`-only run, this tells the user what a minor pass would cover.

**Calibration note for the author** — short, and only for first-time or early-career authors: separate "not yet written" from "written incorrectly," and name the one or two highest-yield changes.

Deduplicate before output: one home per defect, cross-references elsewhere.

### Reviewer's Notes (chat reply only, never in the file)

Findings that are real but should not be asked of the author now — typically ablations, extra baseline families, robustness studies, and other work the venue does not require at the current evidence level.

One line each: the finding, plus why it need not be done now. **No item cap** — this block is cheap, lives only in the chat, and exists so the model's alternative is not to silently drop such findings or smuggle them into the review where the author will do the work anyway. Keep each line to one sentence so the block stays scannable.
