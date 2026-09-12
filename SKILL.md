---
name: neroli-scientific-writing
description: "Rewrite scientific drafts, including AI-generated text, through an author-informed pipeline for argument, exposition, language, and final comparison. Use for substantive manuscript revision, proof exposition, introductions, abstracts, and translation of scientific manuscripts in Nero Ziyu Li's preferred style. Respect explicit light-edit requests. Do not activate for applications, research statements, emails, non-paper translation, ordinary scientific Q&A, or a proof-correctness review alone."
---

# Neroli Scientific Writing

Turn a supplied draft into scientific prose whose reasoning a reader can follow: explain the problem, expose the obstruction, introduce what resolves it, and state what the result actually establishes. Preserve the author's scientific position and useful individual voice. Apply the stages below within the requested passage; do not impose their names or a fixed outline on the manuscript.

This is an instruction-driven editing pipeline, informed by two mathematics papers and the author's explicit preferences. It requires no API, private files, or other skill. Its strongest grounding is mathematical exposition; adaptations to empirical science are editorial extensions.

## Scope

Use this skill for scientific papers and manuscript passages: abstracts, introductions, definitions, theorem and proof exposition, discussion, and faithful manuscript translation. It consolidates the paper-writing guidance previously held in Nero-style. Applications, research statements, correspondence and other non-paper writing are outside its scope. In a mixed request, apply these instructions only to the manuscript component. The skill is self-contained; it does not load personal correspondence or require another writing skill.

## 1. Establish the editing contract

Infer the audience, genre, requested language, source format, and permitted depth from the request and draft. Ask only when an unresolved choice would materially change the result.

- **Default: substantive revision.** Reorder or rewrite prose where this improves the argument. Preserve scientific content, the actual proof strategy, and useful existing organisation. Do not stop at swapping adjectives.
- **Light edit / faithful translation / preserve my wording:** preserve the progression and emphasis, correcting language and local ambiguity. Do not silently apply a structural rewrite.
- **Draft from notes:** develop only supplied claims and support. Mark essential missing content instead of fabricating a complete research story.

If the input is an entire manuscript, inspect its overall structure, main claims, standing assumptions and notation before revising sections. Keep terminology and dependencies consistent across sections. If only an excerpt is available, work locally and state only material limitations; do not pretend to have checked the rest.

### Author's manuscript structure

Apply these explicit author preferences when drafting or substantively revising a complete paper. Apply the relevant rule to an abstract or introduction supplied alone; do not invent missing sections, results or assets for an excerpt. An explicit light-edit contract or the user's current instructions take precedence.

1. **Keep the abstract short: at most five sentences.** State the question and actual main conclusions; do not evade the limit with long sentences or a list of clauses.
2. **Restate the main theorems in the introduction under their original body numbers.** Include the statements themselves, not merely a list of references or informal claims. Use cross-references to the body labels, with the necessary definitions and hypotheses available to the reader. Preserve the exact mathematical content and the distinction between theorems and conjectures. See the LaTeX pattern in [references/argument-and-proof.md](references/argument-and-proof.md).
3. **Put a relevant figure in the introduction.** It should explain the model or construction: for example, a diamond hierarchical lattice when introducing an edge iterated graph system. Generate a mathematically faithful diagram or reuse an authorised source figure. Introduce it in the prose, provide a useful caption, and check its labels, file and rendered appearance. Do not insert a decorative or scientifically unrelated image.
4. **Place the table of contents immediately after the abstract.** In a complete LaTeX paper, put `\tableofcontents` after `\end{abstract}` and before the introduction.
5. **Let the argument determine the number of subsections; three is not a target or a required count.** A section may need no subsections, one, two, or more. Use only divisions that help the reader; never split, merge, or pad material merely to reach three or to make sections look uniform. Retain the author's ceiling of five subsections per section. Preserve necessary proofs and transitions instead of mechanically demoting headings.

6. **Follow the main theorem with a concrete worked calculation.** Choose a relevant nontrivial instance, substitute its parameters, and actually evaluate the quantities appearing in the theorem. Show the short derivation and explain what the computed value establishes. Merely naming an example or repeating the abstract formula is insufficient. When the theorem is restated in the introduction, give a compact calculation there and the full worked example after the body theorem. Keep the theorem general and label the example's special assumptions. Use only justified calculations, distinguish exact expressions, bounds and numerical approximations, and add no unnecessary proof abbreviations.

