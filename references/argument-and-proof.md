# Argument and proof decisions

Use this reference for substantive revision. The current assignment controls how far the editor may change an existing draft.

## Build a reason for the next step

In an introduction, distinguish the broad subject from the specific research problem. Explain what an existing approach already achieves and which obstacle it leaves. State the contribution at the level supported by the manuscript. A classical construction may be useful in a new general setting without being a newly invented idea.

When the source supports it, organise the exposition around a progression such as:

> existing result -> remaining obstruction -> construction or estimate that resolves it -> resulting statement -> use or unresolved extension

This is a relationship between ideas, not a mandatory section order. A reader may need an informal construction and an early theorem statement before the technical definitions. Preserve that arrangement if it works. A short result does not need a miniature literature review.

The explanation of a hypothesis should say what breaks without it. If the supplied argument does not establish necessity, describe where the hypothesis is used instead of calling it necessary. Separate convenience of presentation from mathematical necessity.

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

A useful proof opening can identify the reduction or the estimate that remains. For a two-sided bound, state which construction gives each direction; check inclusion, monotonicity and inequality directions. For an existence-and-uniqueness result, ensure the argument actually establishes both. For a statement about all scales, ensure constants do not accidentally depend on the scale.

If a step is immediate from a displayed identity and a cited lemma, a short sentence is enough. If a step uses a nontrivial covering, flow construction, compactness argument, or passage to a limit, retain the mechanism that makes it valid. Replacing it with “standard” is not an improvement.

Do not infer convergence from boundedness or comparability alone. Do not interchange a nonlinear function and expectation without justification. Do not turn bounds on each point into uniform bounds by removing a dependency. These are local editing checks, not a substitute for a full mathematical review.

If a structural revision crosses several results, compare both the theorem statements and the uses of those theorems. Preserve labels where possible. Do not create auxiliary lemmas solely to make the workflow look systematic.

## Use definitions and examples to reduce the reader's work

Explain the role of a new object near its definition. An interpretation should identify what it measures or makes possible, not translate every symbol back into words. Use a familiar object when it is genuinely the same one; separate objects that share notation but differ mathematically.

Prefer the smallest example that performs a needed job. A counterexample may explain why a tempting shortcut fails. A worked construction may show how an abstract definition is evaluated. A numerical check illustrates behaviour under the reported conditions; it does not prove the general theorem.

Preserve an example already doing this work. Do not insert a favourite graph, metaphor or counterexample from the exemplar papers into unrelated science.

## End a section with what has changed

When a result supplies the next section's input, explain that dependency concretely. When it settles only part of the motivating question, say which part. Keep the unresolved extension visibly unresolved.

Conditional formal verification remains conditional: distinguish encoded statements, assumed external inputs, and conclusions derived from them. Do not convert a manuscript's report of verification into an independent verification claim by the editor.

## Empirical-science extension

The two-paper corpus does not establish a field-specific voice for experimental research. Apply the same editorial logic with observation -> supported inference -> limitation. Preserve sample sizes, units, controls and uncertainty. Do not upgrade an association to a causal explanation or a finite experiment to a universal result. These are editorial safeguards, not observations about the author's experimental practice.
