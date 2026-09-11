# Behavioural evaluation

The [eight cases](cases.json) are original synthetic inputs. They test scientific fidelity, editing scope, and whether the workflow makes a useful revision. They are not extracts from the source papers.

## Run a fresh evaluation

Give the editor the skill and a case's `task` and `input`. Do not show it `criteria`, `initial-outputs.json`, or earlier assessment conclusions. Let it read the skill's relevant references as it normally would. Record the model, settings, date, complete output, and any tools actually used.

Assess the result against that case's criteria. A different valid wording is acceptable. Do not grade by exact sentence matching or by whether stage names appear in the response.

## Rubric

Score each applicable dimension from 0 to 2: 0 fails, 1 partly satisfies, 2 satisfies.

| Dimension | What to examine |
|---|---|
| Scientific fidelity | Hypotheses, quantifiers, dependencies, claim status and numerical facts survive. |
| Argument | The revised progression is justified, and an invalid implication is not concealed. |
| Voice | The language is direct and informative without becoming uniformly terse or bland. |
| Scope | The chosen depth follows the request; good passages need not change. |
| Delivery | Usable revised text comes first, with necessary substantive notes outside it. |

A silent change of a theorem, invented evidence, an unflagged invalid inference, or a false claim of verification is a critical failure regardless of the total score. A natural-language checklist cannot establish mathematical correctness by itself.

For author similarity, collect fresh drafts and the author's preferences between blinded revisions. Keep that evaluation separate from these fidelity cases. Include an unmodified-model comparison before claiming an improvement caused by the skill.

## Initial record

[initial-outputs.json](initial-outputs.json) records one development pass by the same assistant that authored the skill. [initial-review.md](initial-review.md) describes its scope. These outputs are examples of observed development behaviour, not independent test evidence or expected strings to memorise.
