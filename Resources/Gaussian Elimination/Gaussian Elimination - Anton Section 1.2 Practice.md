---
title: "Gaussian Elimination - Anton Section 1.2 Practice"
date: 2026-10-09
course: MAT216
type: practice
source_section: "Anton 1.2"
tags: [mat216, practice, gaussian-elimination, textbook]
aliases: [Anton Gaussian Elimination Practice]
---

# Gaussian Elimination — Anton Section 1.2 Practice

> [!abstract] Summary
> Eleven textbook systems specifically assigned to the Gaussian elimination method by Exercises 7, 9, and 11, plus one back-substitution warm-up. The problem statements are transcribed from your book; the answer checks were prepared independently for this vault. Expand an answer only after making your own attempt.

## 1. Where these questions come from

Source: [[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=30|Section 1.2, Exercise Set 1.2]].

| Gaussian elimination exercise | Systems printed under | PDF viewer pages |
|---|---|---|
| 7(a–d) | Exercise 6(a–d) | [[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=33|33]]–[[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=34|34]] |
| 9(a–d) | Exercise 8(a–d) | [[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=34|34]] |
| 11(a–c) | Exercise 10(a–c) | [[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=34|34]]–[[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=35|35]] |

> [!note] Why the exercise numbers differ
> Exercises 6, 8, and 10 say Gauss–Jordan elimination. Exercises 7, 9, and 11 ask you to solve those same systems using **Gaussian elimination**. In this note, reduce to echelon form and then back substitute; you do not need to clear entries above every pivot.

## 2. How to practise

For each problem, write the augmented matrix, label the row operations, obtain echelon form, and state the solution type. For a consistent system, back substitute and express every free variable using a real parameter. Finally, check the result in the original equations.

> [!tip] Keep the work readable
> Use exact fractions. Keep variables in the same column order. Apply each operation to the entire augmented row. A contradictory row means no solution; a zero row requires checking how many variables are free.

Suggested order: warm-up → 7(a–d) → 9(a–d) → 11(a–c). The checkboxes record completed attempts, not instructor assignments.

## 3. Warm-up: Exercise 5(a)

