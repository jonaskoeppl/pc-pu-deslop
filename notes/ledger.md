# Statement ledger and rewrite map (original → transitive rewrite)

Math status: AUDITED = re-derived by the editor and checked by an independent reviewer (reports A, B,
C of review round 1); PROVED = re-derived by the editor only; QUOTED = external input with checked
locator (see citations.md). Manuscript status: DRAFTED → INTEGRATED → EXPO-AUDITED → TYPESET-AUDITED.
Numbers refer to the current build (48 pages).

| Original | New | Disposition | Notes | Math | Manuscript |
|---|---|---|---|---|---|
| Thm 1.1 | Thm 2.1 (thm:main) | REWRITE (specialise) | transitive simple graphs | AUDITED | TYPESET-AUDITED |
| Cor 1.2 | Cor 2.2 (cor:cayley) | RETAIN | LP16 locator flagged as TODO in source | PROVED | TYPESET-AUDITED |
| Cor 1.3 | Thm 2.3 (thm:consequences) | REWRITE | no subdivision transfer needed | QUOTED inputs | TYPESET-AUDITED |
| §1.2 strategy | §3 overview | REWRITE + expand | four steps, mechanism, assembly | AUDITED (report C) | TYPESET-AUDITED |
| Lem 2.1 subdivision | Rem 2.5 | DEMOTE TO PROSE | multigraphs out of scope | – | – |
| Lem 2.2 | Lem 4.9 (lem:pc) | RETAIN, cite [Hut16, Thm 1.2] | Peierls proof of p_c<1 kept | QUOTED/AUDITED | TYPESET-AUDITED |
| Lem 2.3 | Lem 4.5 (lem:correlation) | RETAIN, cite Harris/BK; tree bound proved | | QUOTED/AUDITED | TYPESET-AUDITED |
| kernel facts, Lem 9.2 | Lem 4.1 (lem:kernels) | MERGE | Schur, domination, monotone limits | AUDITED | TYPESET-AUDITED |
| Lem 2.4 | Lem 4.10 (lem:p22-pu) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Prop 2.5 | Prop 4.11 (prop:nonunimodular) | RETAIN, cite [Hut19, Thm 2.9] | | QUOTED | TYPESET-AUDITED |
| Thm 2.6 | Thm 3.1 (thm:crit-bdd) | RETAIN | principal estimate | AUDITED | TYPESET-AUDITED |
| Lem 2.7 weighted MTP | Lem 4.2 (lem:mtp) | REWRITE (transitive MTP, cite) | | QUOTED | TYPESET-AUDITED |
| Lem 2.8 trace | Lem 4.3 (lem:trace) | RETAIN (transitive form) | |tr S| ≤ ‖S‖ stated in §4.2 (B4) | AUDITED | TYPESET-AUDITED |
| Lem 2.9 walk + type chain | Lem 4.4 (lem:walk) | REWRITE; type chain REMOVE | P=(I+Adj/d)/2 | AUDITED | TYPESET-AUDITED |
| Lem 2.10 | Lem 4.6 (lem:subcritical) | REWRITE: sharpness cited | attribution fixed (B5): AB87/Men86 on Z^d, AV08 quasi-transitive, DCT16 Thm 1.1 | QUOTED/AUDITED | TYPESET-AUDITED |
| Lem 2.11 Russo | Lem 4.7 (lem:russo), proof App. A.1 | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 2.12 sprinkling | Lem 4.8 (lem:sprinkling) | RETAIN (cite [Hut19, Lem 2.4]) | also displayed in §3.2 (C11) | AUDITED | TYPESET-AUDITED |
| Def 3.1, Prop 3.2 | Def 3.3, Prop 3.4 (prop:good) | RETAIN | contact set 𝒦; bridge distance a pseudometric (A1) | AUDITED | TYPESET-AUDITED |
| Lem 3.3 | Lem 5.1 (lem:ghost) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 3.4 | Lem 5.2 (lem:bridge-radius) | RETAIN | bridge radius defined in §5.2 | AUDITED | TYPESET-AUDITED |
| (4.1), Lem 4.1 | Lem 6.1 (lem:scales) | REWRITE (one orbit) | cites Lem 4.9 (A10) | AUDITED | TYPESET-AUDITED |
| Def 4.2 | Def 3.5 (def:map) | RETAIN (kernel formulation) | success probability now s | AUDITED | TYPESET-AUDITED |
| Prop 4.3 | Prop 3.6 (prop:amplification) | RETAIN | hypothesis α<1/2−ε made explicit (C7/A11) | AUDITED | TYPESET-AUDITED |
| Lem 4.4 | Lem 6.3 (lem:start) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 4.5 | Lem 6.4 (lem:switching) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 4.6 + density text | Lem 6.5, 6.6 (lem:codes, lem:density) | SPLIT | | AUDITED | TYPESET-AUDITED |
| Lem 4.7 | Lem 6.7 (lem:mean-load) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 4.8 | Lem 6.8 (lem:second-moment) | RETAIN | seam-sum argument made explicit (A8) | AUDITED | TYPESET-AUDITED |
| Lem 4.9 | Lem 6.9 (lem:one-step) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 5.1 | Lem 7.1 (lem:intrinsic-ball) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Lem 5.2 | Lem 7.2 (lem:map-deleted) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Prop 5.3 | Prop 3.7 (prop:efficient) + proof of Thm 3.2 | SPLIT | η ≤ (log 2)/2 added (A2) | AUDITED | TYPESET-AUDITED |
| Lem 5.4 OSSS | Lem 7.3 (lem:osss), proof App. A.2 | MOVE, cite [OSSS05, §3.3 eq. (6)] | revealment now rev_i | QUOTED/AUDITED | TYPESET-AUDITED |
| Prop 5.5 | Thm 3.8 (3.3) | RETAIN | constants C'_a, C''_a named (A7) | AUDITED | TYPESET-AUDITED |
| §6 functional, Lem 6.1 | §8, Lem 8.1 (lem:contacts) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Prop 6.2 | Thm 3.8 (3.4) | RETAIN | | AUDITED | TYPESET-AUDITED |
| Def 7.1–Lem 7.9 | Def 3.9, Prop 3.10, §9 | RETAIN, package | C_0 defined once (B3); entrywise derivative (B2) | AUDITED | TYPESET-AUDITED |
| Lem 8.1, 8.2 | Prop 3.11 (prop:escapes), Lem 10.1 | REWRITE (all geodesic segments) | specialised to threshold 1/(4R) (τ=1/4) | AUDITED | TYPESET-AUDITED |
| §9 proof of Thm 2.6 | §3.5 assembly | MOVE | Claim 9.1 removed; stages (1)–(5) | AUDITED | TYPESET-AUDITED |
| Prop 9.3 | Prop 4.12 (prop:interval) | RETAIN | merging argument restated (B6) | AUDITED | TYPESET-AUDITED |
| §10 | §11 | REWRITE | transitive: no transfer | QUOTED inputs | TYPESET-AUDITED |

