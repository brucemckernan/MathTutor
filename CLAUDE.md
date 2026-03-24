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

## Current state

- **Session 01** (`session_01_diagnostic.ipynb`) is in progress — diagnostic to calibrate difficulty across Calc 1–3 and Linear Algebra.
- Questions: A1 (limits), A2 (multivariable critical points), A3 (improper integrals), B1 (eigendecomposition), B2 (SVD conceptual), B3 (Python power iteration).
- A1 has been answered and feedback given. Remaining questions are outstanding.

## When resuming

Read the current session notebook to check which questions have been answered, then pick up where we left off. Ask the user to share their next answer or to paste the notebook state if it's been updated.
