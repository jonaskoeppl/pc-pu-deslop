# Nonuniqueness for Bernoulli percolation on nonamenable quasi-transitive graphs: towards a deslopped cleaned-up version

The goal of this project is to create a **human-readable version** of the recent
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

## Current scope: the transitive case first

We proceed in two stages.

1. **Transitive case (current).** The notes in this repository rewrite the
   argument of [AI] for graphs that are connected, locally finite, *simple*,
   *transitive* (vertex-transitive) and nonamenable. In this setting the
   averaging over vertex types, the reduction to simple graphs by
   subdivision and several case distinctions of [AI] disappear, and the main
   line of the argument stands out. The notes cover the transitive versions
   of all claimed results below: Theorem 2.1, Corollary 2.2 (Cayley graphs)
   and Theorem 2.3 (mean-field consequences).
2. **Quasi-transitive case (later).** Once the transitive version has been
   checked by human readers, we plan to extend it to quasi-transitive graphs,
   possibly with loops and multiple edges, as treated in [AI].

Quasi-transitive graphs and multigraphs are **not** covered by the current
version of the notes.

---

## ⚠️ Status

- **Not peer reviewed.** The source manuscript was produced by an AI system.
  Nothing in this repository should be read as an endorsement of
  its correctness.
- **Current version: v0.1, transitive case (November 2026).** A complete
  draft of the notes for transitive graphs (`main.pdf`, 49 pages). The draft
  was prepared from [AI] with AI assistance (Claude, Anthropic). Every step
  was re-derived during the rewrite, and independent AI review passes found
  no mathematical gap; their findings and the resulting repairs are recorded
  in `notes/ledger.md`. **No human reader has checked the draft yet.**
- The notes track the logic of [AI]. `notes/ledger.md` maps every statement
  of [AI] to the notes and records each deviation; deviations beyond the
  specialisation to transitive graphs are also stated in the text. Where a
  step is unclear, under-justified, or appears to fail, we **flag it**
  rather than silently repair it. See `notes/` and the issue tracker.
- If you find a gap or an error, please open an issue (see *Contributing*).

Status of the transitive notes (v0.1):

| Section of the notes | Content | From [AI] | Drafted | AI review | Checked by ≥1 human reader | Open issues |
|---|---|---|---|---|---|---|
| §1 Introduction | context, informal statement | §1 | ☑ | ☑ | ☐ | – |
| §2 Setting and main results | Thm 2.1, Cor 2.2, Thm 2.3 | §1 | ☑ | ☑ | ☐ | – |
| §3 Strategy of the proof | reduction, mechanism, Steps 1–4, assembly | §1.2, §9 | ☑ | ☑ | ☐ | – |
| §4 Preliminaries | kernels, mass transport, trace, Russo, sprinkling, reductions | §2, Prop. 9.3 | ☑ | ☑ | ☐ | – |
| §5 Bridges in critical clusters | Step 1a (Prop. 3.4) | §3 | ☑ | ☑ | ☐ | – |
| §6 Local endpoint maps and amplification | Step 1b (Prop. 3.6) | §4 | ☑ | ☑ | ☐ | – |
| §7 Critical moments, near-critical susceptibility | Step 1c (Prop. 3.7), Step 2 (3.3) | §5 | ☑ | ☑ | ☐ | – |
| §8 The triangle diagram | Step 2 (3.4) | §6 | ☑ | ☑ | ☐ | – |
| §9 The corridor deformation | Step 3 (Prop. 3.10) | §7 | ☑ | ☑ | ☐ | – |
| §10 Escapes at both ends of a random path | Step 4 (Prop. 3.11) | §8 | ☑ | ☑ | ☐ | – |
| §11 Consequences | proof of Thm 2.3 | §10 | ☑ | ☑ | ☐ | – |
| App. A | Russo's formula in operator norm, OSSS inequality | §2, §5 | ☑ | ☑ | ☐ | – |

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

**In the transitive notes.** Theorem 1.1 and Corollaries 1.2–1.3 of [AI]
appear as Theorem 2.1, Corollary 2.2 and Theorem 2.3, for connected,
locally finite, simple, transitive, nonamenable graphs. Their core is
Theorem 3.1: if `Aut(G)` is unimodular, then `‖T_{p_c}‖ < ∞`.

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

## Architecture of the transitive notes

Section 3 of the notes is an overview of the whole proof. It states the
four steps precisely and shows how they combine before any of them is
proved.

