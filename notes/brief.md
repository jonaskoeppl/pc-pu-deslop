# Campaign brief — transitive-case rewrite

**Baseline (mathematical authority).** Manuscript "Nonuniqueness of percolation on nonamenable
quasi-transitive graphs" (author line: OpenAI), dated 24 Sept 2026, 53 pp., A4.
SHA-256 of the PDF: 46a78d044d2713e48cb3faa9b0b9d22da9480193e2202fe63d8e0daa7d8a3dbb.
No TeX source available; the PDF is the only source. The user (Jonas, Gruppe Jahnel, TU Braunschweig)
considers its mathematics correct; this campaign re-derives each step while rewriting and records
any gap instead of polishing it away.

**Route.** Route A, rewrite mapping (§7 of route-build): new spine = transitive case; reuse each
argument only after checking it against the transitive assumptions; then polish (Route B phases 3–6)
on the new manuscript.

**Authorised scope change (user request).** Specialise from quasi-transitive (possibly with loops /
multiple edges) to *transitive simple* graphs. Multigraphs are not covered (subdivision leaves the
transitive class); a remark says so.

**Deliverable.** LaTeX source (preamble.tex, main.tex, sections/*.tex, refs.bib) + compiled PDF.
Audience: participants of a reading course (probabilists who know Grimmett-level percolation, not
necessarily nonamenable percolation).

**Principal results of the rewrite.**
1. Thm 2.1: G connected, locally finite, transitive, simple, nonamenable ⇒ sup_{p<pc}‖T_p‖ = ‖T_pc‖ < ∞,
   pc < p_{2→2} ≤ p_u, and a simultaneous nonuniqueness interval [p1,p2] in the standard coupling.
2. Cor 2.2: Cayley graphs (every finite symmetric generating set).
3. Thm 2.3 (user chose to include consequences): triangle condition, mean-field laws (χ, θ, volume tail,
   intrinsic/extrinsic radius), pc < p_{2→2} ≤ p_exp and exponential decay below p_{2→2}.
Core new statement: Thm 3.1 (critical boundedness, unimodular case).

**Standard tools.** Cite classical results (Harris/FKG, BK, sharpness, mass transport, Hutchcroft's
nonunimodular theorem, critical finiteness); prove only non-standard variants (trace inequality, Russo
in operator norm, OSSS covariance form, sprinkling, lazy-walk norm) — short proofs, appendix if long.

**Style authority.** Gruppe-Jahnel house style (skill jahnel-latex-stil) > latex-math-writing house
style. British spelling; "we"; \coloneqq; cleveref; amsalpha; macros \1 \e \d \dd \c; shared theorem
counter by section; no \frac in running text; no sentence starting with a formula.
Deviation (conflict rule): vertex sets/clusters keep plain capitals (A, B, C_x) as in the source and the
percolation literature; calligraphic letters for events/collections. dsfont is not installed in the
build sandbox: \1 falls back to \mathbf{1} there and uses \mathds{1} where dsfont exists.
Paper size A4 (source A4; German group).

**Build.** latexmk -pdf main.tex; inspect pages via pdftoppm.

**Permissions.** Write in /home/claude/paper; reviewer subagents approved by the user (fresh context,
read-only); no external submission.

**Open decisions.** Author line: left to the user (TODO in source).
