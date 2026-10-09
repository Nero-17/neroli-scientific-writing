# Argument and proof decisions

Use this reference for substantive revision. The current assignment controls how far the editor may change an existing draft.

## Build a reason for the next step

In an introduction, distinguish the broad subject from the specific research problem. Explain what an existing approach already achieves and which obstacle it leaves. State the contribution at the level supported by the manuscript. A classical construction may be useful in a new general setting without being a newly invented idea.

When the source supports it, organise the exposition around a progression such as:

> existing result -> remaining obstruction -> construction or estimate that resolves it -> resulting statement -> use or unresolved extension

This is a relationship between ideas, not a mandatory section order. An introduction can give an informal construction and restate a main result before the body develops the technical details. In the body, normally state the theorem once its prerequisites are available and then prove it immediately. A short constructive lemma can instead conclude its complete derivation, as described below. A short result does not need a miniature literature review.

The explanation of a hypothesis should say what breaks without it. If the supplied argument does not establish necessity, describe where the hypothesis is used instead of calling it necessary. Separate convenience of presentation from mathematical necessity.

### Keep the section's destination visible

Give a substantive section a mathematical job and a recognisable culminating result. Consolidate preliminary observations when they form one argument; retain a special family only when it tests a mechanism, establishes a needed case, or explains a boundary. A technically interesting subfamily can still distract from a global question. Do not pad a proof or retain side results merely to make a section look difficult, and do not remove a prerequisite because its later use is unobtrusive. Check downstream references before cutting.

An opening can simply recall previously established quantities and explain the next question. Do not create a subsection just for a short recall or repeat the full formal theorem before its eventual statement. A concrete example may open the argument when it reveals the mechanism; return to it after the general result only if the reader gains something new.

A useful progression is a positive criterion, a precise uncovered case, and the question whether that case reflects a limitation of the proof or occurs in actual models. Use this when the mathematics supports it. It is not a requirement to manufacture suspense, conceal a known counterexample, or impose the order in which the research happened. Select main-results statements for their role in the paper, not to give every section an equal number of theorems.

Ancillary observables with conditional existence can move to an appendix when the main classification uses other quantities. Leave a brief, accurate statement of their status and a pointer in the body; do not imply unconditional coverage. Conversely, keep a short calculation in the body when it directly explains the central mechanism. Neither all conditional results nor all computations belong in appendices.

For a computer-assisted construction, retain the construction idea, essential identities, exact checks and the logical implication from a successful check to the theorem in the paper. A repository can hold large allocations, certificates, verifier code and reproducible instructions; it must not become an unexplained substitute for the argument. When the author requests a clean supplementary repository, omit intermediate round logs and unrelated process records. Publishing a manuscript copy or pinning a particular revision follows the author's explicit choice, not an automatic writing rule.

### Subsection openings from the author's notes

An outline such as “a natural question is ...; we can approach it through ...; finally we prove ...” specifies a logical progression. Fill in the actual question left by the preceding result, identify the concrete mechanism used by the proof, and state the resulting conclusion. For a converse, make clear which implication remains to be established. Merely announcing that the next result is important does not supply a mechanism.

Use the surrounding definitions and proof to complete abbreviated notes. Preserve qualifications such as nonemptiness or eventual rather than immediate periodicity; do not invent a proof or a stronger conclusion to complete the prose. A short opening should orient the reader without reproducing the proof. Three sentences can work, but neither that count nor the phrase “a natural question” is compulsory. Under a local opening edit, leave the theorem and proof in place unless a necessary substantive correction is separately identified.

## Introduce the results under their body numbers

### Shape the introduction around the question

The opening should draw the reader into an actual mathematical problem. A dated conjecture with named authors is one option when the history and attribution are supported. A concrete question, example, or unresolved phenomenon can do the same work. Do not mechanically start every paper with a year or add an invented anecdote. Explain how the starting point leads to the present question, why that question is still open, and what the paper contributes. The transition should expose a logical connection, not merely insert the word "naturally".

After the opening, a Background part gives the reader a useful picture of progress in the area: the relevant approaches, what they establish, and the obstacles that remain. Select literature to position this paper, rather than writing an exhaustive chronology or a list of names. Retain supplied citations; verify new historical claims or mark missing evidence rather than guessing. Keep the opening focused on the motivating problem and develop broader context here.

