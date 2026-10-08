# HW03 feedback

**Student:** Jessica
**Homework:** Homework 20261001 — B2.3 Programming Constructs (functions, selection, repetition)
**Submitted as:** `HW261001` (text file) — not a Word document, so this feedback is given as a
separate sheet instead of Word comments.
**Due:** 2026-10-01 · **Marked:** 2026-10-08 · **Submitted on time**

## Score

**95 / 100**

| Question | Score |
|---|---|
| 1 — Reading functions | **14/14** |
| 2 — Reading functions with loops and selection | 11/14 |
| 3 — Dry-run tracing with a method call | 15/16 |
| 4 — Programming: `maximum(a, b, c)` | 15/16 |
| 5 — Programming: `countVowels(String)` | **18/18** |
| 6 — Programming: `isPrime(int)` | **22/22** |

**Excellent work.** Q5 and Q6 are flawless, and Q6 uses the textbook `i <= n / 2` divisor bound
exactly as the mark scheme accepts. Every point lost is a small detail, not a misunderstanding.

## Feedback on incorrect answers

**Q2 (c) — 0/4**
- Both values are wrong. Trace it properly:
  - `countDown(7)`: the condition is `while (n > 0)`, and the body runs `n = n - 2; count++;`.
    n goes **7 → 5 → 3 → 1 → −1**. That is **4** passes, so the method returns **4** (you wrote 3).
  - `countDown(9)`: n goes **9 → 7 → 5 → 3 → 1 → −1** — **5** passes, so it returns **5**
    (you wrote 4).
- The trap: you stopped counting the moment n reached 0. But the loop condition is checked *before*
  each pass, so the pass that starts at n = 1 runs, takes n to −1, and still increments `count`.

**Q3 (a) — 9/10  (-1 mark)**
- The three working rows are perfect — every value of `n`, the return value, `calls` and `total`.
- The mark is lost in the **last row**. The question says "use the last row for the moment the loop
  ends", so that row must show the value each variable still holds at that moment: `calls` = **3**
  and `total` = **12** (nothing resets them). You filled in the Output cell correctly but left those
  two columns blank.

**Q4 — 15/16  (-1 mark)**
- The program itself is right: the signature matches, the two sequential `if`s correctly find the
  largest, and `main` reads three values and prints `Largest: <value>`.
- The mark is lost on "Show your code **and the expected output**" — no expected output was given.
  Always run the program (or trace it by hand) and record the result. For example, with the input
  `2.5 8.1 3.7` the output is `Largest: 8.1`.

## What was correct

- **Q1 (14/14)** — all four outputs exact, and both explanations (Q1(c) `void` has no value to print;
  Q1(d) the method's `y` is local and separate from `main`'s) are spot on.
- **Q2 (a), (b), (d)** — correct.
- **Q3 (b), (c)** — the trace output and the explanation (static variable persists; a parameter `n` is
  recreated on each call) are both complete.
- **Q5 (18/18)** — correct signature, a proper `length()`/`charAt(i)` loop, both upper and lower case
  covered, the count returned rather than printed, and `main` reads a **line** with `nextLine()` and
  prints in the required `Vowels: <count>` form.
- **Q6 (22/22)** — `n <= 1` rejected, early `return false` on the first exact divisor, `main` looping
  from 2 to `limit` inclusive, primes on one space-separated line, and the `Count: <n>` line correct.
