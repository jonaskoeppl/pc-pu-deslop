# Changelog

Numbers in brackets refer to the notes; [AI] is the original manuscript.

## v0.1 — transitive case (November 2026)

- First complete draft of the notes for connected, locally finite, simple,
  transitive, nonamenable graphs (49 pages). Covers the transitive versions of
  all results claimed in [AI]: Theorem 2.1, Corollary 2.2 and Theorem 2.3.
  The quasi-transitive case of [AI] is not covered yet.
- New overview (Section 3): reduction to critical boundedness (Theorem 3.1),
  the mechanism, the four steps stated precisely, and the assembly of the
  contradiction; dependency diagram (Figure 1).
- Prepared from [AI] with AI assistance (Claude, Anthropic). Every step was
  re-derived; independent AI review passes found no mathematical gap. All
  review findings and repairs are recorded in `notes/ledger.md`.
  Not yet checked by a human reader.
- Deviations from [AI] beyond the specialisation: local endpoint maps are
  formalised as kernels (Definition 3.5); Section 10 uses all geodesic
  segments instead of one orbit; the escape threshold is fixed at `1/(4R)`
  (Proposition 3.11); classical results (sharpness, mass transport,
  Hutchcroft's nonunimodular theorem, critical finiteness) are cited rather
  than reproved; notation is changed so that no symbol has two meanings.
- Open: author line; one locator in [Lyons–Peres] marked `TODO` in
  `sections/02-setting.tex`; the figures await approval.
