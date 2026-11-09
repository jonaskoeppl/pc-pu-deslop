# Nonuniqueness for Bernoulli percolation on nonamenable quasi-transitive graphs: towards a deslopped cleaned-up version

The goal of this project is to create an **human-readable version** of the recent
machine-generated manuscript:

> *Nonuniqueness of percolation on nonamenable quasi-transitive graphs*
> (credited to "OpenAI", dated 24 September 2026), referred to below as **[AI]**.

Additionally, it would be nice to also obtain a lean verification of the proof. 

The manuscript claims a proof of the Benjamini–Schramm conjecture
`p_c < p_u` for Bernoulli **bond** percolation on every nonamenable
quasi-transitive graph. It also claims Hutchcroft's stronger
operator-threshold conjecture `p_c < p_{2→2}`, which gives mean-field
criticality as a consequence.

The goal here is not to add new mathematics. It is to produce a version
of the argument that a percolation theorist can **read, check, and cite
responsibly**.

---

## ⚠️ Status

- **Not peer reviewed.** The source manuscript was produced by an AI system.
  Nothing in this repository should be read as an endorsement of
  its correctness.
- The edited text tracks the logic of [AI] as faithfully as possible. Where a
  step is unclear, under-justified, or appears to fail, we **flag it**
  rather than silently repair it. See `review/` and the issue tracker.
- If you find a gap or an error, please open an issue (see *Contributing*).

| Section of [AI] | Edited | Checked by ≥1 reader | Open issues |
|---|---|---|---|
| §1 Introduction | ☐ | ☐ | – |
| §2 Preliminaries and unimodular reduction | ☐ | ☐ | – |
| §3 Good critical clusters | ☐ | ☐ | – |
| §4 Amplifying local endpoint maps | ☐ | ☐ | – |
| §5 Critical moments and susceptibility | ☐ | ☐ | – |
| §6 Subpower triangle bound | ☐ | ☐ | – |
| §7 Corridor deformation | ☐ | ☐ | – |
| §8 Paths with endpoint escapes | ☐ | ☐ | – |
| §9 Critical boundedness, nonuniqueness interval | ☐ | ☐ | – |
| §10 Consequences | ☐ | ☐ | – |

---

## The claimed results

Let `G = (V,E)` be an infinite, connected, locally finite, quasi-transitive
graph with positive vertex-isoperimetric constant `h_V(G) > 0`.
Let `T_p(x,y) = P_p(x ↔ y)` act on counting-measure `ℓ²(V)`, and let

    p_{2→2}(G) = sup{ p : T_p is bounded on ℓ²(V) }.

**Theorem 1.1 of [AI] (claimed).**

    sup_{p<p_c} ‖T_p‖_{2→2} = ‖T_{p_c}‖_{2→2} < ∞,     p_c < p_{2→2} ≤ p_u.

Moreover, there are `p_c < p_1 < p_2 < 1` such that, in the standard
monotone coupling, almost surely there are infinitely many infinite
clusters simultaneously for every `p ∈ [p_1, p_2]`.

**Corollary 1.2 (claimed).** The same holds for every Cayley graph of a
nonamenable finitely generated group, for an *arbitrary* finite symmetric
generating set.

**Corollary 1.3 (claimed).** The triangle condition `∇_{p_c} < ∞` holds,
together with the mean-field laws:

- `χ(p) ≍ (p_c − p)^{-1}`
- `θ(p) ≍ p − p_c`
- `P_{p_c}(|C| ≥ n) ≍ n^{-1/2}`
- intrinsic and extrinsic critical radius tails `≍ n^{-1}`

It also gives `p_c < p_{2→2} ≤ p_exp`, so connection probabilities decay
exponentially throughout a nonempty supercritical interval.

## Background

- **Benjamini–Schramm (1996):** a connected, locally finite,
  quasi-transitive graph has `p_c < p_u` if and only if it is
  nonamenable. The amenable ("only if") direction is classical
  (Burton–Keane; Gandolfi–Keane–Newman).
