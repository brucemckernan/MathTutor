# MathTutor — Project Context

## What this project is

A personal math tutoring project. The user is refreshing college-level mathematics for long-term skill consolidation. Background: Calculus 1–3 (limits, derivatives, integrals, sequences/series, multivariable, vector calculus) and Linear Algebra through SVD.

Goals:
- Practice questions with detailed reasoning (not just answers)
- Python exercises accompanying theory where appropriate
- Adaptive difficulty across sessions based on observed performance
- ~2–3 hours/week

## Agreed process

1. Each session has two paired notebooks:
   - `session_NN_<topic>.ipynb` — questions + user's answers
   - `session_NN_<topic>_feedback.ipynb` — Claude's feedback (LaTeX-rendered, with code cells for verification)
2. The user works through questions in their notebook, writing answers in markdown cells and code in code cells.
3. The user pastes or describes answers into Claude Code chat.
4. Claude writes feedback into the corresponding `_feedback.ipynb`, filling in sections as answers arrive. Sections for unanswered questions are left as *Awaiting your answer.*
5. Claude notes misconceptions and uses overall performance to calibrate future sessions.

## Python exercises

Include Python only where computation is genuinely illuminating (e.g. visualising SVD geometry, convergence behaviour). The user's goal is mathematical understanding, not Python practice.

## Current state

- **Sessions 01–12** — **complete**. All questions answered and feedback written.
- **Session 13** (`session_13_trig_log_inverse.ipynb`) — **next up**. Trig sub (secant + double-angle), logarithmic integration, inverse functions. 11 questions across three sections.

## Session plan

| Session | Topic | Subject | Status |
|---|---|---|---|
| 02 | Integration by Parts | Calc 2 | Complete |
| 03 | Orthogonality, Projections, Least Squares | Linear Algebra | Complete |
| 04 | Taylor and Maclaurin Series | Calc 1/2 | Complete |
| 05 | SVD: Computation and Geometry | Linear Algebra | Complete |
| 06 | Series Convergence Tests | Calc 2 | Complete |
| 07 | Multiple Integrals | Calc 3 | Complete |
| 08 | Trig Substitution and Partial Fractions | Calc 2 | Complete |
| 09 | Lagrange Multipliers | Calc 3 | Complete |
| 10 | Line Integrals and Green's Theorem | Calc 3 | Complete |
| 11 | Stokes' and Divergence Theorems | Calc 3 | Complete |
| 12 | Series: Recognition, Manipulation, Identities | Calc 2 | Complete |
| 13 | Trig Sub (secant + double-angle), Log Integration, Inverse Functions | Calc 1/2 | **Next** |

After Session 13: plan a mixed review session retesting S01 gaps (IBP, power iteration) and any weaknesses observed along the way.

## Calibration notes (from Session 01)

- **Strong:** Eigendecomposition (B1), identifying correct technique, algebraic execution once setup is right.
- **Gaps:** IBP LIATE assignment (A3), nonlinear back-substitution verification (A2), SVD geometric picture (B2), algorithm implementation precision (B3).
- **Untested at S01:** Taylor series, series convergence, multiple integrals, trig sub, partial fractions, Lagrange multipliers, vector calculus, orthogonality/projections.
- **Difficulty:** Maintain current level for Calculus; stretch slightly on Linear Algebra.

## Calibration notes (from Session 12)

- **Strong:** Series identification (all 5 Q7(e) series correct), geometric series formula, exponential series, Euler's formula derivation, Basel problem, root test, ratio test, absolute/conditional convergence classification, constant-power factoring (targeted in Q3).
- **Watch:** Index notation precision — in Q7(d) used $n$ as both summation variable and fixed subscript; off-by-one on telescoping closed form ($1 - 1/N$ vs $1 - 1/(N+1)$). Re-indexing elaboration added to S12 feedback notebook (`s12fb_reindex` cell).

## When resuming

Check which session is next, read that session's notebook to see which questions have been answered, then pick up from there. Ask the user to share their answers or paste the notebook state.
