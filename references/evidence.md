# Evidence and design basis

Prepared 2026-09-09. The author selected the following two papers for this version. Their public HTML versions were read for structure, exposition and language. No third paper or private correspondence is part of the public evidence base.

## Public corpus and reading coverage

**P1. Nero Ziyu Li, _Fractal dimensions for Iterated Graph Systems_, arXiv:2212.01987v4, 28 May 2024.** [Versioned source](https://arxiv.org/html/2212.01987v4).

Read the abstract, introduction, definitions, examples and proof sections 2–4. This is the author preprint; the journal version was not checked. The bibliography's cited works were not independently reviewed.

**P2. Ziyu Neroli, _Iterated Graph Systems (I): random walks and diffusion limits_, arXiv:2603.13798v3, 7 August 2026.** [Versioned source](https://arxiv.org/html/2603.13798v3).

Read the abstract and introduction; closely examined resistance and local-mass arguments in section 2, including the estimates leading to the walk dimension. Also examined the transition to metric limits, selected section 3 arguments, and section 4's reduction, conclusion and conjectural outlook. Reading combined formula-bearing passages and prose-focused extraction. This was an exposition study, not a complete proof audit, independent numerical reproduction, or Lean verification.

## Observations and their editorial use

The following are observations about the selected text, not claims about every sentence's authorship or all future preferences.

| Source location | Observation | Editorial use |
|---|---|---|
| [P1 §1.2](https://arxiv.org/html/2212.01987v4#S1.SS2) | Results are previewed and the technical difficulties located. | State the destination and identify the actual obstruction. |
| [P1 §3.2](https://arxiv.org/html/2212.01987v4#S3.SS2) | A changing shortest-path example motivates the later construction. | Use examples to expose a failed shortcut. |
| [P1 §2.4](https://arxiv.org/html/2212.01987v4#S2.SS4) | Immediate results receive short proofs. | Preserve justified compression. |
| [P2 §1.1–1.3](https://arxiv.org/html/2603.13798v3#S1.SS1) | Comparisons, definitions and interpretations locate the contribution. | Explain what a formalism adds and what its quantities mean. |
| [P2 §2.2](https://arxiv.org/html/2603.13798v3#S2.SS2) | Local estimates precede a shared scaling result and its next use. | Order prerequisites and explain the resulting mechanism. |
| [P2 §4.2](https://arxiv.org/html/2603.13798v3#S4.SS2) | The outlook identifies missing theory before conjectural conclusions. | Keep the boundary of established results visible. |

## Differences that should not become universal rules

P1's Notation 2.14 defines `\asymp` through a positive limiting ratio; P2's opening of section 2 defines it through two-sided bounds. Read the current manuscript's convention before editing it.

Both texts contain compressed arguments and more explanatory passages. P1 also contains broad promotional language; P2 uses emphatic interpretation in places. The skill does not reproduce every surface feature or assume that newer prose is always preferred.

## Explicit preferences and editorial extensions

The commissioning author's explicit proof-writing preference is to avoid unnecessary abbreviation variables. The requested product is a pipeline that revises AI-generated or other drafts in his logic, language and style. These are requirements supplied by the author, not preferences inferred solely from the papers.

The five-stage workflow, before/after comparison, local reasoning checks, output contract, empirical-science extension and regression cases are new editorial design. British spelling is a tentative default. The public skill is self-contained and includes no private style-guide files, personal correspondence, internal task identifiers, or private Drive links.

## Calibration limits

These two papers support an author-informed starting point. They do not establish a universal human style, a reliable detector of AI authorship, or broad effectiveness across scientific disciplines. Assistance and revision history have not been established sentence by sentence.

Use fresh drafts and the author's actual editing choices to improve the rules. Record the task, competing revisions, preferred choice and reason; preserve the scope of a preference. The synthetic evaluation cases test intended behaviour, not measured similarity to a held-out corpus.

## Scope consolidation, 2026-09-11

The author requested a paper-only public skill under the name `neroli-scientific-writing`. The former local academic-writing reference was reviewed against this workflow: motivating gaps, purposeful examples, difficulty-dependent proof length, explicit light-edit and translation boundaries, correction notes, and the preference against unnecessary abbreviation variables are retained. Overlapping rules are expressed in the workflow and its existing references rather than duplicated in another guide. No additional paper was read for this consolidation. Non-paper personal style and its private provenance remain outside this package.

## Author feedback on manuscript structure, 2026-09-11

The author explicitly requested five rules: an abstract of no more than five sentences; main theorem statements repeated in the introduction using their body numbers; a relevant model figure in the introduction; a table of contents immediately after the abstract; and normally at most three, absolutely at most five subsections per section. These are author instructions, not statistical inferences from the two-paper corpus.

The author also supplied a current revision of P2 as an introduction exemplar. Its abstract and introduction were inspected for organisation and typesetting: it uses a DHL figure and non-counting theorem restatements that refer to body labels. This additional reading was limited to exposition, not a proof audit. The public package records the reusable pattern and preferences, without distributing the private project URL, manuscript, figure or contact details. The short LaTeX example in the argument reference is newly constructed.

## Author feedback on worked calculations, 2026-09-11

The author requested that the main theorem be followed by a concrete calculation showing how to use it. This is an explicit author preference. The requirement to distinguish exact values, finite bounds and numerical approximations applies when constructing that calculation. The public rule records the preference without reproducing an unpublished manuscript or its numerical results.

## Author feedback on introductions and equation presentation, 2026-09-11

The author requested an engaging opening that naturally leads to the paper's question, followed by background on the area's progress, main theorem statements with their body numbers, and a final Lean formalisation subsection. The author explicitly described this as an adaptable example, not an obligatory sequence or historical opening. The prohibition on formula boxes is also an explicit preference, not an inference from the corpus.

The linked [paper's introduction](https://arxiv.org/html/2603.13798v3#S1) was read again for this update. It moves from a historical conjecture to a specific unresolved problem and the paper's purpose, followed by Background, the model, Main results and Formalisation by Lean. The final subsection distinguishes proved formal statements from external hypotheses. This reading supports the organisational example; no Lean code was audited or compiled. The rule requires each new manuscript's own evidence for its history and formalisation claims.

## Clarification: one results subsection and flexible subdivision, 2026-09-11

The author clarified that the introduction should collect its main results in one subsection, following the order of the body sections, and that three subsections per section must not be treated as a target. This supersedes any interpretation of the earlier subsection guideline as a fixed template; the maximum of five remains. The [Main results subsection of P2](https://arxiv.org/html/2603.13798v3#S1.SS3) was reread: it presents graph results from Section 2, diffusion results from Section 3, and the random-model result from Section 4 in one connected overview. Its body sections use different subsection counts. These observations support the explicit preference and do not require copying the exemplar's topics, theorem count or full introduction structure.
