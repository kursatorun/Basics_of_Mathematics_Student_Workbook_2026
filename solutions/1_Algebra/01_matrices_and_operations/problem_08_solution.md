# Problem 8 — Row Operations and Their Reversibility

## Problem Statement

We are given:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
$$

We need to perform these row operations in order:

$$
R_2 \leftarrow R_2 - 2R_1
$$

$$
R_3 \leftarrow R_3 + R_1
$$

$$
R_2 \leftrightarrow R_3
$$

We need to write the matrix after each step and give an operation that reverses each step.

## Theoretical Background and Concepts

A row operation changes the specified row while leaving the other rows unchanged. When adding or subtracting rows, we work with entries in the same column.

These operations can be reversed:
- Subtracting a multiple of another row is reversed by adding that same multiple.
- Adding a row is reversed by subtracting it.
- Swapping two rows is reversed by swapping them again.

We use the current matrix at each step, not the original matrix every time.

## Detailed Step-by-Step Solution

### Step 1 — Subtract twice row 1 from row 2

$$
R_2 \leftarrow R_2 - 2R_1
$$

The new second row is:

$$
(2,4,1)-2(1,2,-1)
=
(2-2,\ 4-4,\ 1+2)
=
(0,0,3)
$$

The first and third rows stay unchanged:

$$
A_1 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3
\end{pmatrix}
$$

To reverse this step, add twice row 1 back to row 2:

$$
R_2 \leftarrow R_2 + 2R_1
$$

### Step 2 — Add row 1 to row 3

Starting from $A_1$, we perform:

$$
R_3 \leftarrow R_3 + R_1
$$

The new third row is:

$$
(-1,1,3)+(1,2,-1)
=
(0,3,2)
$$

The first and second rows stay unchanged:

$$
A_2 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2
\end{pmatrix}
$$

To reverse this step, subtract row 1 from row 3:

$$
R_3 \leftarrow R_3 - R_1
$$

### Step 3 — Swap rows 2 and 3

$$
R_2 \leftrightarrow R_3
$$

The second and third rows exchange places:

$$
A_3 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3
\end{pmatrix}
$$

To reverse this step, swap the same rows again:

$$
R_2 \leftrightarrow R_3
$$

## Verification and Consistency Checks

To undo the whole process, we must reverse the operations in the opposite order.

First, swapping rows 2 and 3 of $A_3$ gives $A_2$ again.

Next, subtracting row 1 from row 3 gives:

$$
(0,3,2)-(1,2,-1)=(-1,1,3)
$$

This brings us back to $A_1$.

Finally, adding twice row 1 to row 2 gives:

$$
(0,0,3)+2(1,2,-1)=(2,4,1)
$$

We recover the original matrix:

$$
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
=A
$$

All the matrices remain $3\times3$, and row 1 stays unchanged throughout the process.

One sign to watch is in the first step: the last entry of row 2 becomes $1-2(-1)=3$, not $-1$.
