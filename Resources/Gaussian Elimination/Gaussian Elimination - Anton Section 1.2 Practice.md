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
> Eleven textbook systems specifically assigned to the Gaussian elimination method by Exercises 7, 9, and 11, plus one back-substitution warm-up. The problem statements are transcribed from your book; the worked solutions were prepared independently for this vault. Each solution shows the augmented matrix, row operations, and back substitution or contradiction. Expand a solution only after making your own attempt.

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
> The rows represent $x_1-3x_2+4x_3=7$, $x_2+2x_3=2$, and $x_3=5$.
> Solve from the bottom row upward:
> $$
> \begin{aligned}
> x_3&=5\\
> x_2+2x_3=2&\quad\Rightarrow\quad x_2=2-2(5)=-8\\
> x_1-3x_2+4x_3=7&\quad\Rightarrow\quad x_1=7+3(-8)-4(5)=-37.
> \end{aligned}
> $$
> **Conclusion:** the unique solution is $(x_1,x_2,x_3)=(-37,-8,5)$.
> **Check:** $-37-3(-8)+4(5)=7$, $-8+2(5)=2$, and $x_3=5$.

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

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2, x_3)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{ccc|c}1&1&2&8\\-1&-2&3&1\\3&-7&4&10\end{array}\right].
> $$
>
> **2. Clear entries below this pivot:** $R_2\leftarrow R_2+R_1$, $R_3\leftarrow R_3-3R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&2&8\\0&-1&5&9\\0&-10&-2&-14\end{array}\right].
> $$
>
> **3. Make the pivot 1:** $R_2\leftarrow -R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&2&8\\0&1&-5&-9\\0&-10&-2&-14\end{array}\right].
> $$
>
> **4. Clear entries below this pivot:** $R_3\leftarrow R_3+10R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&2&8\\0&1&-5&-9\\0&0&-52&-104\end{array}\right].
> $$
>
> **5. Make the pivot 1:** $R_3\leftarrow (-\frac{1}{52})R_3$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&2&8\\0&1&-5&-9\\0&0&1&2\end{array}\right].
> $$
>
> **6. Read the echelon rows and back substitute.**
>
> Every variable has a pivot. Work upward from the last nonzero row.
>
> $$
> \begin{aligned}
> x_3&=2\\
> x_2-5x_3=-9&\quad\Rightarrow\quad x_2=-9+5\left(2\right)=1\\
> x_1+x_2+2x_3=8&\quad\Rightarrow\quad x_1=8-\left(1\right)-2\left(2\right)=3
> \end{aligned}
> $$
>
> **Conclusion:** the system has a **unique solution**.
>
> $$
> (x_1,x_2,x_3)=\left(3,\;1,\;2\right).
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side.

### Exercise 7(b)

- [ ] Attempt and check Exercise 7(b).

