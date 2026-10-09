---
title: "Gaussian Elimination - Worked Examples and Practice"
date: 2026-10-08
course: MAT216
type: practice
related_lecture: 2
tags: [mat216, practice, gaussian-elimination, back-substitution]
aliases: [Gaussian Elimination Practice]
---

# Gaussian Elimination — Worked Examples and Practice

> [!abstract] Summary
> Two instructor worked examples and three practice questions, transcribed from the original PDFs. The solution explanations below were prepared for this vault and checked independently; source answers are retained. Try each problem before opening its solution.

## 1. Before you begin

1. Write the augmented matrix in a fixed variable order.
2. Use row operations to obtain echelon form.
3. Check for a contradiction before counting free variables.
4. Back substitute; introduce real parameters for free variables.
5. State the solution type and substitute back into the original equations.

> [!tip] Use exact fractions
> Keep fractions exact and apply every row operation to the whole augmented row. A zero row alone does not prove infinitely many solutions: check consistency and whether any variable is free.

## 2. Worked example A: infinitely many solutions

Source: [[Additional Examples of Gaussian Elimination.pdf#page=1|Additional examples, PDF pages 1–2]].

$$
\begin{aligned}
2x_1+2x_2+2x_3&=0\\
-2x_1+5x_2+2x_3&=1\\
8x_1+x_2+4x_3&=-1
\end{aligned}
$$

> [!question]- Reveal the worked solution
> Start with
> $$
> \left[\begin{array}{ccc|c}2&2&2&0\\-2&5&2&1\\8&1&4&-1\end{array}\right].
> $$
> Apply $R_1\leftarrow\tfrac12R_1$, then $R_2\leftarrow R_2+2R_1$ and $R_3\leftarrow R_3-8R_1$:
> $$
> \left[\begin{array}{ccc|c}1&1&1&0\\0&7&4&1\\0&-7&-4&-1\end{array}\right].
> $$
> Now $R_3\leftarrow R_3+R_2$, followed by $R_2\leftarrow\tfrac17R_2$:
> $$
> \left[\begin{array}{ccc|c}1&1&1&0\\0&1&\frac47&\frac17\\0&0&0&0\end{array}\right].
> $$
> Let $x_3=t$, with $t\in\mathbb R$. Back substitution gives
> $$
> x_2=\frac17-\frac47t,\qquad x_1=-\frac17-\frac37t.
> $$
> Thus
> $$
> (x_1,x_2,x_3)=\left(-\frac17-\frac37t,\frac17-\frac47t,t\right),\quad t\in\mathbb R.
> $$
> **Conclusion:** the system is consistent with two pivots and one free variable, so it has infinitely many solutions. Substitution yields left-hand sides $0$, $1$, and $-1$ for every real $t$.

## 3. Worked example B: four variables

Source: [[Additional Examples of Gaussian Elimination.pdf#page=3|Additional examples, PDF pages 3–4]].

$$
\begin{aligned}
x_1+2x_2-x_3+x_4&=6\\
-x_1+x_2+2x_3-x_4&=3\\
2x_1-x_2+2x_3+2x_4&=14\\
x_1+x_2-x_3+2x_4&=8
\end{aligned}
$$

> [!question]- Reveal the worked solution
> The augmented matrix is
> $$
> \left[\begin{array}{cccc|c}1&2&-1&1&6\\-1&1&2&-1&3\\2&-1&2&2&14\\1&1&-1&2&8\end{array}\right].
> $$
> Apply $R_2\leftarrow R_2+R_1$, $R_3\leftarrow R_3-2R_1$, and $R_4\leftarrow R_4-R_1$:
> $$
> \left[\begin{array}{cccc|c}1&2&-1&1&6\\0&3&1&0&9\\0&-5&4&0&2\\0&-1&0&1&2\end{array}\right].
> $$
> Scale $R_2\leftarrow\tfrac13R_2$, then use $R_3\leftarrow R_3+5R_2$ and $R_4\leftarrow R_4+R_2$:
> $$
> \left[\begin{array}{cccc|c}1&2&-1&1&6\\0&1&\frac13&0&3\\0&0&\frac{17}{3}&0&17\\0&0&\frac13&1&5\end{array}\right].
> $$
> Scale $R_3\leftarrow\tfrac3{17}R_3$, then $R_4\leftarrow R_4-\tfrac13R_3$:
> $$
> \left[\begin{array}{cccc|c}1&2&-1&1&6\\0&1&\frac13&0&3\\0&0&1&0&3\\0&0&0&1&4\end{array}\right].
> $$
> Back substitute: $x_4=4$, $x_3=3$, $x_2=3-1=2$, and $x_1=6-4+3-4=1$.
> $$
> (x_1,x_2,x_3,x_4)=(1,2,3,4).
> $$
> **Conclusion:** four pivots, four variables, and no contradiction give a unique solution. Substitution reproduces $(6,3,14,8)$ on the right-hand sides.

## 4. Practice questions

Source: [[Practice Problems of Gaussian Elimination.pdf#page=1|Instructor practice sheet]].

### Problem 1

- [x] Solve without viewing the answer.

$$
\begin{aligned}
x+y+2z&=9\\
2x+4y-3z&=1\\
3x+6y-5z&=0
\end{aligned}
$$

> [!question]- Check answer and solution
> **Source answer:** $(x,y,z)=(1,2,3)$.
>
> Start with
> $$
> \left[\begin{array}{ccc|c}1&1&2&9\\2&4&-3&1\\3&6&-5&0\end{array}\right].
> $$
> Apply $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-3R_1$:
> $$
> \left[\begin{array}{ccc|c}1&1&2&9\\0&2&-7&-17\\0&3&-11&-27\end{array}\right].
> $$
> Scale $R_2\leftarrow\tfrac12R_2$, then $R_3\leftarrow R_3-3R_2$:
> $$
> \left[\begin{array}{ccc|c}1&1&2&9\\0&1&-\frac72&-\frac{17}{2}\\0&0&-\frac12&-\frac32\end{array}\right].
> $$
> Hence $z=3$, $y=-\tfrac{17}{2}+\tfrac72(3)=2$, and $x=9-2-6=1$.
> **Conclusion:** a unique solution. Substitution gives $(9,1,0)$.

### Problem 2

- [x] Solve without viewing the answer.

$$
\begin{aligned}
x_2+x_3-2x_4&=-3\\
x_1+2x_2-x_3&=2\\
2x_1+4x_2+x_3-3x_4&=-2\\
x_1-4x_2-7x_3-x_4&=-19
\end{aligned}
$$

> [!question]- Check answer and solution
> **Source answer:** $(x_1,x_2,x_3,x_4)=(-1,2,1,3)$.
>
> Write the augmented matrix and swap $R_1\leftrightarrow R_2$:
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&2\\0&1&1&-2&-3\\2&4&1&-3&-2\\1&-4&-7&-1&-19\end{array}\right].
> $$
> Apply $R_3\leftarrow R_3-2R_1$ and $R_4\leftarrow R_4-R_1$:
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&2\\0&1&1&-2&-3\\0&0&3&-3&-6\\0&-6&-6&-1&-21\end{array}\right].
> $$
> Now $R_4\leftarrow R_4+6R_2$, $R_3\leftarrow\tfrac13R_3$, and $R_4\leftarrow-\tfrac1{13}R_4$:
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&2\\0&1&1&-2&-3\\0&0&1&-1&-2\\0&0&0&1&3\end{array}\right].
> $$
> Read the rows as equations and solve from the bottom up:
> $$
> \begin{aligned}
> x_4&=3\\
> x_3-x_4=-2&\quad\Rightarrow\quad x_3=-2+3=1\\
> x_2+x_3-2x_4=-3&\quad\Rightarrow\quad x_2=-3-1+6=2\\
> x_1+2x_2-x_3=2&\quad\Rightarrow\quad x_1=2-4+1=-1.
> \end{aligned}
> $$
> **Conclusion:** the unique solution is
> $$
> (x_1,x_2,x_3,x_4)=(-1,2,1,3).
> $$
> **Check in the original equations:**
> $$
> \begin{aligned}
> x_2+x_3-2x_4&=2+1-6=-3\\
> x_1+2x_2-x_3&=-1+4-1=2\\
> 2x_1+4x_2+x_3-3x_4&=-2+8+1-9=-2\\
> x_1-4x_2-7x_3-x_4&=-1-8-7-3=-19.
> \end{aligned}
> $$
> The numbers $-3$, $2$, $-2$, and $-19$ are the original right-hand-side constants, not the values of the variables.

### Problem 3

- [x] Solve without viewing the answer.

$$
\begin{aligned}
x_1-x_2+2x_3&=4\\
x_1+x_3&=6\\
2x_1-3x_2+5x_3&=4\\
3x_1+2x_2-x_3&=1
\end{aligned}
$$

> [!question]- Check answer and solution
> **Source answer:** no solution.
>
> Start with
> $$
> \left[\begin{array}{ccc|c}1&-1&2&4\\1&0&1&6\\2&-3&5&4\\3&2&-1&1\end{array}\right].
> $$
> Apply $R_2\leftarrow R_2-R_1$, $R_3\leftarrow R_3-2R_1$, and $R_4\leftarrow R_4-3R_1$:
> $$
> \left[\begin{array}{ccc|c}1&-1&2&4\\0&1&-1&2\\0&-1&1&-4\\0&5&-7&-11\end{array}\right].
> $$
> The operation $R_3\leftarrow R_3+R_2$ produces $[0\;0\;0\mid-2]$, meaning $0=-2$.
> **Conclusion:** the system is inconsistent, so it has no solution. You can stop once the contradiction is established.

## Possible exam concept questions

- [ ] Why does worked example A have exactly one free variable?
- [ ] Why is the first row swap useful in practice problem 2?
- [ ] Does having more equations than unknowns guarantee no solution?
- [ ] Why does the contradictory row in problem 3 take priority over pivot counting?

## Open items

No unresolved symbols were found in these five problem statements. The original PDFs remain available for comparison.

---

**Related:** [[Gaussian Elimination - Teacher Materials|Teacher materials]] · [[2026-10-07 Lecture 02 - Gaussian Elimination and Back Substitution|Lecture 02]] · [[Formula Sheet]] · [[Course Overview]] · [[INDEX]]
