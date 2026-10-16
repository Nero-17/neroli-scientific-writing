# Lean formalisation statements

Use this guidance when drafting or revising a manuscript's Lean formalisation note. Prefer one compact paragraph with four informational parts: version and coverage, verification status, external inputs, and code availability. These are not four mandatory sentences or four separate paragraphs; adapt the wording and sentence count to the actual development.

## Lead with the strongest supported coverage

The author wants the extent of formalisation to be prominent. When supported, explicitly write **all mathematical results of this paper**, rather than weakening full coverage to "the main results" or "some results". When coverage is complete within particular sections, write **all mathematical results in Sections X–Y and Appendices A–B**. Use **all mathematical content** only when the definitions, constructions, arguments and calculations covered by that broader phrase have also been accounted for. Prefer "all" within a precise verified scope to vague wording such as "generally formalised".

State the Lean version and the mathlib revision used, when available. Check that the formal statements represent the paper's mathematical objects and hypotheses: encoding theorem statements or proving an implication from assumed core conclusions is not full proof coverage. Do not include unresolved conjectures or unverified numerical experiments in a claim that all results have been proved. Mention a material exception briefly when needed; do not append generic disclaimers to an otherwise accurate statement.

## Report verification and external inputs precisely

Describe a successful build and the absence of incomplete proof dependencies only when supported by checks for the stated scope. Prefer "The formalisation builds successfully, and none of these proofs depends on `sorryAx`" to vague claims about having "no errors". A successful build or a source search for `sorry` alone does not establish this: inspect theorem dependencies, for example with `#print axioms`.

Identify every unformalised external mathematical input by its precise literature citation and theorem or lemma number, and identify the paper's results that rely on it. Say whether the code declares it as an axiom or accepts it as an explicit hypothesis. Such a statement describes formal proofs relative to those inputs, not formal proofs of the inputs themselves. Results already proved in mathlib are not unformalised black boxes. Check explicit theorem hypotheses as well as axiom dependencies; an assumed core result may not appear in `#print axioms`.

When verified, state that the only remaining axioms are `propext`, `Classical.choice` and `Quot.sound`. Do not automatically copy this claim between projects; other dependencies, including native-evaluation axioms, must be reported accurately. Without external inputs, say so directly. With a short list, name the inputs in the paragraph; with a long list, use a compact adjacent table mapping paper result, external citation and Lean declaration, rather than an overloaded sentence.

## End with the corresponding code

Give the repository URL, optionally displayed on its own line using `\url{...}`. Prefer an existing release tag or commit identifying the code corresponding to the manuscript; do not invent one. Keep build commands, the full paper-to-Lean declaration mapping and detailed dependency reports in the repository README or other appropriate repository documentation. Creating or publishing a release is a separate action, not implied by editing this paragraph.

## Adaptable wording

The following is a template, not a verification claim. Replace the bracketed fields with checked information and adapt the coverage and external-input wording to the actual project:

> We have formalised all mathematical results of this paper in Lean [version], using mathlib [revision]. The formalisation builds successfully, and none of these proofs depends on `sorryAx`. The formal proofs of [paper results] use [precisely cited external results] as [declared axioms / explicit hypotheses], whose proofs are not formalised here; apart from these inputs, the proofs depend only on `propext`, `Classical.choice` and `Quot.sound`. The code corresponding to this version of the paper is available at [repository URL] ([release or commit, when available]).

If there are no unformalised external inputs and the dependency audit supports it, replace the third part with:

> These proofs depend only on Lean's standard axioms `propext`, `Classical.choice` and `Quot.sound`, with no additional axioms or unformalised external inputs.

If evidence is unavailable, flag the missing information to the author rather than inserting an unsupported claim into the manuscript or starting a formalisation project merely to fill the note.