$$
\begin{aligned}
2x_1+2x_2+2x_3&=0\\
-2x_1+5x_2+2x_3&=1\\
8x_1+x_2+4x_3&=-1
\end{aligned}
$$

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2, x_3)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{ccc|c}2&2&2&0\\-2&5&2&1\\8&1&4&-1\end{array}\right].
> $$
>
> **2. Make the pivot 1:** $R_1\leftarrow (\frac{1}{2})R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&1&0\\-2&5&2&1\\8&1&4&-1\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_2\leftarrow R_2+2R_1$, $R_3\leftarrow R_3-8R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&1&0\\0&7&4&1\\0&-7&-4&-1\end{array}\right].
> $$
>
> **4. Make the pivot 1:** $R_2\leftarrow (\frac{1}{7})R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&1&0\\0&1&\frac{4}{7}&\frac{1}{7}\\0&-7&-4&-1\end{array}\right].
> $$
>
> **5. Clear entries below this pivot:** $R_3\leftarrow R_3+7R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&1&1&0\\0&1&\frac{4}{7}&\frac{1}{7}\\0&0&0&0\end{array}\right].
> $$
>
> **6. Read the echelon rows and back substitute.**
>
> The free variable is $x_3$. Set $x_3=t$, with the parameter in $\mathbb R$.
>
> $$
> \begin{aligned}
> x_2+\frac{4}{7}x_3=\frac{1}{7}&\quad\Rightarrow\quad x_2=\frac{1}{7}-\frac{4}{7}\left(t\right)=\frac{1}{7}-\frac{4}{7}t\\
> x_1+x_2+x_3=0&\quad\Rightarrow\quad x_1=0-\left(\frac{1}{7}-\frac{4}{7}t\right)-\left(t\right)=-\frac{1}{7}-\frac{3}{7}t
> \end{aligned}
> $$
>
> **Conclusion:** the system is consistent with 1 free variable, so it has **infinitely many solutions**.
>
> $$
> (x_1,x_2,x_3)=\left(-\frac{1}{7}-\frac{3}{7}t,\;\frac{1}{7}-\frac{4}{7}t,\;t\right),\qquad t\in\mathbb R.
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side for every real parameter choice.

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

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x, y, z, w)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{cccc|c}1&-1&2&-1&-1\\2&1&-2&-2&-2\\-1&2&-4&1&1\\3&0&0&-3&-3\end{array}\right].
> $$
>
> **2. Clear entries below this pivot:** $R_2\leftarrow R_2-2R_1$, $R_3\leftarrow R_3+R_1$, $R_4\leftarrow R_4-3R_1$.
>
> $$
> \left[\begin{array}{cccc|c}1&-1&2&-1&-1\\0&3&-6&0&0\\0&1&-2&0&0\\0&3&-6&0&0\end{array}\right].
> $$
>
> **3. Make the pivot 1:** $R_2\leftarrow (\frac{1}{3})R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&-1&2&-1&-1\\0&1&-2&0&0\\0&1&-2&0&0\\0&3&-6&0&0\end{array}\right].
> $$
>
> **4. Clear entries below this pivot:** $R_3\leftarrow R_3-R_2$, $R_4\leftarrow R_4-3R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&-1&2&-1&-1\\0&1&-2&0&0\\0&0&0&0&0\\0&0&0&0&0\end{array}\right].
> $$
>
> **5. Read the echelon rows and back substitute.**
>
> The free variables are $z$, $w$. Set $z=s$, $w=t$, with all parameters in $\mathbb R$.
>
> $$
> \begin{aligned}
> y-2z=0&\quad\Rightarrow\quad y=0+2\left(s\right)=2s\\
> x-y+2z-w=-1&\quad\Rightarrow\quad x=-1+\left(2s\right)-2\left(s\right)+\left(t\right)=-1+t
> \end{aligned}
> $$
>
> **Conclusion:** the system is consistent with 2 free variables, so it has **infinitely many solutions**.
>
> $$
> (x,y,z,w)=\left(-1+t,\;2s,\;s,\;t\right),\qquad s,t\in\mathbb R.
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side for every real parameter choice.

### Exercise 7(d)

- [ ] Attempt and check Exercise 7(d).