- **Hutchcroft, *Percolation on hyperbolic graphs* (GAFA 2019),
  denoted [H19]:**
  - introduces the operator threshold `p_{2→2}`;
  - shows `p_c ≤ p_{2→2} ≤ p_u` and `∇_p < ∞` for all `p < p_{2→2}`;
  - proves `p_c < p_{2→2}` for nonamenable Gromov-hyperbolic
    quasi-transitive graphs;
  - proves `p_c < p_{2→2}` for graphs with a quasi-transitive
    nonunimodular automorphism subgroup (Theorem 2.9);
  - conjectures `p_c < p_{q→q}` for all `q ∈ (1,∞)` and all nonamenable
    quasi-transitive graphs (Conjecture 6.1). This is equivalent to
    `p_c < p_{2→2}`.
- [H19] reduces the problem to the unimodular case. Its hyperbolic proof
  checks two conditions:
  - a linear susceptibility bound `limsup (p_c − p) χ_p < ∞`;
  - an "isoperimetric" condition on `T_p`.

  It does this using hyperbolic geometry, including the Bonk–Schramm
  embedding and a hyperbolic Magic Lemma. [AI] claims to replace the
  geometric input with arguments that use only nonamenability.

## Architecture of the argument in [AI]

```
§2  reductions ── simple graphs (subdivision, Lemma 2.1)
     │           └ nonunimodular case ← [H19, Thm 2.9]   (Prop. 2.5)
     │           sharpness, BK/Harris, Russo, sprinkling [H19, Lemma 2.4]
     ▼
§3  "good" critical clusters: bridge counts stay controlled after
     arbitrary deletions, outside a stretched-exponentially small event
     ▼
§4  local endpoint maps: if E|C|^α = ∞ for some α<1/2, build maps
     whose endpoint kernel becomes dispersive (small ℓ² norm) much
     faster than their success probability or cap degrades
     ▼
§5  ⇒ sup_x E_{p_c}|C_x|^α < ∞ for all α<1/2   (Prop. 5.3)
     ⇒ χ_max(p) ≤ C_η (p_c−p)^{-1-η}            (Prop. 5.5)
     ▼
§6  triangle trace a_3(p) ≤ C_η (p_c−p)^{-η}    (Prop. 6.2)
     ▼
§7  corridor deformation T_t: operator norm barely moves,
     averaged row sum decreases at a rate bounded below
§8  random paths with "escapes" at both endpoints
     ▼
§9  contradiction if ‖T_{p_c}‖ = ∞  ⇒  Theorem 2.6 (unimodular case)
     ⇒ p_c < p_{2→2} by sprinkling; simultaneous interval (Prop. 9.3)
     ▼
§10 mean-field consequences via [Hutchcroft 2020, 2022], [Kozma–Nachmias], …
```

The genuinely new claims are in §§3–9. §2 and §10 mostly assemble
known results.

## What "cleaned-up" means here

The source text is dense and locally fluent. It is also hard to audit:
long chains of terse assertions, constants whose dependencies are
implicit, and frequent "it remains"/"indeed" transitions that hide real
steps. Our editorial rules are:

1. **Faithfulness first.** No silent fixes. Any change to a statement, a
   hypothesis, or the logic of a proof is marked in the source with
   `% EDIT:` and in the text with a margin note.
2. **Explicit dependencies.**
   - Every lemma lists exactly which earlier results it uses.
   - Every constant lists what it may depend on (`G`, `ε`, the old map,
     `p`, …).
   - The order of parameter choices is stated explicitly. This matters
     a lot in §§4, 8, 9.
3. **Separate cited from proved.** Imported results (from [H19],
   Hutchcroft 2020/2022, Antunović–Veselić, Häggström–Peres–Schonmann,
   etc.) are stated as numbered *Facts*, with precise references and
   hypotheses checked against the original sources.
4. **Expand compressed steps.** Arguments like "standard finite energy",
   "by transport", or "one checks" are written out or flagged `[GAP?]`.
5. **Consistent notation.** One symbol per object across the paper:
   - `χ`, `χ_max`, `χ^+`;
   - `ρ = ‖P‖`;
   - `c_σ`;
   - `K` (endpoint kernel) versus `K` (contact counts), which [AI]
     overloads;
   - `D` (field) versus `D(p)` versus `𝒟(F)`, also overloaded in [AI].