## Review round 1 (snapshot rev1, main.pdf sha256 bcff3dc9…): dispositions

No BLOCKER and no mathematical MAJOR finding. All findings were repaired:

- Cold read (C1–C15): C1 rewrote the "every power" sentence; C2 "four steps" throughout, Fig. 1 box
  "Assembly", internal proof labels renamed "Stage"; C3 new paragraph "Three structural facts" in §3.2;
  C4 amplification paragraph rewritten; C5 "inverse success probability"; C6 "pseudometric"; C7
  ε fixed before Prop 3.6 (hypothesis α ∈ (0,1/2−ε)), Prop 3.7 uses caps only through |C_x| ≤ M; C8
  avoidance vs. transfer separated; C9 probability vs. number of edges separated, "−p times"; C10
  conditional susceptibility bound explained; C11 sprinkling bound displayed; C12 Fig. 1 reworked
  (sprinkling box moved, arrows to assembly and main result, no hyphenation); C13 notation (see below);
  C14 "simple" added; C15 Z, marks defined, Fig. 2 after Def 3.9, roadmap sentence fixed.
- Part I (A1–A13): all repaired as proposed.
- Part II (B1–B9): all repaired as proposed; B5 also adds [AV08] (verified: J. Stat. Phys. 130 (2008)
  983–1009, Thm 2: p_T = p_H on quasi-transitive graphs) and confirms [DCT16, Thm 1.1] states finite
  susceptibility below β_c on locally finite transitive graphs.

## Notation changes after review (house rule: no symbol reused)

success probability u → s (Part I); amplification steps k → ℓ (§6), first map ℓ → ℓ_0; selected-index
position s → j (§6); iterates j → ℓ (§7); H := log(1/r) and t := U+(σ+ξ)m removed (explicit log(1/r),
cost(Φ)); unit vectors δ_x → 1_x; revealment δ_i → rev_i; stabiliser Γ_x → Stab(x); §5: number of
edges K → m, constant B → D_0, Chernoff parameter λ → s, score Z → Y, local R and C_1 removed; §7:
maximiser Z → Y, cluster B → W, exponent θ → α', F(p) → Ψ(p); §8: ζ → ε_2, threshold t → y,
integration variable q → p'; §10: labelled object ξ → Ξ, middle walk η → π, n_J → n_⋆, τ removed;
§11: β → b; assembly: B → D_⋆, κ → κ_⋆. Kept deliberately: π_n (probability, §6) vs. paths π;
cluster C_i (§6) vs. constant C_1; κ_h, κ (§8) and κ_⋆ as distinct decorated symbols.

## Review round 2 (regression, snapshot rev2, main.pdf sha256 3ab60093…)

No BLOCKER, no MAJOR; all repairs of round 1 verified (renames, ε/β order, cost(Φ) proof, Stage 1
of §7.2, constants of (3.3), Prop 4.12, attribution, Lemma 9.1, threshold 1/(4R), §5 constants,
new §3.2 paragraphs, Fig. 1). Eight MINOR notation/wording findings, all repaired:
R1 exponent a → α in the proof of (3.3) (C_α, c_α, n_α); R2 mean load kernel F(x,z) → L̄(x,z), new
kernel F'_{p_c}; R3 Azuma threshold no longer named, Cauchy–Schwarz written with F_1, F_2; R4 §5
Hoeffding parameter → ϑ, §8 size cutoff → n_0, App. A.1 integration variable → p̃; R5 App. A.1
p_1 → p̄, dominating kernel g → D̄; R6 Props 3.6/3.7 phrased as "arbitrarily small efficiency
ratio", §7.2 Stage 1 without η; R7 generic kernel J → L (§4.1), 𝖩 := T² (§8), B_0 → D_1 (§9);
R8 "at its i-th step", "for every domain Λ" in Lemma 9.1, \mbox in Fig. 1.
Typeset audit: clean build (no warnings, no overfull boxes), 49 pages, every page inspected at
contact-sheet resolution, figure pages at full resolution; contents moved to its own page.