$$
\begin{aligned}
-2b+3c&=1\\
3a+6b-3c&=-2\\
6a+6b+3c&=5
\end{aligned}
$$

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(a, b, c)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{ccc|c}0&-2&3&1\\3&6&-3&-2\\6&6&3&5\end{array}\right].
> $$
>
> **2. Swap rows to obtain a nonzero pivot:** $R_1\leftrightarrow R_2$.
>
> $$
> \left[\begin{array}{ccc|c}3&6&-3&-2\\0&-2&3&1\\6&6&3&5\end{array}\right].
> $$
>
> **3. Make the pivot 1:** $R_1\leftarrow (\frac{1}{3})R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&2&-1&-\frac{2}{3}\\0&-2&3&1\\6&6&3&5\end{array}\right].
> $$
>
> **4. Clear entries below this pivot:** $R_3\leftarrow R_3-6R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&2&-1&-\frac{2}{3}\\0&-2&3&1\\0&-6&9&9\end{array}\right].
> $$
>
> **5. Make the pivot 1:** $R_2\leftarrow (-\frac{1}{2})R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&2&-1&-\frac{2}{3}\\0&1&-\frac{3}{2}&-\frac{1}{2}\\0&-6&9&9\end{array}\right].
> $$
>
> **6. Clear entries below this pivot:** $R_3\leftarrow R_3+6R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&2&-1&-\frac{2}{3}\\0&1&-\frac{3}{2}&-\frac{1}{2}\\0&0&0&6\end{array}\right].
> $$
>
> **Conclusion:** a row reads $0=6$, which is impossible. The system is **inconsistent**, so it has **no solution**. No back substitution is needed.

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

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{cc|c}2&-3&-2\\2&1&1\\3&2&1\end{array}\right].
> $$
>
> **2. Make the pivot 1:** $R_1\leftarrow (\frac{1}{2})R_1$.
>
> $$
> \left[\begin{array}{cc|c}1&-\frac{3}{2}&-1\\2&1&1\\3&2&1\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_2\leftarrow R_2-2R_1$, $R_3\leftarrow R_3-3R_1$.
>
> $$
> \left[\begin{array}{cc|c}1&-\frac{3}{2}&-1\\0&4&3\\0&\frac{13}{2}&4\end{array}\right].
> $$
>
> **4. Make the pivot 1:** $R_2\leftarrow (\frac{1}{4})R_2$.
>
> $$
> \left[\begin{array}{cc|c}1&-\frac{3}{2}&-1\\0&1&\frac{3}{4}\\0&\frac{13}{2}&4\end{array}\right].
> $$
>
> **5. Clear entries below this pivot:** $R_3\leftarrow R_3-(\frac{13}{2})R_2$.
>
> $$
> \left[\begin{array}{cc|c}1&-\frac{3}{2}&-1\\0&1&\frac{3}{4}\\0&0&-\frac{7}{8}\end{array}\right].
> $$
>
> **Conclusion:** a row reads $0=-\frac{7}{8}$, which is impossible. The system is **inconsistent**, so it has **no solution**. No back substitution is needed.

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

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2, x_3)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{ccc|c}3&2&-1&-15\\5&3&2&0\\3&1&3&11\\-6&-4&2&30\end{array}\right].
> $$
>
> **2. Make the pivot 1:** $R_1\leftarrow (\frac{1}{3})R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&\frac{2}{3}&-\frac{1}{3}&-5\\5&3&2&0\\3&1&3&11\\-6&-4&2&30\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_2\leftarrow R_2-5R_1$, $R_3\leftarrow R_3-3R_1$, $R_4\leftarrow R_4+6R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&\frac{2}{3}&-\frac{1}{3}&-5\\0&-\frac{1}{3}&\frac{11}{3}&25\\0&-1&4&26\\0&0&0&0\end{array}\right].
> $$
>
> **4. Make the pivot 1:** $R_2\leftarrow (-3)R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&\frac{2}{3}&-\frac{1}{3}&-5\\0&1&-11&-75\\0&-1&4&26\\0&0&0&0\end{array}\right].
> $$
>
> **5. Clear entries below this pivot:** $R_3\leftarrow R_3+R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&\frac{2}{3}&-\frac{1}{3}&-5\\0&1&-11&-75\\0&0&-7&-49\\0&0&0&0\end{array}\right].
> $$
>
> **6. Make the pivot 1:** $R_3\leftarrow (-\frac{1}{7})R_3$.
>
> $$
> \left[\begin{array}{ccc|c}1&\frac{2}{3}&-\frac{1}{3}&-5\\0&1&-11&-75\\0&0&1&7\\0&0&0&0\end{array}\right].
> $$
>
> **7. Read the echelon rows and back substitute.**
>
> Every variable has a pivot. Work upward from the last nonzero row.
>
> $$
> \begin{aligned}
> x_3&=7\\
> x_2-11x_3=-75&\quad\Rightarrow\quad x_2=-75+11\left(7\right)=2\\
> x_1+\frac{2}{3}x_2-\frac{1}{3}x_3=-5&\quad\Rightarrow\quad x_1=-5-\frac{2}{3}\left(2\right)+\frac{1}{3}\left(7\right)=-4
> \end{aligned}
> $$
>
> **Conclusion:** the system has a **unique solution**.
>
> $$
> (x_1,x_2,x_3)=\left(-4,\;2,\;7\right).
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side.

