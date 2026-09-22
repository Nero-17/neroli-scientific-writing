# Geometric derivations and proof figures

Use this reference when substantively revising a geometric argument or its mathematical figures. Follow an explicit light-edit or faithful-translation contract. The aim is to make the operations visible while preserving the proof's full scope.

## Start with the operations

Recover the author's plain-language explanation before choosing the layout. Identify what is decomposed, what transformation is applied, what remains invariant, and what new relation results. These questions help find the steps; they are not four required headings. For a self-similar construction, decomposition, normalisation and reading the transformed parameters may be the natural progression. Another argument may need fewer or different steps.

Keep the section opening to the objects, notation, coordinate convention and assumptions needed for the first step. Integrate short formulas into explanatory sentences, and defer later machinery until its first use. A request for roughly half a page of setup applies to that passage; do not impose it across manuscripts or remove a necessary definition to meet it. Give central identities and derivations room in display math, without displaying each elementary assignment separately.

Write a short explanation of each operation, then place its figure immediately after it or as close as the final pagination permits. Separate figures are useful when a single image asks the reader to follow several different operations at once. Keep panel identities consistent across the sequence. End with a concise lemma when it formally collects a complete derivation just given, and explicitly identify that derivation as its proof. Do not repeat the proof or present an unproved general statement as a summary.

## Make each figure answer a mathematical question

Choose the figure from the step's task: which pieces interact, which map identifies two problems, or how a displacement is composed. A decomposition diagram should distinguish the relevant pairings; a transformation diagram should track the same objects or point; a displacement diagram should show where the vectors start and end. Retain required empty cases rather than suggesting every candidate pair intersects.

Let the surrounding prose explain the operation. Inside the figure, prefer object labels, parameter symbols, map labels and a small number of necessary numerical values. Move sentence-length explanations into the text or caption. A caption can identify the chosen parameters, finite approximation and panel convention; it should not repeat the entire proof. Minimal text still needs unambiguous symbols and legible labels at the final printed size.

Ask what the reader learns from each figure beyond the nearby text or another figure. Delete or replace a redundant figure instead of decorating it or preserving its number. Repair the affected references. The number of figures follows the operations and the user's request, not a preferred count.

## Keep coordinate and vector meaning visible

- Add axes, an origin and a few useful ticks when position, translation or scaling is part of the argument. Omit a dense grid or unnecessary ticks that obscure the construction.
- Keep the coordinate convention and unit scale consistent across comparable panels. If the frame or scale changes, label the map and make the change explicit. Independently resizing every object to fill its panel can conceal the dilation being proved.
- Use vector-arrow notation for geometric position and displacement vectors, consistently with the text. Distinguish a displacement arrow from an arrow between panels denoting a map.
- Anchor displacement arrows to their actual endpoints. Arrange a vector sum head to tail when that demonstrates the identity, and verify its signs in the manuscript's translation convention. Preserve consistent colours for the same objects across steps.
- When arrows alone lose their geometric meaning, retain the parent objects as a faint background and show selected pieces more strongly. The context should locate the vectors without competing with them. Choose opacity by inspecting the rendered figure; there is no universal numerical opacity.

Show each object claimed to be drawn in full within the intended scene; do not omit half of a comparison object merely because its intersection is the focus. If a finite window, clipping or approximation is intentional, identify it. Distinguish a missing object from an empty intersection.

## From a geometric example to a table and matrix

When a matrix encodes geometry, let the reader reconstruct it: show the configuration, record the transitions in a table, and count them into the matrix. Place the table and matrix side by side when legible. Use the same state order, colours and labels across all three representations.

Define what the row and column states represent and identify the direction explicitly, for example rows as sources and columns as targets. Explain what belongs in a cell: branch labels, successor states, weights or multiplicities are different objects. If a matrix entry counts labels, state that it is the cardinality of the cell's label set; an empty set gives a zero entry. Different labels reaching the same target still contribute separately under that convention. Do not assume a reader will infer these rules from braces or a slash in the heading.

In an aggregated state, the represented geometric object may be a union of several sets. Show that union explicitly in the introductory figure rather than relying on an undefined set-of-parameters shorthand. Define the transition rule before using its table. A one-step matrix requires a state description sufficient to determine the next transition; do not silently replace it with a multi-step rule, assume closure, or treat a visually plausible table as proof that the states are valid. Flag unresolved mathematical dependencies instead of resolving them cosmetically.

## Lattice inclusion figures

For a lattice contained in a finer lattice, show their points in the same coordinate frame and scale. Where their grid relation matters, overlay the coarse grid and the fine grid, with distinguishable line weights and point markers. Make clear that inclusion concerns lattice points; the connecting segments need not coincide. A displayed finite window illustrates the relation, while exact basis identities or the surrounding argument establish it for the infinite lattices. State the example's parameters and reference the figure at the relevant condition of the proposition.

## Check the drawing against the derivation

Generate exact constructions from their coordinates or maps using maintainable vector or plotting sources where practical. Check the image against the algebra: domains, pair indices, centres, translation signs, dilation factors, transformed points and any inverse map used to recover the original intersection. A sketch of one parameter choice or a finite approximation must be labelled accordingly; its appearance cannot establish a universal statement or an exact limiting set.

Inspect the rendered manuscript at its intended reading size, including the placement of each explanation and figure. Check clipping, overlapping labels, arrowheads, faint context and the consistency of text, captions and assets. Do not claim a visual inspection or successful compilation when only source files were examined.

Check page flow as well: avoid unexplained blank areas created by oversized floats or unnecessary forced placement, keep each explanation near its figure, and verify numbering and references after moving or deleting material. A figure that is clear as a standalone image must still be readable at its actual manuscript size.
