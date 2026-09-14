# Classwork feedback 20260911

**Student:** Jessica
**Classwork:** Classwork 01 — B2.1 Programming Fundamentals (variables, data types, substring manipulation)
**Date:** 2026-09-11
**Marked:** 2026-09-14

## Score

**77 / 100**

| Question | Score |
|---|---|
| Q1 — data types, naming, print vs println | 10/12 |
| Q2 — string manipulation (tracing) | 12/14 |
| Q3 — scope of variables + tracing | 15/16 |
| Q4 — debugging and scope | 12/14 |
| Q5 — program using all data types | 15/20 |
| Q6 — substring-manipulation program | 13/24 |

Note: `Classwork01_20260911_marked_p1.png` … `_p3.png` in this folder show every
mark and deduction in place on your script.

## Feedback on incorrect answers

**Q1 (b) (-2 marks)**
- All four VALID / INVALID judgements are correct, but the question says
  *"State, **giving a reason**, …"* and no reasons were given.

**Q2 (f) (-2 marks)**
- You wrote `error`. `indexOf` does **not** raise an error when the substring is
  absent — it returns **-1**. The printed output is `-1`.

**Q3 (a) (-1 mark)**
- All the values are correct. The last row, however, shows `2` in the
  **y (local)** column. When `main()` runs, the local `y` from `modify()` no
  longer exists (it was destroyed when the method returned), so that cell should
  be left blank.

**Q4 (a) (-2 marks)**
- You correctly spotted that the local `score` has no value yet. To gain the
  remaining marks it needs to be spelled out: the declaration
  `int score = score + 10;` is **self-referential** — the `score` on the right
  refers to the local variable being declared, which has not been initialised.
  That is why the compiler reports *"variable score might not have been
  initialized"*.

**Q5 (-5 marks)**
- All five data types declared correctly, and the `+` operator is used well.
  Deductions:
  - `System.output.println(...)` — the field is `System.out`, not
    `System.output`. This would not compile.
  - You used `println()` throughout; the question asked for a **mixture** of
    `print()` and `println()`.
  - Only two of the five values are output, and no expected output is shown.

**Q6 (-11 marks)**
- (a) `trim()` is used correctly, but the output line rebuilds the name with an
  extra space (`substring(0, space+1) + " " + substring(space+1)` gives
  `Michael  Jackson` — two spaces). Simply printing `cleanName` would have been
  correct.
- (b) and (c) are **swapped**: (b) asks for the first name but you wrote
  `cleanName.substring(7)` (that is the surname), and (c) asks for the surname
  but you wrote `cleanName.substring(0, 7)` (that is the first name).
- (e) `email.substring(0, domain+1)` includes the `@`, giving `mjackson@`.
  The domain is `email.substring(domain + 1)`.
- (f) correct.

## What went well

- Q2 was almost perfect — `length`, `charAt`, `substring`, `toUpperCase` and
  `replace` were all predicted correctly.
- Q3 was one of the strongest answers in the class: every trace value is right,
  and your explanation of shadowing is complete and precise.
- Q4 (b) is exactly right, including the output.

## Next steps

1. `indexOf` returns an **int index** — and **-1** when not found (it never throws).
2. `System.out` (not `System.output`).
3. When a question asks for a *mixture* of `print()`/`println()`, make sure both appear.
4. Read each part of a multi-part question carefully — (b) and (c) were swapped here.

---
_Marks and margin notes are also marked up on your scanned script
(`Classwork01_20260911_marked_p1.png` … `_p3.png`)._