### Exercise 9(c)

- [ ] Attempt and check Exercise 9(c).

$$
\begin{aligned}
4x_1-8x_2&=12\\
3x_1-6x_2&=9\\
-2x_1+4x_2&=-6
\end{aligned}
$$

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{cc|c}4&-8&12\\3&-6&9\\-2&4&-6\end{array}\right].
> $$
>
> **2. Make the pivot 1:** $R_1\leftarrow (\frac{1}{4})R_1$.
>
> $$
> \left[\begin{array}{cc|c}1&-2&3\\3&-6&9\\-2&4&-6\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_2\leftarrow R_2-3R_1$, $R_3\leftarrow R_3+2R_1$.
>
> $$
> \left[\begin{array}{cc|c}1&-2&3\\0&0&0\\0&0&0\end{array}\right].
> $$
>
> **4. Read the echelon rows and back substitute.**
>
> The free variable is $x_2$. Set $x_2=t$, with the parameter in $\mathbb R$.
>
> $$
> \begin{aligned}
> x_1-2x_2=3&\quad\Rightarrow\quad x_1=3+2\left(t\right)=3+2t
> \end{aligned}
> $$
>
> **Conclusion:** the system is consistent with 1 free variable, so it has **infinitely many solutions**.
>
> $$
> (x_1,x_2)=\left(3+2t,\;t\right),\qquad t\in\mathbb R.
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side for every real parameter choice.

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

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x, y, z, w)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{cccc|c}0&10&-4&1&1\\1&4&-1&1&2\\3&2&1&2&5\\-2&-8&2&-2&-4\\1&-6&3&0&1\end{array}\right].
> $$
>
> **2. Swap rows to obtain a nonzero pivot:** $R_1\leftrightarrow R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&4&-1&1&2\\0&10&-4&1&1\\3&2&1&2&5\\-2&-8&2&-2&-4\\1&-6&3&0&1\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_3\leftarrow R_3-3R_1$, $R_4\leftarrow R_4+2R_1$, $R_5\leftarrow R_5-R_1$.
>
> $$
> \left[\begin{array}{cccc|c}1&4&-1&1&2\\0&10&-4&1&1\\0&-10&4&-1&-1\\0&0&0&0&0\\0&-10&4&-1&-1\end{array}\right].
> $$
>
> **4. Make the pivot 1:** $R_2\leftarrow (\frac{1}{10})R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&4&-1&1&2\\0&1&-\frac{2}{5}&\frac{1}{10}&\frac{1}{10}\\0&-10&4&-1&-1\\0&0&0&0&0\\0&-10&4&-1&-1\end{array}\right].
> $$
>
> **5. Clear entries below this pivot:** $R_3\leftarrow R_3+10R_2$, $R_5\leftarrow R_5+10R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&4&-1&1&2\\0&1&-\frac{2}{5}&\frac{1}{10}&\frac{1}{10}\\0&0&0&0&0\\0&0&0&0&0\\0&0&0&0&0\end{array}\right].
> $$
>
> **6. Read the echelon rows and back substitute.**
>
> The free variables are $z$, $w$. Set $z=s$, $w=t$, with all parameters in $\mathbb R$.
>
> $$
> \begin{aligned}
> y-\frac{2}{5}z+\frac{1}{10}w=\frac{1}{10}&\quad\Rightarrow\quad y=\frac{1}{10}+\frac{2}{5}\left(s\right)-\frac{1}{10}\left(t\right)=\frac{1}{10}+\frac{2}{5}s-\frac{1}{10}t\\
> x+4y-z+w=2&\quad\Rightarrow\quad x=2-4\left(\frac{1}{10}+\frac{2}{5}s-\frac{1}{10}t\right)+\left(s\right)-\left(t\right)=\frac{8}{5}-\frac{3}{5}s-\frac{3}{5}t
> \end{aligned}
> $$
>
> **Conclusion:** the system is consistent with 2 free variables, so it has **infinitely many solutions**.
>
> $$
> (x,y,z,w)=\left(\frac{8}{5}-\frac{3}{5}s-\frac{3}{5}t,\;\frac{1}{10}+\frac{2}{5}s-\frac{1}{10}t,\;s,\;t\right),\qquad s,t\in\mathbb R.
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side for every real parameter choice.

