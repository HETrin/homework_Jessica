# HW02 feedback

**Student:** Jessica
**Homework:** Homework 20260924 — B2.3 Programming Constructs (selection, repetition, dry-run tracing)
**Submitted as:** `HW260924` (text file) — not a Word document, so this feedback is given as a
separate sheet instead of Word comments.
**Due:** 2026-09-24 · **Marked:** 2026-09-27

## Score

| | |
|---|---|
| Academic mark | **99 / 100** |
| Late-submission penalty | **−20** |
| **Mark recorded** | **79 / 100** |

| Question | Score |
|---|---|
| 1 — Reading selection structures | **14/14** |
| 2 — Reading repetition structures | **14/14** |
| 3 — Dry-run tracing | 15/16 |
| 4 — Programming: selection | **16/16** |
| 5 — Programming: counted repetition | **18/18** |
| 6 — Programming: sentinel-controlled repetition | **22/22** |

> **About the penalty.** The work itself is worth **99/100** — the best-improved script in the class.
> However the homework was due on **2026-09-24** and was submitted late, so a **20-mark penalty**
> has been applied to the recorded mark. The penalty reflects the deadline, not the quality of your
> work: the comments below describe the 99-mark paper.

**This is an excellent piece of work — the best-improved script in the class.**

## Feedback on incorrect answers

**Q3 (a) (-1 mark)**
- Five of the six rows are perfect, including every value of `total` and the final output line.
- The one mark is lost in the **last row**: the `total` column is left **blank**. At the moment the
  loop ends `total` still holds **69** (the value from row 5) — nothing resets it. Your Output cell
  on that row already says `Total: 69`, so the value is there; it just needs to appear in the
  `total` column too.

Everything else in Q3 is correct, including the explanation in (c): `n++` moves the loop towards
its stopping condition, and without it `n` stays 1 for ever → infinite loop.

## What went well

**Q1, Q2 (28/28) — every single answer correct.**
- Q1(d) deserves a special mention: not only did you give both outputs (`Failed` / `Take re-sit`
  and `Passed` / `Take re-sit`), you **explained the reason** — the `if-else` controls only the
  first statement, so `Take re-sit` sits outside the block and always prints. Most of the class
  missed `Take re-sit` for grade = 75; you got it *and* said why.

**Q4 (16/16) — a complete, correct program.**
- Scanner, range validation with `||`, the `else-if` chain in descending order with correct
  boundaries, and the right output for every case. Full marks in every band.

**Q5 (18/18) — a complete, correct program.**
- The loop runs exactly ten times, the sum accumulates correctly, and positives/negatives are
  separated properly. Note you used `else if (num < 0)` rather than a plain `else` — that is the
  careful choice, because **zero is neither positive nor negative**. Your output is also labelled.

**Q6 (22/22) — full marks on the hardest question on the paper.**
- **Priming read before the loop** ✓ and the re-read as the last statement of the body ✓ — so the
  sentinel −1 is never added to the sum or counted.
- Count and sum accumulate correctly.
- **The divide-by-zero guard is exactly right**: `if (count > 0)` around the average, with a
  sensible `else` branch ("No valid values.") when nothing was entered.
- **The average casts to double**: `(double) sum / count` — this is the detail most students miss;
  without the cast the decimal part would be discarded.
- `max` is initialised before the loop and updated with `if (value > max)` ✓.
- Q6(b) is also fully correct: the `while` condition is tested before the body runs, so a value
  must already exist for that test — and reading first also lets the user type −1 straight away to
  skip the loop entirely.

## Next steps

1. **In a trace table, every cell in a row must be filled** — including the final "loop ends" row.
   If a variable is unchanged, write its value again rather than leaving a blank.
2. **Keep doing what you did here.** Everything that cost you marks in HW01 — `System.output`
   (wrong spelling), `toUpperCase(...)` used as a function, unbalanced brackets in `substring`,
   a trace table whose columns contradicted its Output column — is **completely gone** in this
   paper. The programs are complete, compile, and are correctly labelled.
3. This is the standard to hold yourself to from now on.

> **Note:** your `HW261001` file (Homework 20261001) has also arrived and will be marked
> separately.