7. **Define the central objects formally before using them.** Put the main model in a numbered Definition in the introduction, after the definitions of its underlying objects. Give an auxiliary process a precise definition before the estimates that use it; a section opening is appropriate when the process serves that whole section. Specify the parameters, random inputs, independence, dynamics and endpoint conventions that distinguish the model. Ordinary explanatory prose should support, rather than replace, these core definitions.
8. **Place body theorems where their proofs are ready.** Develop the prerequisites in logical order, then normally state the main theorem and immediately prove it. A short constructive lemma may instead summarise a complete derivation immediately preceding it; make that proof relationship explicit and do not repeat the derivation. Do not put an early numbered body statement far from its proof merely for advance publicity; the introduction already provides the overview. A subsection's central conclusion deserves an explicit theorem when that is its mathematical role. Separate existence from an explicit formula or computability when they require different arguments, and check that the existence proof does not depend on material postponed to the computational part. See [references/argument-and-proof.md](references/argument-and-proof.md).
9. **Keep local organisation and examples close to their purpose.** Short stages within a numbered subsection may use unnumbered `\subsubsection*` headings, without adding them to the contents. Choose the heading level from the actual hierarchy; do not make every subsection follow this pattern. Integrate an appendix calculation into the body as an example when it directly explains a nearby result. Examples share the section's theorem counter, rather than having a separate numbering sequence: for example, `\newtheorem{example}[theorem]{Example}`.

### Introduction: engage, orient, state, and document

Open with something concrete that gives the reader a reason to continue: a sourced conjecture and its historical setting, a precise question, or another compelling mathematical starting point. Let that opening lead naturally to the unresolved question and explain what this paper does to answer it. Do not manufacture history, priority, or a complete solution where the paper provides only partial progress.

A useful progression is **opening -> Background -> Main theorems -> Lean formalisation**. After the opening, give enough background on the field's progress and remaining obstacles to orient the reader. Introduce the model or necessary definitions where they help, then collect the main results in one subsection and state the theorems with their body numbers. Present these results in the order of the body sections, using explanatory transitions to connect their questions, conclusions and dependencies; do not split the overview into separate result subsections by topic. Close the introduction with a Lean formalisation subsection when the paper has formalisation to describe; state its actual coverage and limitations. If that status is missing, flag it for the author rather than inventing a verification claim or a completed subsection.

This is a flexible writing pattern, not a mandatory historical opening, set of titles, or fixed section count. Match heading levels to the manuscript: Background will usually be a `\subsection` within `\section{Introduction}`, but can be a separate section when the organisation calls for it. Read [references/argument-and-proof.md](references/argument-and-proof.md) for the progression and formalisation details. Respect the editing contract and the existing subsection guidance; an additional model subsection can justify four introduction subsections.

## 2. Recover the argument before changing the wording

Identify the central question, relevant prior result, specific obstruction, proposed mechanism, conclusion, and remaining limitation, wherever present. This is a compact working outline, not a compulsory report or six-paragraph template.

Record the scientific features that must survive the edit: hypotheses, quantifier order, domains, exceptional sets, constant dependencies, limits, claim status, notation definitions, equation labels, citations, and meaningful examples. For an empirical passage also retain units, sample sizes, experimental conditions, uncertainty and the distinction between observation and explanation.

Read [references/argument-and-proof.md](references/argument-and-proof.md) when revising a proof, a section's logic, or a technical introduction. Use the current manuscript's definitions even when a familiar symbol is used unusually. Never transfer a convention or result from the exemplar papers into a new manuscript.

## 3. Repair the exposition at the level that is needed

### Global rule for theorem statements and definitions

Keep theorem statements as short as their precise content allows. When the conclusions form a progression and the final conclusion subsumes the earlier ones, state only the final conclusion in the theorem. If an intermediate conclusion is independently important, give it a separate lemma and its proof at the appropriate point in the argument. Routine intermediate steps belong in the proof. Preserve necessary hypotheses, quantifiers, parameter dependence and qualifications; do not discard a distinct conclusion that the final one does not imply merely to shorten the statement.

Do not put definitions inside theorem statements, including introduction restatements. Introduce all required definitions separately, before the result, using `:=` for symbolic definitions. Put an important definition in its own `\begin{definition}...\end{definition}` environment; a short auxiliary definition may stand in ordinary prose or display math outside the theorem. Keep definitions separate from lemma and proposition statements as well. Quantifying an arbitrary object under stated hypotheses, or asserting existence of an object as the theorem's conclusion, is not itself a definitional assignment. After moving a definition, retain its domain, dependencies and any existence or uniqueness justification needed to make it well-defined. Apply this rule to individual result edits as well as whole manuscripts.