Then present the main results in a single Main results (or Main theorems) subsection, with the body numbering described below. Follow the order of the body sections: introduce the question and result of the first substantive section, explain the connection to the next, and continue in that order. Topic changes call for transitions, not separate main-results subsections or an automatic hierarchy of subsubsections. Supply the model and essential definitions before the statements; a dedicated model subsection between Background and Main results is appropriate when needed. Explain how the results answer the opening question, including what remains unresolved, and retain the worked calculation required by the author's profile.

Finish with a Lean formalisation subsection when there is formalisation to report. Distinguish the statements encoded, the results actually proved, and inputs accepted as hypotheses. Cite the supplied repository or revision and report build status, tool attribution and dependency details only when supported. A conditional implication checked in Lean is not an unconditional verification of the paper or its external inputs. Do not copy the exemplar's coverage, tooling or claims about axioms into a different manuscript. If the requested outline includes this subsection but its content is unavailable, flag the missing status separately; do not fabricate code or completion, and do not start a formalisation project merely to fill the outline.

Use this progression flexibly. Names and heading levels follow the actual document; Background is normally a subsection inside the Introduction, not necessarily a new top-level section. Combine or rearrange parts when that makes the argument clearer. A short passage or a light-edit request does not authorise adding the whole structure. Keep the opening as prose rather than requiring a subsection titled "Opening".

### Preserve the theorem numbering

Use the introduction to make the main results readable before their proofs. Set up the model and the required notation, state each selected main theorem with its body number, and explain what the statement settles. Do not replace its hypotheses with an appealing but stronger informal claim. Restate the actual result, not the proof; do not copy every technical lemma into the introduction.

For LaTeX, a non-counting restatement environment can refer forward to the body's label:

```latex
\newenvironment{restated}[2]{%
  \par\medskip\noindent\textbf{#1~\ref{#2}.}\itshape
}{\par\medskip}
% In the introduction, after the needed definitions:
\begin{restated}{Theorem}{thm:main}
  % The same mathematical statement as the body theorem.
\end{restated}
% Later in the body:
\begin{theorem}\label{thm:main}
  % The authoritative statement.
\end{theorem}
```

Use the correct result kind, including Corollary or Conjecture. Share statement text where practical; otherwise compare the two versions for assumptions, quantifiers, constants and claim status. Do not duplicate label definitions or advance the theorem counter in the introduction. Compile enough times to resolve forward references and inspect the resulting numbers. The example specifies a numbering mechanism, not a required theorem or a source of mathematical content.

Put a model figure near the relevant introduction passage. Explain what the vertices, edges, arrows or panels represent, especially if a construction uses directed replacement data but the studied process is undirected. Preserve source attribution where appropriate. A figure borrowed from an exemplar is suitable only when its model matches the new paper.

Organise long sections by their mathematical jobs, such as model and main statement, estimates, and completion of the proof. **Prefer at most three subsections per section and at least three typeset pages per subsection.** Three is not a required subsection count: zero, one, or two may be appropriate, and sections need not match. This current preference replaces the former five-subsection ceiling as the operative structural guidance.

For a substantive structural edit, inspect subsection boundaries and their lengths in the actual or intended manuscript layout. Merge genuinely connected short units and supply transitions, retaining assumptions, necessary proofs, labels and cross-references. If a section naturally fits a single coherent flow, it need not have subsections at all. A short opening, recall, model description, or Lean status note may belong in nearby prose instead of a separate heading; do not merge unrelated arguments simply to hit a page target.

The three-page preference is layout-dependent. When a compiled PDF and source are available, inspect the subsection's actual extent rather than counting touched pages as full pages. Without reliable pagination, report the length as unverified; do not convert pages into a universal word count. Do not change margins, font size, spacing, or float placement merely to manufacture three pages, and do not add redundant exposition or unsupported mathematics. Journal constraints, author-specified outlines, short paper formats, genuinely distinct arguments, and the editing contract can justify exceptions. Briefly explain a material exception rather than damaging the argument. A light edit or faithful translation preserves the supplied hierarchy unless structural change was authorised. Local proof steps can remain where useful, but a substitute maze of lower-level headings is not a solution.

