# Language and rhythm

The goal is recognisable, direct scientific reasoning. The recommendations below combine author-informed choices with editorial design; they are not a statistical fingerprint of human prose.

## Prefer sentences that do a job

- Give a sentence a concrete subject: the estimate, construction, assumption, example, or author performing a specific operation.
- Use verbs that state the operation: define, bound, compare, construct, imply, fail, depend on. Avoid adding strength unsupported by the source.
- Let “because”, “hence”, “however” and similar connectors express an actual logical relation. If that relation is missing, repair or flag it instead of merely adding a connector.
- Replace vague pronouns when the antecedent could be either an object, an estimate, or an entire argument.
- Retain the same technical term for the same object. Variation for its own sake can create a false distinction.

An equation can be the grammatical continuation of a sentence. Use punctuation accordingly. Explain a new equation's role or a surprising cancellation when that interpretation helps; do not add a verbal duplicate to every display.

## Calibrate density

Put detail at the point of difficulty. A delicate construction may need a substantial paragraph and several equations. An immediate consequence may need one sentence. Sentence length, paragraph length and proof length should vary with the logical work.

Use short transitions to orient the reader after a long derivation. Prefer a specific remaining task over a repeated announcement that the next step is important. Do not add a summary at every paragraph boundary.

Headings and lists help with genuine cases, distinct hypotheses, or comparable regimes. Do not break a continuous proof into a checklist merely because the editor used a checklist internally.

## Preserve conviction without promotion

Keep justified statements definite. A theorem need not become tentative because the prose is modest. Conversely, numerical evidence and a conjectured extension need their original status.

Preserve an intentional contrast that explains a mathematical difference, an unexpected outcome, or an author's position. Do not manufacture a dramatic contrast where none is needed. Descriptive analogies are optional and must make the mechanism easier to understand.

Delete promotional wording when it contributes no scientific information. Do not infer an absolute word ban from a single awkward sentence: a word such as “novel” or “robust” can be appropriate when a concrete novelty or robustness claim is supported. Never insert a claim simply to replace the adjective with a longer justification.

## Control notation without erasing it

Before introducing a symbol, ask whether it represents a necessary mathematical object or merely shortens an expression. A short expression with no fraction and only a few letters or operations should be written directly. Do not use a new symbol just to abbreviate `\lambda p`, `1-p`, or a similarly small expression, even if it occurs repeatedly. This is a global preference for statements, exposition and proofs, not merely a restriction on one-use aliases.

Minimise intermediate variables in proofs. Prefer showing the calculation with its original quantities over assignments whose only purpose is to carry a short intermediate expression to the next line. Review existing aliases as well as new ones. Retain a parameter varied independently, a bound variable, or a constructed object when its mathematical role requires notation; do not erase that role simply because one formula for it is short. Conversely, having a fraction or a long formula is not by itself a reason to introduce a name.

When simplifying notation, compare every use and dependency. In particular, a constant may depend on a point while remaining independent of the scale. Cosmetic renaming must not conceal this difference.

## Use display style for limits

Every limit operator (`\lim`, `\liminf`, or `\limsup`) should be typeset in display style. Add `\displaystyle` to an inline formula containing a limit; displayed equations already have the appropriate style. This is a typographic rule, not a requirement that every limit appear on its own line. Keep a short limit within its sentence when that reads naturally, and use a separate display only when the formula or argument benefits. Preserve all conditions, punctuation and convergence qualifications.

## Display formulas without boxes

Never use `\boxed{...}` to display a manuscript formula. Do not use a substitute frame to emphasise it: avoid `\fbox{...}`, `\framebox{...}`, and framed or coloured equation containers. Use ordinary display math, `equation`, or `align` as appropriate. Make the formula's importance clear through its placement and the surrounding explanation.

Apply this rule to inherited formulas and restated theorems as well as newly written text. When asked to remove boxes from a paper, check the whole manuscript. When editing existing boxed mathematics, remove only the presentational wrapper. Preserve grouping, mathematical content, numbering, labels and cross-references; repair the surrounding math environment if the wrapper supplied it. Do not indiscriminately delete commands containing "box": a box operator used as mathematical notation and the QED marker are not equation frames.

## Translate meaning and register

Preserve the author's intended emphasis and logical progression. Translate mixed-language working notes into the requested target language while retaining technical meaning. Correct accidental repetition, spelling and syntax; do not manufacture errors to create personality.

Use idiomatic English rather than word-for-word Chinese syntax, but do not add institutional praise, new motivation, or a more deferential persona. Follow the existing manuscript's spelling and house style. For a new English draft without guidance, British spelling is a tentative default.