Make the relationship between adjacent claims explicit. A reader should understand why the next definition, estimate, example, or case is needed.

- Replace a generic importance paragraph with the actual question and the concrete limitation of existing work, when supplied.
- Introduce a technical object with its purpose; after a difficult formula explain the mechanism or consequence when that adds information.
- Place an example where it explains a construction, exposes a failed approach, tests a hypothesis, or makes a conclusion usable.
- Preserve simple arguments as simple arguments. Expand the difficult step, not every step. Use case labels or upper/lower bounds when the proof genuinely splits.
- Connect a completed result to its next use when there is a real dependency. Avoid repeating a roadmap after every lemma.

Check the local reasoning needed to support an edited passage. If a claimed implication fails, do not hide it behind smoother prose. Make a correction when it is justified by the supplied material and explain the substantive change separately. If it cannot be repaired, identify the exact missing premise or argument and continue editing independent portions. Do not invent a lemma, strengthen an assumption, weaken a theorem, or change a conjecture into a result to make the text appear complete. Do not label a proof checked merely because it was edited.

### Let a geometric construction carry the explanation

For a constructive or geometric passage, keep the opening to the objects, conventions and hypotheses needed for the first operation. Explain the distinct operations in order, pairing each step's short explanation with its figure when a figure clarifies it. A concise lemma can then collect what these steps have proved. Preserve general quantifiers and the complete argument; an illustration of one parameter choice is not a proof of all cases. Neither three steps nor a half-page opening is a universal template.

Prefer mathematical symbols to prose inside a figure. Use coordinates, vector arrows and faint contextual geometry when they make the operation readable; remove a figure that adds no information. Read [references/proof-figures.md](references/proof-figures.md) when revising a geometric derivation or its figures for the detailed conventions and checks.

## 4. Revise language in the chosen voice

Read [references/language-and-rhythm.md](references/language-and-rhythm.md) for sentence-level decisions. Prefer direct statements, concrete subjects and informative verbs. Retain technically necessary terminology, an intentional contrast, and a justified strong statement.

Remove repetitive promotion, empty transitions, needless nominalisations, and explanations that merely repeat a displayed formula. Do not use a forbidden-word list or replace every long sentence with short ones. Avoid substituting elegant synonyms for the same mathematical object.

**Keep display mathematics selective.** Put short setup formulas and routine substitutions in the sentence when readable. Reserve displays for identities, derivations and conclusions that the reader needs to inspect. Reduce excessive displays by integrating prose and formulas, without removing hypotheses, labels or necessary reasoning. Display style for limits does not require a separate display.

**Avoid shorthand symbols and minimise intermediate variables throughout the manuscript, including proofs.** If an expression is already short, has no fraction and contains only a few letters or operations, write it directly instead of introducing a new symbol for it. For example, do not introduce `h:=\lambda p` or `\delta:=1-p` merely to save those few characters. Repetition alone does not justify an alias for such a short expression. Prefer a direct calculation in the original quantities over a chain of intermediate assignments. Apply this when reviewing inherited notation as well as when drafting. Retain variables that have an independent mathematical role, such as a quantified parameter, an integration variable or an object being constructed; this rule targets shorthand, not necessary mathematics. A fraction or a longer expression does not automatically justify an abbreviation either. Preserve dependencies, scope and grouping when substituting an expression back into the proof. See [references/language-and-rhythm.md](references/language-and-rhythm.md).

**Use `:=` for every symbolic definition.** Apply this throughout the manuscript, including inline definitions, proof-local choices, recursive assignments, endpoint conventions and introduction restatements. Preserve `=` for identities, evaluated special cases, conditions and equations characterising an implicitly defined object. In a chain, distinguish the definition from the subsequent calculation, as in `T(z):=\sum_{j\ge0}z^j=1/(1-z)`. Do not mechanically replace equal signs or invent abbreviation variables to turn a prose definition into a formula. Use `\mathbf` rather than `\mathsf` for the author's upright bold mathematical notation. Keep terminology consistent and descriptive; for example, a process stopped by killing at terminals is a *killed process*, not a *clean process*.

**Use `\displaystyle` for every limit expression, without forcing a separate display.** Inline formulas containing `\lim`, `\liminf`, or `\limsup` must use `\displaystyle`, for example `$\displaystyle\lim_{n\to\infty}a_n=a$`. Ordinary display environments already supply display style, so do not add a redundant command there. Choose inline versus displayed placement according to the sentence and formula; do not break every limit into a separate paragraph. Apply this to hypotheses, definitions, proofs and introduction restatements as well as conclusions. Preserve the limiting variable, one-sided direction, order of limits, quantifiers and mode of convergence.

