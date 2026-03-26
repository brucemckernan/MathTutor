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

- **Session 01** (`session_01_diagnostic.ipynb`) — **complete**. All questions answered and feedback written.
- **Sessions 02–11** notebooks created and ready. User works through them in order.
- Next up: **Session 02** (`session_02_ibp.ipynb`) — Integration by Parts.

## Session plan

| Session | Topic | Subject | Notes |
|---|---|---|---|
| 02 | Integration by Parts | Calc 2 | Gap from S01 A3; LIATE, iterated, cyclic, invisible dv |
| 03 | Orthogonality, Projections, Least Squares | Linear Algebra | Untested core area |
| 04 | Taylor and Maclaurin Series | Calc 1/2 | Gap tool from S01 A1; limits + approximation |
| 05 | SVD: Computation and Geometry | Linear Algebra | Retest S01 B2 gap; one Python visualisation |
| 06 | Series Convergence Tests | Calc 2 | Ratio, comparison, integral, AST |
| 07 | Multiple Integrals | Calc 3 | Double/triple, polar, change of order |
| 08 | Trig Substitution and Partial Fractions | Calc 2 | Integration techniques follow-up |
| 09 | Lagrange Multipliers | Calc 3 | Constrained optimisation |
| 10 | Line Integrals and Green's Theorem | Calc 3 | Conservative fields, FT of line integrals |
| 11 | Stokes' and Divergence Theorems | Calc 3 | Vector calculus theorems |

After Session 11: plan a mixed review session retesting S01 gaps (IBP, power iteration) and any weaknesses observed along the way.

## Calibration notes (from Session 01)

- **Strong:** Eigendecomposition (B1), identifying correct technique, algebraic execution once setup is right.
- **Gaps:** IBP LIATE assignment (A3), nonlinear back-substitution verification (A2), SVD geometric picture (B2), algorithm implementation precision (B3).
- **Untested:** Taylor series, series convergence, multiple integrals, trig sub, partial fractions, Lagrange multipliers, vector calculus, orthogonality/projections.
- **Difficulty:** Maintain current level for Calculus; stretch slightly on Linear Algebra.

## When resuming

Check which session is next, read that session's notebook to see which questions have been answered, then pick up from there. Ask the user to share their answers or paste the notebook state.
