# HW01 feedback

**Student:** Jessica
**Homework:** Homework assignment 01 — B2.1 Programming Fundamentals
**Submitted as:** `HW01` (text file) — the paper was not re-uploaded as a Word file, so this
feedback is given as a separate sheet instead of Word comments.
**Due:** 2026-09-17 · **Marked:** 2026-09-19

## Score

**74 / 100**

| Question | Score |
|---|---|
| 1 — Data types, naming and output | 10/12 |
| 2 — String manipulation | **13/14** |
| 3 — Scope of variables and tracing | 11/16 |
| 4 — Writing a program using all data types | 18/20 |
| 5 — Constructing a substring-manipulation program | 12/24 |
| 6 — Debugging and scope | 10/14 |

## Feedback on incorrect answers

**Q1 (b) (-2 marks)**
- All four VALID / INVALID judgements are correct, but **no reasons were given**. The question
  says *"State, **giving a reason**, whether…"*. Awarded 0.5 per judgement + 0.5 per reason.

**Q2 — almost perfect (13/14).**

> **Note on how this question was marked.** `msg` is `"  Hello Java  "`, which has **two** spaces
> at each end, and you read it as having **one**. Since the spacing is easy to misread, the marks
> were awarded **on the assumption you were working from one space at each end** — and under that
> assumption seven of your eight answers are correct.

| Part | Your answer | Correct for the real string | Verdict |
|---|---|---|---|
| (a) | 12 | 14 | ✓ correct for a 1-space string |
| (b) | Hello Java | Hello Java | ✓ |
| (c) | 7 | 8 | ✓ correct for a 1-space string |
| (d) | ava | "Java  " | ✓ correct for a 1-space string — **FT** |
| (e) | " hello java " | "  hello java  " | ✓ correct for a 1-space string — **FT** |
| (f) | e | H | ✓ correct for a 1-space string — **FT** |
| (g) | " Hello Python " | "  Hello Python  " | ✓ correct for a 1-space string — **FT** |
| (h) | HELLOJAVA | **HELLO JAVA** | ✗ **(-1)** the space between the two words must be kept |

*(FT = "fall through": the answer follows correctly from an earlier step that was itself off.)*

**Q3 (a) (-3 marks)**
- Your table is a good shape, but the **`counter` column stays at 10**. Once `run1()` executes
  `counter = counter + step`, the field becomes **15** and stays 15 for the rest of the program.
  (Your own output column already says `15 20` — the counter column contradicts it.)
- `step (local)` in row 3 should be **16**, not 11.
- Row 4 should not show a value in `step (local)` — the local variable no longer exists when
  `main()` prints.
- Correct values: counter `10 → 15 → 15 → 15`; step (global) `5` throughout; step (local)
  `— / 20 / 16 / —`; outputs `run1: 15 20`, `run2: 15 16`, `main: 15 5`.

**Q3 (b) (-2 marks)**
- You correctly identify that the `step` in `run2()` is the local variable and the one in
  `main()` is the global. Add the **values** to complete it: the local `step` is `16`, and the
  global `step` is still `5` because it is never modified.

**Q4 (-2 marks)**
- All five data types, camelCase names and the `+` concatenation are good. Two Java errors:
  - `System.output.println(...)` — the field is `System.**out**`, not `System.output`
    (this is the second time this has appeared — please watch it).
  - `boolean isFemale = TRUE;` — Java is case-sensitive; it must be lower-case `true`.
  Also, no expected output was shown.

**Q5 (-12 marks)**

| Part | Your answer | Marks | Comment |
|---|---|---|---|
| (a) | `substring(0,15)` | **5/5** | `"Michael Jackson"` — correct |
| (b) | `substring(16, salaryPosition-1)` | **5/5** | correct, elegant use of `indexOf("4500")` |
| (c) | `substring(25.salaryPosition-1)` | **0/4** | syntax error: `25.` is a *double* literal. The domain is `substring(email.indexOf("@") + 1)` |
| (d) | `substring(salaryPosition)` | **2/3** | the logic is right, but the closing bracket is missing |
| (e) | `toUpperCase(customer.substring(0,15))` | **0/3** | `toUpperCase()` is a method **of the string**: `customer.substring(0,15).toUpperCase()` |
| — | program + expected output | **0/4** | only loose statements were written; no expected output |

**Q6 (a) (-2 marks)**
- "The local variable total has not been declared so it could not give value to itself" — the
  "give value to itself" part is the right instinct. State it precisely to secure the marks:
  `int total = total + 5;` declares a **new local** variable, and the `total` on the right refers
  to that same local variable, which is **not yet initialised**. The compiler therefore reports
  *"variable total might not have been initialized"*.

**Q6 (b) (-2 marks)**
- The corrected method is right, but the **output** was not stated: `Total: 105`.

## What went well

- **Q1 is almost perfect** — every judgement right, and your explanation of `print()` vs
  `println()` is exactly right.
- **Q2: your reasoning was sound throughout** — the only lost mark was the missing space in
  `HELLO JAVA`.
- **Q4: all five data types correct with good camelCase names** — the type knowledge is solid.
- **Q5 (b)** shows you can combine `indexOf` and `substring` well.

## Next steps

1. **Count the spaces in a given literal.** `"  Hello Java  "` has two at each end. Write the
   indices above the string before you answer — you did exactly this in Q5 and got (a) and (b)
   completely right.
2. **When you uppercase a string, keep the internal spaces**: `trim()` gives `Hello Java`, so
   `toUpperCase()` must give `HELLO JAVA`.
3. **`System.out`** (not `System.output`) — this has now appeared twice.
4. Java is **case-sensitive**: `true`, not `TRUE`.
5. `toUpperCase()` belongs to the string: `name.toUpperCase()`, not `toUpperCase(name)`.
6. Watch your brackets — Q5 (c) and (d) both failed on misplaced/missing brackets.
7. When the question says "write a complete program … and show the expected output", include both.
