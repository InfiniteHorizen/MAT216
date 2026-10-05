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

Related: [INDEX](INDEX.md), [Course Overview](Course%20Overview.md), [Lecture 01](Lectures/2026-10-05%20Lecture%2001%20-%20Systems%20of%20Linear%20Equations.md)