## Keep a compact record of the claim

For a technical passage, track only the distinctions relevant to editing it:

| Feature | Questions that prevent silent changes |
|---|---|
| Objects | Finite approximant, combinatorial limit, completed metric space, or process on that space? |
| Assumptions | Which are standing, local, or needed only in a particular case? |
| Quantifiers | For each point or uniformly in all points? Almost everywhere or everywhere? What may a constant depend on? |
| Limits | Which variable tends to its limit, in what order and topology? Is convergence actually available? |
| Estimates | Equality, asymptotic ratio, two-sided comparison, upper bound, or numerical approximation? |
| Status | Definition, proved result, cited input, computation, conjecture, or interpretation? |

Keep this record small and internal unless the user requests a diagnostic. It must not become new notation in the paper.

## Recover an existing manuscript without losing its content

When the author names an older draft as the source, inspect it alongside the current version and agreed outline. Map the introduction, basic properties, definitions, arguments and examples to their intended destinations. A new outline is not permission to discard material that still fits it. Preserve author-selected prose, especially an introduction the author wants restored; repair only the inconsistencies required by the current claims. Explain substantive omissions briefly rather than silently dropping them.

Carry forward still-valid content, not superseded mathematics. Distinguish an old hypothesis removed by a new proof from one that remains necessary. When a classification or theorem changes, check its dependent abstract statements, introduction restatements, tables, examples and conclusions within the authorised scope. Make the needed consistency edits without turning a local request into a whole-paper rewrite. Keep sections explicitly excluded by the author unchanged and flag any dependency that cannot be resolved within that boundary.

For a shared Overleaf or Git manuscript, obtain the latest accessible source before editing and compare changes before publishing. Preserve concurrent author edits; reconcile a newer revision rather than overwriting it. Compile and inspect affected pages when suitable tools are available, then save through the requested channel and verify that the saved revision contains the edit. Local compilation, mathematical verification and successful remote saving are separate claims. This workflow applies when direct manuscript editing is requested; it does not require network access for an ordinary pasted-text revision or grant permission to publish elsewhere.

## Define observations before deriving a classification

Start with the observable: what is sampled, what is counted, and what asymptotic behaviour its exponent records. When relevant, specify the root or volume sampling, the randomness being averaged, conditioning, metric, normalisation, side of a transition, and order of limits. Use one common convention where it really applies, with explicit exceptions for different observations.

Define an exponent through that observable and prove its existence and expression separately. Do not insert the desired dimension formula as its definition and then advertise an equivalence as a discovery. If only some observables exist throughout the model class, explain that selection before defining a class from them; derive the smaller set of equivalent invariants afterwards. Do not claim that these are the only possible unconditional observables unless proved.

Keep nearby but different conclusions distinct: a cumulative tail and a point probability, a cell average and a pointwise estimate, an expected growth rate and an almost-sure dimension, a finite graph law and a metric scaling limit. An averaged or one-sided result can be valuable under its stated definition; changing the definition does not prove the original stronger claim. A proof outline remains a proof outline, and a missing local-limit or comparison argument remains a stated gap.

A compact opening table can orient the reader across observables and regimes. Its entries must agree with the precise definitions and statements below, including zero exponents, exceptions and sufficient versus necessary conditions. Keep the choice and number of quantities specific to the paper.

## Attribute overlap and distinguish an extension

When comparing a new manuscript with prior work, use the original theorem statements and relevant definitions, not the abstract or a familiar symbol alone. Match model assumptions, observables, conditioning, counting conventions and conclusion strength. An identical formula under a different sampling law may require a comparison lemma; equality of growth rates does not establish equality or similarity of the underlying matrices.

Separate direct reuse, a reformulation, a genuine extension and a remaining proof obligation. Give the exact theorem or equation citation where needed to identify a proof input. A concise comparison such as `Also see \cite{source}` need not have a result number when the author requests it and the relationship is clear; do not force detailed locators into every heading. Keep a necessary locator in the proof or nearby prose. Do not claim novelty merely from a new name, notation or packaging, and do not call something an extension from a special model if the cited work already treats the general case. Conversely, the absence of a result in one paper does not establish literature-wide priority.

