# Argument and proof decisions

Use this reference for substantive revision. The current assignment controls how far the editor may change an existing draft.

## Build a reason for the next step

In an introduction, distinguish the broad subject from the specific research problem. Explain what an existing approach already achieves and which obstacle it leaves. State the contribution at the level supported by the manuscript. A classical construction may be useful in a new general setting without being a newly invented idea.

When the source supports it, organise the exposition around a progression such as:

> existing result -> remaining obstruction -> construction or estimate that resolves it -> resulting statement -> use or unresolved extension

This is a relationship between ideas, not a mandatory section order. An introduction can give an informal construction and restate a main result before the body develops the technical details. In the body, follow the author's preference for stating the theorem only once its prerequisites are available and then proving it immediately. A short result does not need a miniature literature review.

The explanation of a hypothesis should say what breaks without it. If the supplied argument does not establish necessity, describe where the hypothesis is used instead of calling it necessary. Separate convenience of presentation from mathematical necessity.

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

Organise long sections by their mathematical jobs, such as model and main statement, estimates, and completion of the proof. The number of subsections follows the argument: zero, one, two, or more may be appropriate. Three is neither a target nor a minimum, and different sections need not have matching counts. Keep the author's absolute ceiling of five. Merge genuinely connected parts and write the transitions that the old headings were replacing. A small number of local proof steps may still be useful; a long substitute hierarchy is not a solution.

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

## Revise a proof by its dependencies

Find the endpoint and the indispensable intermediate steps. Keep assumptions and definitions available before they are used. Move explanatory prose where it prepares the difficult step, rather than collecting all explanation in a preamble.

Shorten a theorem around that endpoint. A progression of weaker conclusions followed by a stronger final conclusion should not be a running account of the proof inside the statement. Retain the final conclusion; if an intermediate result matters in its own right, state and prove it as a separate lemma. Keep a routine intermediate estimate in the proof. Check actual logical implication before removing a clause: convergence, a convergence rate and an effective algorithm are not interchangeable, and independent conclusions must remain available with their original hypotheses. Update references to extracted lemmas and keep the introduction's restatement aligned with the revised body theorem.

For a subsection that constructs a bound, distinguish the argument that the bound exists from the argument that a finite computation evaluates it. If these are separate mathematical tasks, an unnumbered local heading for each can make the progression clear. Continuity or monotonicity needed for existence must be proved there, or cited from an earlier result; a later finite formula cannot silently supply them. State each central conclusion as a theorem when warranted and put its proof next to the statement. In the body the usual order is prerequisites, theorem, proof, worked example. The introduction's numbered restatements remain the explicit overview exception.

A useful proof opening can identify the reduction or the estimate that remains. For a two-sided bound, state which construction gives each direction; check inclusion, monotonicity and inequality directions. For an existence-and-uniqueness result, ensure the argument actually establishes both. For a statement about all scales, ensure constants do not accidentally depend on the scale.

If a step is immediate from a displayed identity and a cited lemma, a short sentence is enough. If a step uses a nontrivial covering, flow construction, compactness argument, or passage to a limit, retain the mechanism that makes it valid. Replacing it with “standard” is not an improvement.

Do not infer convergence from boundedness or comparability alone. Do not interchange a nonlinear function and expectation without justification. Do not turn bounds on each point into uniform bounds by removing a dependency. These are local editing checks, not a substitute for a full mathematical review.

If a structural revision crosses several results, compare both the theorem statements and the uses of those theorems. Preserve labels where possible. Do not create auxiliary lemmas solely to make the workflow look systematic.

## Use definitions and examples to reduce the reader's work

Explain the role of a new object near its definition. An interpretation should identify what it measures or makes possible, not translate every symbol back into words. Use a familiar object when it is genuinely the same one; separate objects that share notation but differ mathematically.

Give the main model a numbered Definition after its underlying space or construction has been introduced. Auxiliary models need their own precise definition before their first use when changed dynamics, source conventions or boundary rules matter to the argument. Use `:=` for symbolic definitions; a condition such as `f(x)=a` remains an equality even when it uniquely characterises a root. Do not mistake a proved formula for a definition or introduce dispensable notation to satisfy a typographical rule.

Definitions belong outside theorem, lemma and proposition statements. Move a phrase such as “put” or “define” and its assignment into the preceding setup; use a separate Definition environment if the object is important. Make any needed parameter hypotheses available in that setup. A root or limit must be justified before it is used as a defined object, unless its existence is the conclusion currently being proved; do not conceal a forward dependency by moving the defining formula earlier. A theorem may still quantify objects and assert existence and uniqueness without embedding a new definition.

Prefer the smallest example that performs a needed job. A counterexample may explain why a tempting shortcut fails. A worked construction may show how an abstract definition is evaluated. A numerical check illustrates behaviour under the reported conditions; it does not prove the general theorem.

After the main theorem, work through a concrete admissible instance: specify the object and parameters, compute the theorem's inputs, carry out the resulting finite calculation, and explain the output. For a critical-density representation, for example, evaluate a finite-cell probability and its root, identifying that root as a bound if the theorem says it is a bound. Verify algebra and any numerical values; do not present a finite approximation as the limiting answer. A compact calculation after an introduction restatement may point to the full example after the body theorem. This author preference does not require new examples after every technical lemma, and it does not override an explicit light-edit contract.

Preserve an example already doing this work. Do not insert a favourite graph, metaphor or counterexample from the exemplar papers into unrelated science.

An appendix consisting of a directly relevant calculation can instead become an example beside the general theorem it illustrates. Share the theorem counter with examples and preserve stable labels when moving them. Keep the theorem's general hypotheses separate from the example's special geometry; placing a special case in the body must not silently narrow the surrounding result.

## End a section with what has changed

When a result supplies the next section's input, explain that dependency concretely. When it settles only part of the motivating question, say which part. Keep the unresolved extension visibly unresolved.

Conditional formal verification remains conditional: distinguish encoded statements, assumed external inputs, and conclusions derived from them. Do not convert a manuscript's report of verification into an independent verification claim by the editor.

## Empirical-science extension

The two-paper corpus does not establish a field-specific voice for experimental research. Apply the same editorial logic with observation -> supported inference -> limitation. Preserve sample sizes, units, controls and uncertainty. Do not upgrade an association to a causal explanation or a finite experiment to a universal result. These are editorial safeguards, not observations about the author's experimental practice.