**Prefer explicit limits to convergence arrows.** Write `\lim_{n\to\infty}a_n=a` rather than `a_n\to a` or `a_n\longrightarrow a`. State monotonicity separately when replacing `\uparrow` or `\downarrow`. Retain the variable, direction of a one-sided limit, order of iterated limits, and any uniformity or probabilistic mode of convergence; convergence in distribution must not become pathwise convergence. For inequalities ending in an arrow, give the inequality and the limiting statement separately. Prefer words for logical implications and parameter approaches in prose. Conventional arrows within limit subscripts, function signatures or connectivity notation may remain when they express the intended mathematical relation; this is not a blanket character replacement.

Keep LaTeX commands, mathematical environments, labels and citation keys intact unless the requested change requires an update. Follow an existing consistent spelling convention; British spelling is a tentative default for a new English draft, not a requirement for all authors or journals. Preserve the target language and register in translation, including the strength of a supplied judgement and the distinction between a fact, a conjecture and an intention. Do not add personal anecdotes, application rhetoric or correspondence flourishes to a paper.

**Do not use `\boxed` in manuscript text. Do not put formulas in boxes.** Use ordinary displayed or aligned mathematics, with equation numbers when useful. Remove presentational frames such as `\boxed`, `\fbox`, or framed equation containers in the edited scope while preserving the enclosed mathematics, labels and references. This does not remove a mathematical box operator or an end-of-proof symbol. See [references/language-and-rhythm.md](references/language-and-rhythm.md).

## 5. Compare and deliver

Compare the revision with the source, not just with how fluent the revision sounds:

1. Is the scientific claim the same, or is every substantive correction clearly identified?
2. Have all necessary conditions, qualifications, exceptional cases and dependencies survived?
3. Are proof steps and transitions justified rather than merely asserted?
4. Does each new symbol, paragraph, and structural change help the reader? Have short-expression aliases and dispensable intermediate variables been removed, including inside proofs, without losing dependencies or mathematical meaning?
5. Do notation, cross-references, numerical values and claim status agree across the edited scope?
6. For a complete paper, is the abstract at most five short sentences, followed by the contents; does the introduction contain a relevant figure and accurate theorem restatements with body numbers; are the main results collected in one subsection in body-section order, with each section using only the subdivisions its content needs rather than a fixed count; and is the main theorem followed by a checked, concrete worked calculation?
7. Does the introduction engage the reader with a concrete starting point, connect it to the paper's question, orient the reader before stating results, and accurately describe any Lean formalisation? Has the final LaTeX source in the edited scope been checked for `\boxed` and other presentational formula frames, including inherited formulas and theorem restatements?
8. Are the core models formally defined before use, body theorems adjacent to their proofs, and local headings and example counters consistent with the argument? Does every symbolic assignment use `:=`, with identities and characterising equations still using `=`?
9. Does each theorem state its final substantive conclusion concisely, with independently important intermediate conclusions moved to lemmas? Are all definitions outside result statements, using `:=` where symbolic and a Definition environment when important, with hypotheses and well-definedness preserved?
10. For an illustrated derivation, does each step explain an actual operation and sit beside its figure? Do symbols, coordinates, scales and arrow directions agree with the algebra, and does each figure add information? If a lemma closes the derivation, have the preceding steps proved its full statement without a duplicate proof?

Check touched LaTeX cross-references or compile when the source and suitable tools are available and the change warrants it. Report only checks actually performed. A successful compile does not verify mathematics.

Return the revised text in the requested format first. Add a short note only for substantive changes, unresolved scientific issues, or requested explanations. Do not append stage logs, a compulsory style score, a generic disclaimer, or several alternative drafts. If the user requests an audit or change list, provide it. Stop when the contract and comparison checks are satisfied; do not keep rewriting merely to create more differences.

## Calibration and boundaries

[references/examples.md](references/examples.md) contains original worked examples; read it when the intended editing depth or a language decision is unclear. [references/evidence.md](references/evidence.md) distinguishes observed patterns, explicit preferences, and editorial extensions; read it when explaining or updating this skill's basis.

The current user's explicit requirements override this profile. The historical papers are evidence for editorial choices, not flawless templates, verified theorem libraries, or proof of exclusively unaided authorship. Preserve clarity and scientific accountability rather than attempting to certify that text was written by a human.
