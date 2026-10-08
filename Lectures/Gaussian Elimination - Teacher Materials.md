---
title: "Gaussian Elimination - Teacher Materials"
date: 2026-10-08
course: MAT216
type: teacher-materials
related_lecture: 2
tags: [mat216, teacher-materials, gaussian-elimination]
aliases: [Gaussian Elimination Handouts]
---

# Gaussian Elimination — Teacher Materials

> [!abstract] Summary
> A reading guide to the three PDFs supplied by the instructor. Use these alongside [[2026-10-07 Lecture 02 - Gaussian Elimination and Back Substitution|Lecture 02]], then work through [[Gaussian Elimination - Worked Examples and Practice|the practice note]].

## 1. Start here

| Order | Material | What to do |
|---|---|---|
| 1 | [[2026-10-07 Lecture 02 - Gaussian Elimination and Back Substitution|Lecture 02]] | Review row operations, pivots, free variables, and back substitution. |
| 2 | [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf|Main handout]] | Compare the instructor's method with the class notes. |
| 3 | [[Additional Examples of Gaussian Elimination.pdf|Additional examples]] | Follow two worked problems: an infinite family and a four-variable unique solution. |
| 4 | [[Practice Problems of Gaussian Elimination.pdf|Practice sheet]] | Attempt all three questions before checking answers. |
| 5 | [[Elementary Matrices and Inverses - Supplement|Elementary matrices and inverses]] | Read the later part of the main handout as supplementary material. |

## 2. Main handout: page guide

Page links below use the **PDF viewer's page number**, not the printed footer.

| PDF page | Printed page | Content |
|---|---|---|
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=1|1]] | 1 | System, augmented matrix, coefficient matrix |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=2|2]] | 3 | Pivot positions, pivot columns, elimination setup |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=3|3]] | 4 | Clearing entries below pivots |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=4|4]] | 5 | Back substitution, normalising pivots, elementary matrices intro |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=5|5]] | 6 | Constructing elimination matrices from the identity |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=6|6]] | 7 | Product of elimination matrices; inverse motivation |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=7|7]] | 8 | Undoing a row replacement |
| [[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=8|8]] | 9 | Two-sided inverse identities |

> [!todo] Check the source upload
> This PDF contains eight pages, with printed footers 1, 3, 4, …, 9. Printed page 2 is absent. Check whether the instructor uploaded a separate page or a fuller version; no missing content has been reconstructed.

### Preview

![[Solving Systems of Linear Equations - Gaussian Elimination and Back Substitution.pdf#page=1]]

## 3. Clarifications when reading

> [!warning] Pivot-column typo
> On PDF page 2, the displayed matrix has pivots in **columns 1, 2, and 4**. The text says columns 1, 2, and 5. Read the positions from the matrix.

> [!note] Pivots need not already equal 1
> Gaussian elimination may leave nonzero pivots such as 1, 2, and 5. Scaling them to 1 is useful and matches the class-note procedure, but back substitution also works before normalisation. The handout uses both presentations.

> [!warning] Inverse rule has a limited scope
> Changing the sign of the row-addition multiplier undoes a **row replacement**. It is not a general rule for inverting matrices. Scaling is undone by the reciprocal; swapping is undone by swapping again.

The handout's main worked system and solution $(2,1,-2)$ already appear in Lecture 02. The supplementary note explains the elementary-matrix extension without repeating the full lecture.

## Possible exam concept questions

- [ ] How does an augmented matrix differ from a coefficient matrix?
- [ ] Can a pivot be nonzero but unequal to 1?
- [ ] How do you distinguish a zero row from a contradictory row?
- [ ] Why must a row operation also change the right-hand side?

## Open items

- [ ] Confirm whether printed page 2 is available.
- [ ] Confirm when elementary matrices and inverses are covered in class; they are currently supplementary.

---

**Related:** [[INDEX]] · [[Course Overview]] · [[Formula Sheet]] · [[Gaussian Elimination - Worked Examples and Practice|Worked examples and practice]] · [[Elementary Matrices and Inverses - Supplement|Supplement]]
