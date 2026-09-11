# Worked editing examples

All examples below were constructed for this skill. They are not quotations from the exemplar papers and do not describe new results by their author. Use the decisions they demonstrate, not their wording as a reusable template.

## 1. Rebuild a generic introduction around supplied facts

**Task:** Substantively revise an introduction for specialists. Supplied facts: earlier estimates apply to bounded-degree graphs; the current graph family can have unbounded degrees; the manuscript proves uniform exit-time scaling by combining local mass and resistance estimates. No diffusion-limit theorem is supplied.

**Draft**

> Fractal graphs are an exciting and rapidly evolving area with far-reaching implications. Our powerful framework offers a comprehensive solution to the challenges of diffusion. We study exit times. Previous estimates assume bounded degree, which our graphs need not have. We combine local mass estimates with local resistance estimates to obtain uniform exit-time scaling.

**Revision**

> Existing exit-time estimates assume bounded vertex degree. The graphs considered here need not satisfy this assumption, so those estimates do not apply directly. We obtain uniform exit-time scaling by combining local mass estimates with local resistance estimates.

**Decision:** Put the actual obstacle before the method. Remove the unsupported claim to solve diffusion. Do not invent a more detailed mechanism or assert a diffusion theorem.

## 2. Keep the argument visible without abbreviating its ingredients

**Task:** Improve the exposition. Assume positive sequences satisfy

\[
c_1\lambda^n\leq a_n\leq C_1\lambda^n,
\qquad
c_2\mu^n\leq b_n\leq C_2\mu^n,
\]

where all four constants are positive and independent of \(n\), \(\lambda>0\), and \(\mu>1\).

**Draft**

> We employ a sophisticated asymptotic analysis. The logarithmic ratio converges to \(\log\lambda/\log\mu\). This follows from the bounds.

**Revision**

> Taking logarithms in the two bounds gives
> \[
> \log a_n=n\log\lambda+O(1),
> \qquad
> \log b_n=n\log\mu+O(1),
> \]
> where both error terms are bounded independently of \(n\). Since \(\mu>1\), division and passage to the limit yield
> \[
> \lim_{n\to\infty}\frac{\log a_n}{\log b_n}
> =\frac{\log\lambda}{\log\mu}.
> \]

**Decision:** Show the actual reason for the limit, including the denominator condition. No extra aliases are needed. This argument also accommodates \(\lambda\leq1\); avoid a quotient-bound argument that silently assumes positive numerators.

## 3. Preserve pointwise qualifications

**Draft**

> For \(\mu\)-almost every \(x\), there exist \(C(x)>0\) and \(t_0(x)>0\) such that \(p_t(x,x)\leq C(x)t^{-\alpha}\) for \(0<t<t_0(x)\). This proves the same uniform estimate everywhere.

**Revision**

> For \(\mu\)-almost every \(x\), there exist \(C(x)>0\) and \(t_0(x)>0\) such that
> \[
> p_t(x,x)\leq C(x)t^{-\alpha},\qquad 0<t<t_0(x).
> \]
> The estimate is pointwise, with constants and a time threshold that may depend on \(x\).

**Separate note:** The last sentence was corrected: the stated bound neither covers every point nor provides constants uniform in \(x\).

## 4. Do not polish away a proof gap

**Draft**

> Since \(2\leq u_n/v_n\leq3\) for every \(n\), the ratio converges. This immediately completes the proof.

**Revision**

> The bounds \(2\leq u_n/v_n\leq3\) show that the ratio is bounded, but they do not establish convergence.

**Separate note:** A further argument is needed. The sequence \(u_n/v_n=5/2+(-1)^n/2\) satisfies these bounds and does not converge. The claimed proof is therefore incomplete from the information given.

## 5. Respect a light-edit request

**Task:** Grammar only; preserve the order and voice.

**Draft**

> We first give the example, since the definition is easier to understand after it. The two path has different lengths. This is the reason that we keep both colours.

**Revision**

> We first give the example, since the definition is easier to understand after it. The two paths have different lengths. This is why we keep both colours.

**Decision:** Do not apply the default structural revision when the author requested grammar only.

## 6. Allow already good prose to remain

**Task:** Improve this proof if needed. The inequalities \(f_n\leq g_n\leq h_n\), the limits \(f_n\to L\) and \(h_n\to L\), and the squeeze theorem are available.

**Draft and revision**

> Since \(f_n\leq g_n\leq h_n\) and both outer sequences converge to \(L\), the squeeze theorem gives \(g_n\to L\).

**Decision:** No added roadmap, lemma, notation or paragraph is needed.
