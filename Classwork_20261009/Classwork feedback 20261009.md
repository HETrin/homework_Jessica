# Classwork feedback 20261009

**Student:** Jessica
**Classwork:** Classwork 20261009 — B2.3 Programming Constructs
(functions · selection · repetition · library functions incl. `Random`)
**Date:** 2026-10-09 · **Marked:** 2026-10-09
**Answer language:** A-Level pseudocode — accepted.

## Score

**86 / 100**

| Question | Score |
|---|---|
| Q1 — Reading functions and loops | 29/30 |
| Q2 — Library functions: the `Random` class | 22/30 |
| Q3 — Writing a complete program (Collatz) | 35/40 |

Full marked pages: `Classwork20261009_marked_AS_20261009_Jessica_p1..p3.png`

## Feedback on incorrect answers

**Q1 (d) — 5/6**
- Both cases are identified and both examples come from this paper — good.
- One sentence is the wrong way round: a value-returning method **can** be used directly in the main
  program. What distinguishes it is that it hands a value *back*, so that value can be stored in a
  variable, printed, or used inside a larger expression. A `void` method gives you nothing to use.

**Q2 (a) (iii) — 1/2**
- The loop runs four times — correct. The missing half: `nextInt()` returns a **new** pseudo-random
  value every time it is called.

**Q2 (a) (iv) — 1/4**
- "Easier to maintain" and "convenient to use" are not the advantages on **slide 38**. That slide
  names two:
  - **Reuse of code** — essential functions are common in many applications, so they do not need to
    be written over again.
  - **Improve reliability** — library code is thoroughly tested and can be relied on.
- Each needs a link to this program: `rnd.nextInt(6)` is called instead of writing and testing your
  own random-number generator.

**Q2 (c) (i) — 2/3**
- The range is given. Add the shape's detail: a circle of **radius 0.5 centred at (0.5, 0.5)** —
  the 0.25 in the test is r².

**Q2 (c) (ii) — 3/4**
- The chain of reasoning is right (circle area `0.25π`, square area 1, hence `π ≈ 4 × cnt / N`).
- One slip: you wrote "with radius 0.25". The **radius is 0.5**; it is **r²** that equals 0.25, which
  is why the test compares against `0.25`.

**Q2 (c) (iii) — 1/3**
- "`cnt` is a double" is not correct — `cnt` is declared as an `int`. The reason `4.0` is written is
  **integer division**: `4 * cnt / N` would be worked out in whole numbers and the fraction thrown
  away. `4.0` forces the expression into `double` arithmetic.

**Q3 (b) — 9/10**
- The loop itself is exactly right — `WHILE n <> 1 DO`, call `nextTerm`, increment the count.
- One fault: the parameter is `n`, but the body uses `num`, which is never declared and never given
  the value of `n`. Add `num <- n` before the loop (or use `n` throughout).

**Q3 (d) — 13/16**
- Clever use of the FOR bound: `FOR index <- 1 TO steps(numb)` evaluates `steps(numb)` **once**, before
  the loop body starts destroying `numb`, so the sequence prints correctly. That is a genuinely good
  piece of thinking.
- But the last line has the same problem: `OUTPUT "Steps", steps(numb)` runs **after** the loop, when
  `numb` is 1 — so it prints 0, not 8. Capture the number of steps into a variable before the loop
  and print that.
- The label must be `Steps: ` (with a colon and a space), and the question asks you to show the
  **expected output** for 6 and 7 — neither was written down.

## What went well

- **Q1 (a), (b), (c)** — all three outputs exact.
- **Q3 (a)** — correct, and `n DIV 2` is the right operator for an integer.
- **Q3 (b)** — the loop logic is textbook; only the variable name is wrong.
- **Q3 (d)** — you avoided the "destroyed variable" trap for the sequence by exploiting when the FOR
  bound is evaluated. Most answers miss that.
- **Q3 (c)** — a complete answer (unknown number of repetitions, precondition loop).

## Next steps

1. **Learn slide 38's two advantages verbatim.** "Reuse of code" and "improve reliability" are
   examinable content, and this paper lost 3 marks for describing *other* slides' ideas.
2. **Integer division again.** You have now met this in two papers. Rule of thumb: if the answer
   should be a fraction and the variables are `int`, one operand must be written as a `double`
   (`4.0`, not `4`).
3. **Check the label the question asks for.** `Steps: 8` versus `Steps 8` — the mark scheme wants the
   first. Same for `Vowels: ` and `Count: ` in earlier homeworks.
4. **Write the expected output when the question asks for it.** Free marks; the answer box was empty.
