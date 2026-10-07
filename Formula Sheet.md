---
title: "MAT216 Formula Sheet"
date: 2026-10-05
course: MAT216
tags: [mat216, formula-sheet]
---

# Formula Sheet (running)

## Lecture 01: Systems of Linear Equations

**Standard linear equation**

$$ax + by = c$$

**Matrix form of a system**

$$AX = B$$

| Symbol | Name | Size for $m$ equations, $n$ unknowns |
|---|---|---|
| $A$ | coefficient matrix | $m \times n$ |
| $X$ | variable matrix | $n \times 1$ |
| $B$ | constant matrix | $m \times 1$ |

**Compact form**

$$\sum_{j=1}^{n} a_{ij}x_j = b_i, \qquad i = 1, 2, \dots, m$$

**Types of system**

| Type | Condition | Solutions |
|---|---|---|
| Consistent | has a solution | unique, or infinitely many |
| Inconsistent | reduces to $0 = b,\; b \neq 0$ | none |

**In echelon form (consistent system)**

- no free variable $\Rightarrow$ unique solution
- at least one free variable $\Rightarrow$ infinitely many solutions

**Homogeneous system** ($B = 0$)

- always consistent (zero solution $X = 0$ always works)
- non-trivial solution exists if $m < n$

**Degenerate equation**

$$0x_1 + 0x_2 + \dots + 0x_n = b$$

## Lecture 02: Echelon form and row operations

**Row operations (only these three):**

1. Scale: $R_i' = cR_i$, with $c \neq 0$
2. Swap: $R_i \leftrightarrow R_j$
3. Replace: $R_i' = R_i \pm cR_j$, with $i \neq j$

Use fractions, not decimals. Column operations are not allowed.

**Echelon form:** no row $0 = b$ with $b \neq 0$; the leading unknown of each row is strictly to the right of the one above; entries below a pivot are $0$; all-zero rows are at the bottom.

**Solution type from echelon form:**

- A row $\left[\,0\ \cdots\ 0 \mid b\,\right]$ with $b \neq 0$: no solution
- Number of pivots $=$ number of variables: unique solution
- Number of pivots $<$ number of variables: infinitely many solutions, with $(\text{variables}) - (\text{pivots})$ free variables

**Gaussian elimination goal:** upper triangular form, then back substitution (bottom to top).

**Free-variable solution (example):** if $z = t$ is free, $y - z = 3$ and $x + 2y + z = 2$ give $(x, y, z) = (-4 - 3t,\ 3 + t,\ t)$.

Related: [INDEX](INDEX.md), [Course Overview](Course%20Overview.md), [Lecture 01](Lectures/2026-10-05%20Lecture%2001%20-%20Systems%20of%20Linear%20Equations.md), [Lecture 02](Lectures/2026-10-07%20Lecture%2002%20-%20Gaussian%20Elimination%20and%20Back%20Substitution.md)
