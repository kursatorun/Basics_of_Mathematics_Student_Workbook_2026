# Problem 6 — Transpose

## Problem Statement

We are given:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix},
\qquad
B = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
$$

We need to compute $A^T$, $B^T$, and $AB$. Then we need to check that:

$$
(AB)^T = B^T A^T
$$

## Theoretical Background and Concepts

The transpose of a matrix is made by turning its rows into columns. For example, the first row of $A$ becomes the first column of $A^T$.

When we transpose a product, the order of the matrices is reversed:

$$
(AB)^T = B^T A^T
$$

We will check this by calculating both sides separately.

## Detailed Step-by-Step Solution

### Step 1 — Find the transposes

The rows of $A$ become the columns of $A^T$:

$$
A^T = \begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
$$

The rows of $B$ become the columns of $B^T$:

$$
B^T = \begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
$$

### Step 2 — Compute AB

$A$ has size $2\times3$ and $B$ has size $3\times2$. The inside dimensions match, so we can multiply them. The result has size $2\times2$.

We multiply each row of $A$ by each column of $B$:

$$
AB = \begin{pmatrix}
1\cdot1 + 2\cdot2 + 3\cdot(-1) &
1\cdot0 + 2\cdot1 + 3\cdot3 \\
4\cdot1 + 5\cdot2 + 6\cdot(-1) &
4\cdot0 + 5\cdot1 + 6\cdot3
\end{pmatrix}
$$

$$
AB = \begin{pmatrix}
1+4-3 & 0+2+9 \\
4+10-6 & 0+5+18
\end{pmatrix}
=
\begin{pmatrix}
2 & 11 \\
8 & 23
\end{pmatrix}
$$

### Step 3 — Find the transpose of AB

We turn the rows of $AB$ into columns:

$$
(AB)^T = \begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

### Step 4 — Compute B transpose times A transpose

Now we calculate the other side separately:

$$
B^T A^T =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
$$

$$
B^T A^T =
\begin{pmatrix}
1\cdot1 + 2\cdot2 + (-1)\cdot3 &
1\cdot4 + 2\cdot5 + (-1)\cdot6 \\
0\cdot1 + 1\cdot2 + 3\cdot3 &
0\cdot4 + 1\cdot5 + 3\cdot6
\end{pmatrix}
$$

$$
B^T A^T =
\begin{pmatrix}
1+4-3 & 4+10-6 \\
0+2+9 & 0+5+18
\end{pmatrix}
=
\begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

## Verification and Consistency Checks

Both calculations give exactly the same matrix:

$$
(AB)^T =
\begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
= B^T A^T
$$

So the transpose property is verified for these matrices.

The sizes also match:
- $A$ is $2\times3$, so $A^T$ is $3\times2$.
- $B$ is $3\times2$, so $B^T$ is $2\times3$.
- Both $(AB)^T$ and $B^T A^T$ are $2\times2$.

A common mistake would be to write $A^T B^T$ instead. The order must be reversed. Here, $A^T B^T$ would have size $3\times3$, so it could not equal our $2\times2$ result.
