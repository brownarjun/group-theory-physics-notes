# group-theory-physics-notes

One-pass, problem-complete study of **group theory and group representations with a physics link**, as preparation for QFT. Sister repo to [brownarjun/weinberg-qm-notes](https://github.com/brownarjun/weinberg-qm-notes); same conventions, same completion rule.

## Sources and their roles

| Book | Role | Why |
|---|---|---|
| Peter Woit, *Quantum Theory, Groups and Representations: An Introduction* (Springer 2017) | **Spine** — read in order | Mathematically honest proofs; freely available as PDF from the author's Columbia website |
| A. Zee, *Group Theory in a Nutshell for Physicists* (Princeton 2016) | **Intuition engine** — read after / alongside each phase | Physical voice: why group theory *is* quantum mechanics; roots & weights, SU(3), Lorentz group |

Do not read both cover to cover. Read Woit for structure and proofs, Zee for the physics meaning of the same material.

## Completion rule

A section/phase is **done** only when:

1. Its key results can be stated without looking.
2. Every notebook in the phase executes end-to-end.
3. The phase's problems file has every problem worked with `date | confidence (1–5) | key idea | gotcha`.
4. **progress.md is updated in the same sitting** — updating the tracker is part of the definition of done, not a separate task.

## Physics link (the point of the repo)

Each phase ends with a **physics deposit**: re-derive a Weinberg/QFT-relevant result using only that phase's machinery. Running connective tissue lives in `physics-dictionary.md` (math object → physical instance).

End state of the project: understand why irreducible representations of the Poincaré group label elementary particles — the front door to QFT, and a direct bridge from the Weinberg reading.

## Phase map

| Phase | Content | Main source | Physics deposit |
|---|---|---|---|
| A | Finite groups; representations; character theory | Woit I (ch. 1–2), Zee part I as intuition | Symmetry types in QM; why degeneracies come in irrep-sized bunches |
| B | Lie groups & algebras; SU(2), SO(3); the double cover | Woit II, Zee | Angular momentum = SU(2) irreps; Weinberg ch. 2–4 bridge |
| C | Roots & weights; SU(3); tensor products | Zee + Woit | CG coefficients from characters; flavor multiplets |
| D | Lorentz & Poincaré groups | Zee + Woit | Classification of one-particle states (Weinberg ch. 2 doorway to QFT) |

Section/chapter numbers in notebooks cite Woit/Zee loosely — **verify numbering against your own copies** and correct in the notebooks.

## Repo layout

- `notebooks/A*/` — one notebook per topic within a phase. Convention (same as Weinberg repo): first cell states what the section claims; every numbered derivation is reproduced symbolically (SymPy, never transcribed); notebook ends with **My summary** and **Gaps** fill-in cells (left for the reader); notebooks are stored unexecuted.
- `problems/phaseX.md` — worked solutions. Format per problem: `date | confidence (1–5) | key idea | gotcha`.
- `physics-dictionary.md` — the running math→physics dictionary.
- `progress.md` — phase-level checklist with exit criteria. **Updated as part of every completion.**
- `reviews/phaseX_quiz.md` — self-quiz sheets + spaced-repetition recaps.

## Computational lab rule

Everything computable is computed from definitions (Cayley tables, conjugacy classes, character tables, decompositions) — verified against the theory's internal checks (orthogonality, sum-of-squares), never copied from a table in a book.
