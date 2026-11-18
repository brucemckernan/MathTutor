# MathTutor — Project Context

## What this project is

A personal math tutoring project. The user is refreshing college-level mathematics for long-term skill consolidation. Background: Calculus 1–3 (limits, derivatives, integrals, sequences/series, multivariable, vector calculus) and Linear Algebra through SVD.

Goals:
- Practice questions with detailed reasoning (not just answers)
- Python exercises accompanying theory where appropriate
- Adaptive difficulty across sessions based on observed performance
- ~1 question/week (maintenance mode from S14 onwards)

## Phase 1 — completed sessions (S01–S13)

All 13 sessions complete. Full feedback notebooks exist for each.

| Session | Topic | Subject |
|---|---|---|
| 01 | Diagnostic | Mixed |
| 02 | Integration by Parts | Calc 2 |
| 03 | Orthogonality, Projections, Least Squares | Linear Algebra |
| 04 | Taylor and Maclaurin Series | Calc 1/2 |
| 05 | SVD: Computation and Geometry | Linear Algebra |
| 06 | Series Convergence Tests | Calc 2 |
| 07 | Multiple Integrals | Calc 3 |
| 08 | Trig Substitution and Partial Fractions | Calc 2 |
| 09 | Lagrange Multipliers | Calc 3 |
| 10 | Line Integrals and Green's Theorem | Calc 3 |
| 11 | Stokes' and Divergence Theorems | Calc 3 |
| 12 | Series: Recognition, Manipulation, Identities | Calc 2 |
| 13 | Trig Sub (secant + double-angle), Log Integration, Inverse Functions | Calc 1/2 |

## Phase 2 — maintenance mode

**Format:** ~1 question/week from `session_14_maintenance.ipynb`. Questions are pre-loaded for the first 12 weeks (3 months). User submits one answer at a time; Claude writes feedback into `session_14_maintenance_feedback.ipynb`.

**Notebook:** `session_14_maintenance.ipynb` / `session_14_maintenance_feedback.ipynb`

**Agreed process (unchanged):**
1. User works a question in their notebook, writing answers in markdown/code cells.
2. User pastes answer into Claude Code chat.
3. Claude writes feedback into the `_feedback.ipynb`, filling in the relevant section.
4. Claude commits and pushes after each answer.

## Calibration notes (from Session 01)

- **Strong:** Eigendecomposition (B1), identifying correct technique, algebraic execution once setup is right.
- **Gaps:** IBP LIATE assignment (A3), nonlinear back-substitution verification (A2), SVD geometric picture (B2), algorithm implementation precision (B3).

## Calibration notes (from Session 12)

- **Strong:** Series identification, geometric/exponential series, Euler's formula, Basel problem, root/ratio tests, absolute/conditional convergence classification.
- **Watch:** Index notation precision — summation variable vs fixed subscript; off-by-one on telescoping closed forms.

## Calibration notes (from Session 13)

- **Strong:** Trig sub pattern identification and execution (Q1, Q2, Q4), completing the square (Q4), log integration recognition (Q5, Q6, Q7), substitution selection judgment (Q7), implicit differentiation for inverse trig (Q11), inverse function algebra (Q8a, Q9a), $(f^{-1})'$ formula (Q10).
- **Watch:**
  - Reference triangle: initially labelled hypotenuse as $x^2+1$ instead of $\sqrt{x^2+1}$ (Q3). Resolved after elaboration — heuristic now in feedback notebook.
  - Notation slips under pressure: wrote $\cos^2\theta$ where $\cos\theta$ was intended (Q2); wrote $\sqrt{\cos^2\theta} = \cos^2\theta$ rather than $\cos\theta$.
  - Algebraic verification: verified $f(f^{-1}(x))=x$ numerically at one point rather than algebraically (Q8b).
  - Domain vs range of exponential: labelled domain of $e^{x-1}-2$ as $(-2,\infty)$ (the range) rather than $\mathbb{R}$ (Q9b). Error: confused output restriction with input restriction.
  - Interval notation: used $[-\infty,\ldots]$ instead of $(-\infty,\ldots)$.
- **Untested topics identified for maintenance phase:** improper integrals, volumes of revolution, gradient/directional derivatives, row reduction/null space/rank, L'Hôpital's rule, arc length, parametric curves.

## When resuming

Read `session_14_maintenance.ipynb` to find which questions have been answered (non-empty answer cells), then pick up from the next unanswered question. Each question is independent — no need to review prior questions unless the user asks.
