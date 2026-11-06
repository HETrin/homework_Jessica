# Classwork feedback 20261106

**Student:** Jessica
**Classwork:** Classwork 20261106 — B2.2 Data structures
(arrays · pass-by-reference)
**Date:** 2026-11-06 · **Marked:** 2026-11-06
**Answer language:** written in A-Level pseudocode — accepted (full credit for correct content).

## Score

**94 / 100**

| Question | Score |
|---|---|
| Q1 — Reading arrays | 26/30 |
| Q2 — Writing array methods and a complete program | 28/30 |
| Q3 Part B — Pass-by-reference | 40/40 |

Full marked pages: `Classwork20261106_marked_p1..p3.png`

## Feedback on incorrect answers

**Q1(c) — 2/6**
- Index 5 out of bounds is correct, but this is a **runtime error** (ArrayIndexOutOfBoundsException), not a syntax error.
- Say that the program **stops** at that line.

**Q2(b) — 18/20**
- The reading loop, the average call, printing and the above-average loop are correct.
- Initialise `str <- ""` before concatenating, and call `average(temp)` — not `average(temp[1:8])`.
- Not writing the `average` function itself is **not** penalised.

## What went well

- **Q1(a), Q1(b) — full marks.** All values, the trace and the output 8 21 are correct.
- **Q2(a) — 10/10.** Correct function with array parameter, loop, MOD test, counter and RETURN.
- **Q3 — 40/40.** The trace, the BYREF explanation, Replace and Swap are all fully correct.

## Next steps

- Distinguish the error types: **syntax** (will not compile), **runtime** (starts, then crashes), **logic** (runs but the answer is wrong).
- Initialise accumulators (`str`, `total`) before using them.
- Call a function with its arguments, not with an array slice.