For the author's own results, omit the optional descriptive title in `\begin{theorem}`, `\begin{lemma}`, `\begin{proposition}` and `\begin{corollary}`. Explain their role in the preceding prose. Optional result headings are for external attribution or an explicitly requested comparison or generalisation credit, not descriptive names. Verify the stated relationship; "Also see" does not mean "proved there in identical generality". Definitions omit descriptive optional headings as well, with attribution in the text. Preserve internal labels and introduction numbering when removing a descriptive heading.

Separate a historical physical observation from a new rigorous theorem, and a deterministic surrogate from a probabilistic model with a specified law. Numerical agreement, a calibrated approximation and a theorem relating the models have different evidential roles. Credit earlier insight even if its method differs from the present proof. When asking whether a claim is new, neither matching numbers nor different notation resolves the question. If a combined theorem contains both previously known and new conclusions with separate arguments, splitting it can make the contribution and attribution clear.

## Revise a proof by its dependencies

Find the endpoint and the indispensable intermediate steps. Keep assumptions and definitions available before they are used. Move explanatory prose where it prepares the difficult step, rather than collecting all explanation in a preamble.

Shorten a theorem around that endpoint. A progression of weaker conclusions followed by a stronger final conclusion should not be a running account of the proof inside the statement. Retain the final conclusion; if an intermediate result matters in its own right, state and prove it as a separate lemma. Keep a routine intermediate estimate in the proof. Check actual logical implication before removing a clause: convergence, a convergence rate and an effective algorithm are not interchangeable, and independent conclusions must remain available with their original hypotheses. Update references to extracted lemmas and keep the introduction's restatement aligned with the revised body theorem.

For a subsection that constructs a bound, distinguish the argument that the bound exists from the argument that a finite computation evaluates it. If these are separate mathematical tasks, an unnumbered local heading for each can make the progression clear. Continuity or monotonicity needed for existence must be proved there, or cited from an earlier result; a later finite formula cannot silently supply them. State each central conclusion as a theorem when warranted and put its proof next to the statement. In the body the usual order is prerequisites, theorem, proof, worked example. The introduction's numbered restatements remain the explicit overview exception.

A useful proof opening can identify the reduction or the estimate that remains. For a two-sided bound, state which construction gives each direction; check inclusion, monotonicity and inequality directions. For an existence-and-uniqueness result, ensure the argument actually establishes both. For a statement about all scales, ensure constants do not accidentally depend on the scale.

For a short geometric or constructive lemma, the reader may understand the statement more readily after performing its operations. Give only the setup needed to start, then develop the complete argument in a few meaningful steps. State the lemma immediately afterwards as the formal conclusion, explicitly referring to the preceding derivation as its proof. Keep the destination clear in the opening without duplicating the full statement. This is a local alternative to theorem-then-proof, not a reason to postpone every main result or replace a proof with pictures. Do not repeat the same calculation after the concluding lemma. If the preceding discussion is only illustrative, it cannot serve as the proof; retain a complete argument. See [proof-figures.md](proof-figures.md) for pairing steps with mathematical figures.

If a step is immediate from a displayed identity and a cited lemma, a short sentence is enough. If a step uses a nontrivial covering, flow construction, compactness argument, or passage to a limit, retain the mechanism that makes it valid. Replacing it with “standard” is not an improvement.

Do not infer convergence from boundedness or comparability alone. Do not interchange a nonlinear function and expectation without justification. Do not turn bounds on each point into uniform bounds by removing a dependency. These are local editing checks, not a substitute for a full mathematical review.

If a structural revision crosses several results, compare both the theorem statements and the uses of those theorems. Preserve labels where possible. Do not create auxiliary lemmas solely to make the workflow look systematic.

## Use definitions and examples to reduce the reader's work

Explain the role of a new object near its definition. An interpretation should identify what it measures or makes possible, not translate every symbol back into words. Use a familiar object when it is genuinely the same one; separate objects that share notation but differ mathematically.