Source: [[Howard Anton, Chris Rorres - Elementary Linear Algebra with Applications-Wiley (2005).pdf#page=33|PDF page 33]]. This augmented matrix is already in echelon form. Solve by back substitution.

- [ ] Attempt and check Exercise 5(a).

$$
\left[\begin{array}{ccc|c}1&-3&4&7\\0&1&2&2\\0&0&1&5\end{array}\right].
$$

> [!question]- Answer and back-substitution check
> Read upward: $x_3=5$, $x_2=2-2(5)=-8$, and $x_1=7+3(-8)-4(5)=-37$.
> The unique solution is $(x_1,x_2,x_3)=(-37,-8,5)$.

## 4. Exercise 7: first set

### Exercise 7(a)

- [ ] Attempt and check Exercise 7(a).

$$
\begin{aligned}
x_1+x_2+2x_3&=8\\
-x_1-2x_2+3x_3&=1\\
3x_1-7x_2+4x_3&=10
\end{aligned}
$$

> [!question]- Check answer
> A unique solution: $(x_1,x_2,x_3)=(3,1,2)$.
>
> **Check / hint:** Clear column 1, then eliminate the entry below the second pivot.

### Exercise 7(b)

- [ ] Attempt and check Exercise 7(b).

$$
\begin{aligned}
2x_1+2x_2+2x_3&=0\\
-2x_1+5x_2+2x_3&=1\\
8x_1+x_2+4x_3&=-1
\end{aligned}
$$

> [!question]- Check answer
> Infinitely many solutions. Let $x_3=t$, $t\in\mathbb R$:
> $$
> (x_1,x_2,x_3)=\left(-\frac17-\frac37t,\frac17-\frac47t,t\right).
> $$
>
> **Check / hint:** This is also worked example A in [[Gaussian Elimination - Worked Examples and Practice|the teacher practice note]]. Try it independently before revisiting that solution.

### Exercise 7(c)

- [ ] Attempt and check Exercise 7(c).

$$
\begin{aligned}
x-y+2z-w&=-1\\
2x+y-2z-2w&=-2\\
-x+2y-4z+w&=1\\
3x-3w&=-3
\end{aligned}
$$

> [!question]- Check answer
> Infinitely many solutions with two free variables. Let $z=s$, $w=t$, where $s,t\in\mathbb R$:
> $$
> (x,y,z,w)=(t-1,2s,s,t).
> $$
>
> **Check / hint:** Keep the variable order $(x,y,z,w)$. Two equations disappear during elimination.

### Exercise 7(d)

- [ ] Attempt and check Exercise 7(d).

$$
\begin{aligned}
-2b+3c&=1\\
3a+6b-3c&=-2\\
6a+6b+3c&=5
\end{aligned}
$$

> [!question]- Check answer
> No solution: the system is inconsistent.
>
> **Check / hint:** Twice the second equation plus three times the first has the same left-hand side as the third equation, but its right-hand side is $-1$, not $5$.

## 5. Exercise 9: mixed solution types

### Exercise 9(a)

- [ ] Attempt and check Exercise 9(a).

$$
\begin{aligned}
2x_1-3x_2&=-2\\
2x_1+x_2&=1\\
3x_1+2x_2&=1
\end{aligned}
$$

> [!question]- Check answer
> No solution: the system is inconsistent.
>
> **Check / hint:** The first two equations give $(x_1,x_2)=(\tfrac18,\tfrac34)$, but the third left-hand side then equals $\tfrac{15}{8}$ rather than $1$.

### Exercise 9(b)

- [ ] Attempt and check Exercise 9(b).

$$
\begin{aligned}
3x_1+2x_2-x_3&=-15\\
5x_1+3x_2+2x_3&=0\\
3x_1+x_2+3x_3&=11\\
-6x_1-4x_2+2x_3&=30
\end{aligned}
$$

> [!question]- Check answer
> A unique solution: $(x_1,x_2,x_3)=(-4,2,7)$.
>
> **Check / hint:** The fourth equation is $-2$ times the first. A redundant equation alone does not mean a free variable exists.

### Exercise 9(c)

- [ ] Attempt and check Exercise 9(c).

$$
\begin{aligned}
4x_1-8x_2&=12\\
3x_1-6x_2&=9\\
-2x_1+4x_2&=-6
\end{aligned}
$$

> [!question]- Check answer
> Infinitely many solutions. Let $x_2=t$, $t\in\mathbb R$:
> $$
> (x_1,x_2)=(3+2t,t).
> $$
>
> **Check / hint:** All three equations reduce to $x_1-2x_2=3$.

### Exercise 9(d)

- [ ] Attempt and check Exercise 9(d).

$$
\begin{aligned}
10y-4z+w&=1\\
x+4y-z+w&=2\\
3x+2y+z+2w&=5\\
-2x-8y+2z-2w&=-4\\
x-6y+3z&=1
\end{aligned}
$$

> [!question]- Check answer
> Infinitely many solutions with two free variables. Let $z=s$, $w=t$, where $s,t\in\mathbb R$:
> $$
> (x,y,z,w)=\left(\frac85-\frac35s-\frac35t,\frac1{10}+\frac25s-\frac1{10}t,s,t\right).
> $$
>
> **Check / hint:** Keep the order $(x,y,z,w)$, and swap a row with a nonzero $x$ coefficient to the top. Your solution must include both free variables.

## 6. Exercise 11: rectangular systems

### Exercise 11(a)

- [ ] Attempt and check Exercise 11(a).

$$
\begin{aligned}
5x_1-2x_2+6x_3&=0\\
-2x_1+x_2+3x_3&=1
\end{aligned}
$$

> [!question]- Check answer
> Infinitely many solutions. Let $x_3=t$, $t\in\mathbb R$:
> $$
> (x_1,x_2,x_3)=(2-12t,5-27t,t).
> $$
>
> **Check / hint:** There are only two equations for three variables. Check consistency, then identify the free variable.

### Exercise 11(b)

- [ ] Attempt and check Exercise 11(b).

$$
\begin{aligned}
x_1-2x_2+x_3-4x_4&=1\\
x_1+3x_2+7x_3+2x_4&=2\\
x_1-12x_2-11x_3-16x_4&=5
\end{aligned}
$$

> [!question]- Check answer
> No solution: the system is inconsistent.
>
> **Check / hint:** The third left-hand side is three times the first minus twice the second. Those right-hand sides give $3(1)-2(2)=-1$, contradicting $5$.

### Exercise 11(c)

- [ ] Attempt and check Exercise 11(c).

$$
\begin{aligned}
w+2x-y&=4\\
x-y&=3\\
w+3x-2y&=7\\
2u+4y+w+7x&=7
\end{aligned}
$$

> [!question]- Check answer
> Infinitely many solutions. Let $u=t$, $t\in\mathbb R$:
> $$
> (w,x,y,u)=\left(\frac{t-4}{5},\frac{9-t}{5},\frac{-6-t}{5},t\right).
> $$
>
> **Check / hint:** Use a fixed variable order, for example $(w,x,y,u)$, and include zeros for absent variables. The third equation is the sum of the first two.

## 7. Reflection

- [ ] I can identify contradictions before counting free variables.
- [ ] I can express an infinite solution family with all required parameters.
- [ ] I can explain why a redundant equation does not always imply infinitely many solutions.
- [ ] I can check my answer in the original equations.

> [!todo] Mistake log
> Record an exercise number, the step that went wrong, and the correction here. Reattempt that question later without opening its answer.

---

**Related:** [[Anton and Rorres - Elementary Linear Algebra Book Guide|Book guide]] · [[2026-10-07 Lecture 02 - Gaussian Elimination and Back Substitution|Lecture 02]] · [[Gaussian Elimination - Worked Examples and Practice|Teacher practice]] · [[Gaussian Elimination - Teacher Materials|Teacher materials]] · [[INDEX]]
