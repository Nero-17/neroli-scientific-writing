---
name: humanize-scientific-writing-neroli
description: "Rewrite scientific drafts, including AI-generated text, through an author-informed pipeline for argument, exposition, language, and final comparison. Use for substantive manuscript revision, proof exposition, introductions, abstracts, and translation of scientific manuscripts in Nero Ziyu Li's preferred style. Respect explicit light-edit requests. Do not activate for applications, research statements, emails, non-paper translation, ordinary scientific Q&A, or a proof-correctness review alone."
---

# Humanize Scientific Writing — Neroli

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

## 2. Recover the argument before changing the wording

Identify the central question, relevant prior result, specific obstruction, proposed mechanism, conclusion, and remaining limitation, wherever present. This is a compact working outline, not a compulsory report or six-paragraph template.

Record the scientific features that must survive the edit: hypotheses, quantifier order, domains, exceptional sets, constant dependencies, limits, claim status, notation definitions, equation labels, citations, and meaningful examples. For an empirical passage also retain units, sample sizes, experimental conditions, uncertainty and the distinction between observation and explanation.

Read [references/argument-and-proof.md](references/argument-and-proof.md) when revising a proof, a section's logic, or a technical introduction. Use the current manuscript's definitions even when a familiar symbol is used unusually. Never transfer a convention or result from the exemplar papers into a new manuscript.

## 3. Repair the exposition at the level that is needed

Make the relationship between adjacent claims explicit. A reader should understand why the next definition, estimate, example, or case is needed.

- Replace a generic importance paragraph with the actual question and the concrete limitation of existing work, when supplied.
- Introduce a technical object with its purpose; after a difficult formula explain the mechanism or consequence when that adds information.
- Place an example where it explains a construction, exposes a failed approach, tests a hypothesis, or makes a conclusion usable.
- Preserve simple arguments as simple arguments. Expand the difficult step, not every step. Use case labels or upper/lower bounds when the proof genuinely splits.
- Connect a completed result to its next use when there is a real dependency. Avoid repeating a roadmap after every lemma.

Check the local reasoning needed to support an edited passage. If a claimed implication fails, do not hide it behind smoother prose. Make a correction when it is justified by the supplied material and explain the substantive change separately. If it cannot be repaired, identify the exact missing premise or argument and continue editing independent portions. Do not invent a lemma, strengthen an assumption, weaken a theorem, or change a conjecture into a result to make the text appear complete. Do not label a proof checked merely because it was edited.

## 4. Revise language in the chosen voice

Read [references/language-and-rhythm.md](references/language-and-rhythm.md) for sentence-level decisions. Prefer direct statements, concrete subjects and informative verbs. Retain technically necessary terminology, an intentional contrast, and a justified strong statement.

Remove repetitive promotion, empty transitions, needless nominalisations, and explanations that merely repeat a displayed formula. Do not use a forbidden-word list or replace every long sentence with short ones. Avoid substituting elegant synonyms for the same mathematical object.

**Do not introduce unnecessary abbreviation variables in mathematical proofs.** Retain meaningful objects and useful existing notation. A new symbol should identify an object or repeated operation that actually helps the reader, rather than shorten a single expression or conceal its dependencies. This preference does not ban definitions, constants, or standard notation.

Keep LaTeX commands, mathematical environments, labels and citation keys intact unless the requested change requires an update. Follow an existing consistent spelling convention; British spelling is a tentative default for a new English draft, not a requirement for all authors or journals. Preserve the target language and register in translation, including the strength of a supplied judgement and the distinction between a fact, a conjecture and an intention. Do not add personal anecdotes, application rhetoric or correspondence flourishes to a paper.

## 5. Compare and deliver

Compare the revision with the source, not just with how fluent the revision sounds:

1. Is the scientific claim the same, or is every substantive correction clearly identified?
2. Have all necessary conditions, qualifications, exceptional cases and dependencies survived?
3. Are proof steps and transitions justified rather than merely asserted?
4. Does each new symbol, paragraph, and structural change help the reader?
5. Do notation, cross-references, numerical values and claim status agree across the edited scope?

Check touched LaTeX cross-references or compile when the source and suitable tools are available and the change warrants it. Report only checks actually performed. A successful compile does not verify mathematics.

Return the revised text in the requested format first. Add a short note only for substantive changes, unresolved scientific issues, or requested explanations. Do not append stage logs, a compulsory style score, a generic disclaimer, or several alternative drafts. If the user requests an audit or change list, provide it. Stop when the contract and comparison checks are satisfied; do not keep rewriting merely to create more differences.

## Calibration and boundaries

[references/examples.md](references/examples.md) contains original worked examples; read it when the intended editing depth or a language decision is unclear. [references/evidence.md](references/evidence.md) distinguishes observed patterns, explicit preferences, and editorial extensions; read it when explaining or updating this skill's basis.

The current user's explicit requirements override this profile. The historical papers are evidence for editorial choices, not flawless templates, verified theorem libraries, or proof of exclusively unaided authorship. Preserve clarity and scientific accountability rather than attempting to certify that text was written by a human.