```
§3.1  reduction: Thm 2.1 ⇐ Thm 3.1 (‖T_{p_c}‖ < ∞ if Aut(G) is unimodular)
       + sprinkling (Lemma 4.8) + nonunimodular case [H19, Thm 2.9] (Prop. 4.11)
§3.2  mechanism: the row sums χ(p) blow up at p_c, the ℓ² norm need not
§3.3  Part I: a priori estimates
       Step 1  E_{p_c}|C_o|^α < ∞ for all α < 1/2                 (Thm 3.2)
               by contradiction: bridges in critical clusters (Prop. 3.4)
               → amplification of endpoint maps (Prop. 3.6)
               → efficient maps give light tails (Prop. 3.7)
       Step 2  χ(p) ≤ C_η (p_c−p)^{-1-η},  ∇_p ≤ C_η (p_c−p)^{-η}    (Thm 3.8)
§3.4  Part II: the corridor deformation
       Step 3  the norm barely moves, the row sum decreases
               quadratically                                      (Prop. 3.10)
       Step 4  escapes at both ends of a lazy-walk path           (Prop. 3.11)
§3.5  assembly: Steps 1–4 + sprinkling ⇒ contradiction if ‖T_{p_c}‖ = ∞
§§4–10  proofs of the four steps;  §11  mean-field consequences
```

Figure 1 of the notes shows the same dependencies as a diagram.

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

In v0.1 of the transitive notes, rule 1 is implemented by the statement
ledger `notes/ledger.md` rather than by `% EDIT:` markers, and imported
results are stated as cited lemmas and propositions (with the locators
listed in `notes/citations.md`) rather than as *Facts*.

## Steps flagged for priority review

These are the places where an error would break the argument, and where
we want independent readers first. The list is a reading guide, not a
list of known errors. Numbers refer to [AI]; the corresponding places in
the transitive notes are given in brackets.

- **Lemma 3.3 / Prop. 3.2** [notes: Lemma 5.1, Prop. 3.4]: uniformity of the marked-pivotal tail over
  all induced domains; the deletion-uniform goodness bound.
- **Lemmas 4.6–4.8** [notes: Lemmas 6.5–6.8]:
  - injectivity of the inverse coding;
  - measure preservation of the exchanges;
  - the claim that joint undoing in the disjoint, non-adjacent class is
    injective *without* the codes (this removes the factor `W^{2k}`).
- **Prop. 4.3** [notes: Prop. 3.6, proved at the end of §6]: the order of parameter choices (`ξ, M, a, n, k`) and
  the claim that the radii need not be uniform.
- **Prop. 5.3** [notes: Prop. 3.7, §7.2; the transfer is Stage 5]:
  - the lower bound `c_0` on the normalized exterior sum;
  - the likelihood-ratio transfer (5.8) from `p` to `p_c`.
- **Prop. 6.2** [notes: (3.4), §8, Stage 5]: the exponent bookkeeping `A_* < 1`,
  `B_* < 1 + η/2`.
- **Prop. 7.5 and Lemmas 7.6–7.8** [notes: Prop. 3.10, Lemmas 9.1(iii) and 9.4]: monotonicity of the deformed
  weights under domain enlargement; the two-leg decomposition.
- **Lemma 8.1** [notes: Prop. 3.11, §10, identity (10.2)]: the labeled reversal identity (8.4); uniformity of the
  collision bounds in `L` and `m`.
- **§9** [notes: §3.5, (3.7)]:
  - simultaneous validity of (9.4) once all path constants are fixed;
  - the final incompatibility as `kR → ∞`.

## Repository layout

```
main.tex, preamble.tex, refs.bib   LaTeX source of the transitive notes
sections/                          one file per section of the notes
figures/                           TikZ source of Figures 1–4
main.pdf                           compiled notes, current version
notes/                             editorial records of the rewrite
  ledger.md                        statement map [AI] → notes, review findings
  citations.md                     external results used, with checked locators
  figure-notes.md                  what each figure is meant to show
  brief.md                         scope and style decisions
CHANGELOG.md                       versions and substantive edits
```

Planned, not yet present: `original/` (unmodified PDF of [AI], provenance
only), `review/` (per-section review notes by human readers), and the
source of the quasi-transitive version.

## Building

```bash
latexmk -pdf main.tex
```

The source uses `dsfont` for the indicator function if it is installed and
falls back to a bold `1` otherwise.

## Versions

Each version of the notes is marked by a git tag of the form `vX.Y`, and
its compiled PDF is attached to the corresponding GitHub release.
`CHANGELOG.md` lists what changed. Versions `0.x` concern the transitive
case only.

## Contributing

- **Gaps and errors:** open an issue titled `[§N, Lemma X] short description`,
  with numbers referring to the notes (prefix `AI` for the original).
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