6. **Strip filler.** Remove promotional or redundant prose. Keep the
   historical survey only where it locates a result precisely.
7. **Honest metadata.** The authorship line and date of [AI] are kept as
   provenance. They are not presented as a claim of authorship by any
   person.

## Steps flagged for priority review

These are the places where an error would break the argument, and where
we want independent readers first. The list is a reading guide, not a
list of known errors.

- **Lemma 3.3 / Prop. 3.2:** uniformity of the marked-pivotal tail over
  all induced domains; the deletion-uniform goodness bound.
- **Lemmas 4.6–4.8:**
  - injectivity of the inverse coding;
  - measure preservation of the exchanges;
  - the claim that joint undoing in the disjoint, non-adjacent class is
    injective *without* the codes (this removes the factor `W^{2k}`).
- **Prop. 4.3:** the order of parameter choices (`ξ, M, a, n, k`) and
  the claim that the radii need not be uniform.
- **Prop. 5.3:**
  - the lower bound `c_0` on the normalized exterior sum;
  - the likelihood-ratio transfer (5.8) from `p` to `p_c`.
- **Prop. 6.2:** the exponent bookkeeping `A_* < 1`,
  `B_* < 1 + η/2`.
- **Prop. 7.5 and Lemmas 7.6–7.8:** monotonicity of the deformed
  weights under domain enlargement; the two-leg decomposition.
- **Lemma 8.1:** the labeled reversal identity (8.4); uniformity of the
  collision bounds in `L` and `m`.
- **§9:**
  - simultaneous validity of (9.4) once all path constants are fixed;
  - the final incompatibility as `kR → ∞`.

## Repository layout (proposed)

```
original/        unmodified PDF of [AI] (provenance only)
paper/           edited LaTeX source
  main.tex
  sections/      one file per section, mirroring [AI]'s numbering
  refs.bib
review/          per-section review notes, open questions, gap log
notes/           expository notes (e.g. Hutchcroft's operator framework,
                 mass transport on quasi-transitive graphs)
CHANGELOG.md     every substantive edit, with a pointer to [AI]
```

## Building

```bash
cd paper
latexmk -pdf main.tex
```

## Contributing

- **Gaps and errors:** open an issue titled `[§N, Lemma X] short description`.
  Quote the exact statement and say whether you believe the step is
  - *unclear* (needs exposition),
  - *incomplete* (needs an argument), or
  - *false* (give a counterexample or explain why).
- **Edits:** open a PR touching one section at a time. Mathematical
  changes must be logged in `CHANGELOG.md`.
- **Reviews:** sign off on a section in `review/§N.md`. Say what you
  checked and to what level of detail.

## Key references

- I. Benjamini, O. Schramm. *Percolation beyond Z^d, many questions and a
  few answers.* Electron. Comm. Probab. 1 (1996), 71–82.
- T. Hutchcroft. *Percolation on hyperbolic graphs.* GAFA 29 (2019),
  766–810. arXiv:1804.10191.
- T. Hutchcroft. *The L² boundedness condition in nonamenable percolation.*
  EJP 25 (2020), no. 127.
- T. Hutchcroft. *Non-uniqueness and mean-field criticality for percolation
  on nonunimodular transitive graphs.* JAMS 33 (2020), 1101–1165.
- T. Hutchcroft. *Critical percolation on any quasi-transitive graph of
  exponential growth has no infinite clusters.* C. R. Math. 354 (2016).
- T. Hutchcroft. *Slightly supercritical percolation on non-amenable graphs
  I: the distribution of finite clusters.* PLMS 125 (2022), 968–1013.
- O. Häggström, Y. Peres, R. H. Schonmann. *Percolation on transitive graphs
  as a coalescent process.* Perplexing Problems in Probability (1999).
- M. Aizenman, C. M. Newman. *Tree graph inequalities and critical behavior
  in percolation models.* J. Stat. Phys. 36 (1984).
- T. Antunović, I. Veselić. *Sharpness of the phase transition … on
  quasi-transitive graphs.* J. Stat. Phys. 130 (2008).

The full bibliography is in `paper/refs.bib`.