Give the main model a numbered Definition after its underlying space or construction has been introduced. Auxiliary models need their own precise definition before their first use when changed dynamics, source conventions or boundary rules matter to the argument. Use `:=` for symbolic definitions; a condition such as `f(x)=a` remains an equality even when it uniquely characterises a root. Do not mistake a proved formula for a definition or introduce dispensable notation to satisfy a typographical rule.

Definitions belong outside theorem, lemma and proposition statements. Move a phrase such as “put” or “define” and its assignment into the preceding setup; use a separate Definition environment if the object is important. Make any needed parameter hypotheses available in that setup. A root or limit must be justified before it is used as a defined object, unless its existence is the conclusion currently being proved; do not conceal a forward dependency by moving the defining formula earlier. A theorem may still quantify objects and assert existence and uniqueness without embedding a new definition.

Prefer the smallest example that performs a needed job. A counterexample may explain why a tempting shortcut fails. A worked construction may show how an abstract definition is evaluated. A numerical check illustrates behaviour under the reported conditions; it does not prove the general theorem.

When one result mixes an object's construction, a main conclusion and several equivalent hypotheses, consider separating them: define the object first; illustrate it immediately if its construction is hard to read; state the theorem with its necessary hypotheses and central conclusion; and collect the equivalent criteria in a proposition. Order these parts by dependency rather than imposing this sequence on every paper. For a cyclic equivalence proof, make each implication explicit, for example `(1) implies (2)`, `(2) implies (3)`, and `(3) implies (1)`, with an actual argument for each link. Keep all necessary assumptions; a concise statement is not a weaker specification.

After the main theorem, work through a concrete admissible instance: specify the object and parameters, compute the theorem's inputs, carry out the resulting finite calculation, and explain the output. For a critical-density representation, for example, evaluate a finite-cell probability and its root, identifying that root as a bound if the theorem says it is a bound. Verify algebra and any numerical values; do not present a finite approximation as the limiting answer. A compact calculation after an introduction restatement may point to the full example after the body theorem. This author preference does not require new examples after every technical lemma, and it does not override an explicit light-edit contract.

Preserve an example already doing this work. Do not insert a favourite graph, metaphor or counterexample from the exemplar papers into unrelated science.

Spend explanation on the example where the reader learns to construct the object. If its matrix and spectral radius have already been obtained, a later application of the dimension formula may be a single sentence citing the theorem. This fulfils the worked-calculation preference without repeating the construction. Do not shorten the first calculation into an unexplained matrix or numerical answer.

An appendix consisting of a directly relevant calculation can instead become an example beside the general theorem it illustrates. Share the theorem counter with examples and preserve stable labels when moving them. Keep the theorem's general hypotheses separate from the example's special geometry; placing a special case in the body must not silently narrow the surrounding result.

## End a section with what has changed

When a result supplies the next section's input, explain that dependency concretely. When it settles only part of the motivating question, say which part. Keep the unresolved extension visibly unresolved.

Conditional formal verification remains conditional: distinguish encoded statements, assumed external inputs, and conclusions derived from them. Do not convert a manuscript's report of verification into an independent verification claim by the editor.

For a final Discussion, explain what the results change in the physical or mathematical picture before listing future directions. Distinguish failure of sufficiency from failure of necessity, an obstruction to one family of classifiers from the impossibility of any classification, and a property of a single model from a counterexample involving a pair. Do not turn a suggestive name into a stronger physical claim: incompatible discrete rescaling factors, for example, do not by themselves negate scale invariance.

Formulate a few concrete open problems about what the present invariants fail to detect or what additional observations might distinguish. Keep them recognisably open, and do not invent technical conjectures for rhetorical effect. An author-supplied final sentence expressing belief in a deeper classification or understanding can retain its personal tone; mark it as belief rather than an established conclusion. Avoid replacing it with a generic recap or promising an unsupported solution.

## Empirical-science extension

The two-paper corpus does not establish a field-specific voice for experimental research. Apply the same editorial logic with observation -> supported inference -> limitation. Preserve sample sizes, units, controls and uncertainty. Do not upgrade an association to a causal explanation or a finite experiment to a universal result. These are editorial safeguards, not observations about the author's experimental practice.
