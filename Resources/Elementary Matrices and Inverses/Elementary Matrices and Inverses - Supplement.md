---
title: "Elementary Matrices and Inverses - Supplement"
date: 2026-10-08
course: MAT216
type: supplementary
status: class-coverage-unconfirmed
tags: [mat216, supplementary, elementary-matrices, inverse]
aliases: [Elementary Matrices Supplement]
---

# Elementary Matrices and Inverses — Supplement

> [!abstract] Summary
> A row operation can be represented by multiplying on the left by an elementary matrix. Undoing the row operation gives its inverse. This note explains the later pages of the instructor handout; it does not mark these topics as completed in class.

Source: [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=4|Main handout, PDF pages 4–8]].

## 1. From a row operation to a matrix

> [!note] Elementary matrix
> An elementary matrix is obtained by performing **one elementary row operation** on an identity matrix. If $A$ has $m$ rows, use $I_m$. Multiplying $EA$ applies that same operation to $A$.

For $R_2\leftarrow R_2-3R_1$, apply the operation to $I_3$:

$$
E_{21}=\begin{bmatrix}1&0&0\\-3&1&0\\0&0&1\end{bmatrix}.
$$

With the matrix from Lecture 02,

$$
A=\begin{bmatrix}1&2&1\\3&8&1\\0&4&1\end{bmatrix},\qquad
b=\begin{bmatrix}2\\12\\2\end{bmatrix},
$$

we obtain

$$
E_{21}A=\begin{bmatrix}1&2&1\\0&2&-2\\0&4&1\end{bmatrix},\qquad
E_{21}b=\begin{bmatrix}2\\6\\2\end{bmatrix}.
$$

> [!tip] The right-hand side changes too
> Treat elimination as $E[A\mid b]=[EA\mid Eb]$. Applying it only to the coefficient matrix changes the system incorrectly.

## 2. Several operations: multiplication order

The next operation is $R_3\leftarrow R_3-2R_2$:

$$
E_{32}=\begin{bmatrix}1&0&0\\0&1&0\\0&-2&1\end{bmatrix}.
$$

Since $E_{21}$ acts first,

$$
U=E_{32}E_{21}A
=\begin{bmatrix}1&2&1\\0&2&-2\\0&0&5\end{bmatrix}.
$$

The combined elimination matrix and transformed constants are

$$
E=E_{32}E_{21}=\begin{bmatrix}1&0&0\\-3&1&0\\6&-2&1\end{bmatrix},\qquad
c=Eb=\begin{bmatrix}2\\6\\-10\end{bmatrix}.
$$

Thus $Ax=b$ becomes $Ux=c$, whose solution is $(2,1,-2)$.

> [!warning] One operation versus a product
> $E_{21}$ and $E_{32}$ are elementary matrices. Their product $E$ represents a sequence of operations and need not itself be elementary. The handout uses “elementary matrix” more broadly for this product.

## 3. Undoing the operation

To undo $R_2\leftarrow R_2-3R_1$, use $R_2\leftarrow R_2+3R_1$:

$$
E_{21}^{-1}=\begin{bmatrix}1&0&0\\3&1&0\\0&0&1\end{bmatrix}.
$$

Both multiplication orders give the identity:

$$
E_{21}^{-1}E_{21}=I_3,\qquad E_{21}E_{21}^{-1}=I_3.
$$

| Row operation | Inverse operation |
|---|---|
| $R_i\leftarrow R_i+kR_j$, $i\ne j$ | $R_i\leftarrow R_i-kR_j$ |
| $R_i\leftarrow kR_i$, $k\ne0$ | $R_i\leftarrow\frac1kR_i$ |
| $R_i\leftrightarrow R_j$ | Swap the same rows again |

> [!warning] Do not negate an entire matrix
> The sign reversal applies only to the multiplier in a row replacement. An arbitrary inverse is not obtained by changing matrix-entry signs.

## 4. Inverse of a product

Undo the last operation first:

$$
(E_{32}E_{21})^{-1}=E_{21}^{-1}E_{32}^{-1}.
$$

For this example,

$$
E^{-1}=\begin{bmatrix}1&0&0\\3&1&0\\0&2&1\end{bmatrix},\qquad E^{-1}U=A.
$$

> [!note] Invertibility
> A square matrix $A$ is invertible if a matrix $A^{-1}$ exists such that $A^{-1}A=AA^{-1}=I$. Here $E^{-1}$ undoes elimination; it is **not** the inverse of $A$.

## Possible exam concept questions

- [ ] How do you construct the elementary matrix for a given row operation?
- [ ] Why do row operations correspond to multiplication on the left?
- [ ] If $E_1$ acts before $E_2$, is the result $E_1E_2A$ or $E_2E_1A$?
- [ ] How do you undo row scaling, row swapping, and row replacement?
- [ ] Why does reversing a product require reversing the order?

> [!question]- Check the multiplication-order answer
> The result is $E_2(E_1A)=E_2E_1A$. To undo it, apply $E_2^{-1}$ first, then $E_1^{-1}$, giving $(E_2E_1)^{-1}=E_1^{-1}E_2^{-1}$.

## Open items

- [ ] Confirm the class date or lecture covering elementary matrices and inverses before assigning a lecture number.

---

**Related:** [[Gaussian Elimination - Teacher Materials|Teacher materials]] · [[2026-10-07 Lecture 02 - Gaussian Elimination and Back Substitution|Lecture 02]] · [[Formula Sheet]] · [[Course Overview]] · [[INDEX]]