## 6. Exercise 11: rectangular systems

### Exercise 11(a)

- [ ] Attempt and check Exercise 11(a).

$$
\begin{aligned}
5x_1-2x_2+6x_3&=0\\
-2x_1+x_2+3x_3&=1
\end{aligned}
$$

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2, x_3)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{ccc|c}5&-2&6&0\\-2&1&3&1\end{array}\right].
> $$
>
> **2. Make the pivot 1:** $R_1\leftarrow (\frac{1}{5})R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&-\frac{2}{5}&\frac{6}{5}&0\\-2&1&3&1\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_2\leftarrow R_2+2R_1$.
>
> $$
> \left[\begin{array}{ccc|c}1&-\frac{2}{5}&\frac{6}{5}&0\\0&\frac{1}{5}&\frac{27}{5}&1\end{array}\right].
> $$
>
> **4. Make the pivot 1:** $R_2\leftarrow 5R_2$.
>
> $$
> \left[\begin{array}{ccc|c}1&-\frac{2}{5}&\frac{6}{5}&0\\0&1&27&5\end{array}\right].
> $$
>
> **5. Read the echelon rows and back substitute.**
>
> The free variable is $x_3$. Set $x_3=t$, with the parameter in $\mathbb R$.
>
> $$
> \begin{aligned}
> x_2+27x_3=5&\quad\Rightarrow\quad x_2=5-27\left(t\right)=5-27t\\
> x_1-\frac{2}{5}x_2+\frac{6}{5}x_3=0&\quad\Rightarrow\quad x_1=0+\frac{2}{5}\left(5-27t\right)-\frac{6}{5}\left(t\right)=2-12t
> \end{aligned}
> $$
>
> **Conclusion:** the system is consistent with 1 free variable, so it has **infinitely many solutions**.
>
> $$
> (x_1,x_2,x_3)=\left(2-12t,\;5-27t,\;t\right),\qquad t\in\mathbb R.
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side for every real parameter choice.

### Exercise 11(b)

- [ ] Attempt and check Exercise 11(b).

$$
\begin{aligned}
x_1-2x_2+x_3-4x_4&=1\\
x_1+3x_2+7x_3+2x_4&=2\\
x_1-12x_2-11x_3-16x_4&=5
\end{aligned}
$$

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(x_1, x_2, x_3, x_4)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{cccc|c}1&-2&1&-4&1\\1&3&7&2&2\\1&-12&-11&-16&5\end{array}\right].
> $$
>
> **2. Clear entries below this pivot:** $R_2\leftarrow R_2-R_1$, $R_3\leftarrow R_3-R_1$.
>
> $$
> \left[\begin{array}{cccc|c}1&-2&1&-4&1\\0&5&6&6&1\\0&-10&-12&-12&4\end{array}\right].
> $$
>
> **3. Make the pivot 1:** $R_2\leftarrow (\frac{1}{5})R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&-2&1&-4&1\\0&1&\frac{6}{5}&\frac{6}{5}&\frac{1}{5}\\0&-10&-12&-12&4\end{array}\right].
> $$
>
> **4. Clear entries below this pivot:** $R_3\leftarrow R_3+10R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&-2&1&-4&1\\0&1&\frac{6}{5}&\frac{6}{5}&\frac{1}{5}\\0&0&0&0&6\end{array}\right].
> $$
>
> **Conclusion:** a row reads $0=6$, which is impossible. The system is **inconsistent**, so it has **no solution**. No back substitution is needed.

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

