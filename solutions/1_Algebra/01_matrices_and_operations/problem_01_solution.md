# Problem 1 — Matrix Size and Entries

## Problem Statement

We are given two matrices:

$$
A = \begin{pmatrix} 2 & -1 & 3 \\ 0 & 4 & 5 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{pmatrix}
$$

We need to:
1. State the sizes of matrices $A$ and $B$.
2. Find the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Theoretical Background and Concepts

Matrix size is written as rows $\times$ columns.
In the index notation $a_{ij}$, the first index $i$ tells us which row to look at, and the second index $j$ tells us which column.
A row vector is taken horizontally from left to right, and a column vector is taken vertically from top to bottom.

## Detailed Step-by-Step Solution

### Step 1 — Matrix sizes
- Matrix $A$ has 2 horizontal rows and 3 vertical columns, so its size is $2 \times 3$.
- Matrix $B$ has 3 horizontal rows and 2 vertical columns, so its size is $3 \times 2$.

### Step 2 — Finding the entries
- $a_{12}$: Go to row 1, column 2 of matrix $A \rightarrow -1$.
- $a_{23}$: Go to row 2, column 3 of matrix $A \rightarrow 5$.
- $b_{21}$: Go to row 2, column 1 of matrix $B \rightarrow -2$.
- $b_{32}$: Go to row 3, column 2 of matrix $B \rightarrow 1$.

### Step 3 — Writing the vectors
The second row of $A$ is:

$$
\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}
$$

The first column of $B$ is:

$$
\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}
$$

## Verification and Consistency Checks

- Matrix $A$ has 6 total entries ($2 \cdot 3 = 6$), and matrix $B$ has 6 total entries ($3 \cdot 2 = 6$). This matches what is written in the problem.
- A row of $A$ must have 3 numbers because $A$ has 3 columns, and our row vector has 3 numbers.
- A column of $B$ must have 3 numbers because $B$ has 3 rows, and our column vector has 3 numbers.
- The positions match the given matrices directly.