> [!question]- Worked solution
> **1. Write the augmented matrix.** Use variable order $(w, x, y, u)$; the column after the bar contains the constants.
>
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&4\\0&1&-1&0&3\\1&3&-2&0&7\\1&7&4&2&7\end{array}\right].
> $$
>
> **2. Clear entries below this pivot:** $R_3\leftarrow R_3-R_1$, $R_4\leftarrow R_4-R_1$.
>
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&4\\0&1&-1&0&3\\0&1&-1&0&3\\0&5&5&2&3\end{array}\right].
> $$
>
> **3. Clear entries below this pivot:** $R_3\leftarrow R_3-R_2$, $R_4\leftarrow R_4-5R_2$.
>
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&4\\0&1&-1&0&3\\0&0&0&0&0\\0&0&10&2&-12\end{array}\right].
> $$
>
> **4. Swap rows to obtain a nonzero pivot:** $R_3\leftrightarrow R_4$.
>
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&4\\0&1&-1&0&3\\0&0&10&2&-12\\0&0&0&0&0\end{array}\right].
> $$
>
> **5. Make the pivot 1:** $R_3\leftarrow (\frac{1}{10})R_3$.
>
> $$
> \left[\begin{array}{cccc|c}1&2&-1&0&4\\0&1&-1&0&3\\0&0&1&\frac{1}{5}&-\frac{6}{5}\\0&0&0&0&0\end{array}\right].
> $$
>
> **6. Read the echelon rows and back substitute.**
>
> The free variable is $u$. Set $u=t$, with the parameter in $\mathbb R$.
>
> $$
> \begin{aligned}
> y+\frac{1}{5}u=-\frac{6}{5}&\quad\Rightarrow\quad y=-\frac{6}{5}-\frac{1}{5}\left(t\right)=-\frac{6}{5}-\frac{1}{5}t\\
> x-y=3&\quad\Rightarrow\quad x=3+\left(-\frac{6}{5}-\frac{1}{5}t\right)=\frac{9}{5}-\frac{1}{5}t\\
> w+2x-y=4&\quad\Rightarrow\quad w=4-2\left(\frac{9}{5}-\frac{1}{5}t\right)+\left(-\frac{6}{5}-\frac{1}{5}t\right)=-\frac{4}{5}+\frac{1}{5}t
> \end{aligned}
> $$
>
> **Conclusion:** the system is consistent with 1 free variable, so it has **infinitely many solutions**.
>
> $$
> (w,x,y,u)=\left(-\frac{4}{5}+\frac{1}{5}t,\;\frac{9}{5}-\frac{1}{5}t,\;-\frac{6}{5}-\frac{1}{5}t,\;t\right),\qquad t\in\mathbb R.
> $$
>
> **Check:** substituting these variable values into the original equations reproduces each right-hand side for every real parameter choice.

## 7. Reflection

- [ ] I can identify contradictions before counting free variables.
- [ ] I can express an infinite solution family with all required parameters.
- [ ] I can explain why a redundant equation does not always imply infinitely many solutions.
- [ ] I can check my answer in the original equations.

> [!todo] Mistake log
> Record an exercise number, the step that went wrong, and the correction here. Reattempt that question later without opening its answer.

---

**Related:** [[Anton and Rorres - Elementary Linear Algebra Book Guide|Book guide]] · [[2026-10-07 Lecture 02 - Gaussian Elimination and Back Substitution|Lecture 02]] · [[Gaussian Elimination - Worked Examples and Practice|Teacher practice]] · [[Gaussian Elimination - Teacher Materials|Teacher materials]] · [[INDEX]]
