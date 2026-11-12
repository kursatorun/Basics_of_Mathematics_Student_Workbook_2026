# Problem 5 — Matrix Times Vector

## Problem Statement

We are given:

$$
A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix},
\qquad
x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

We need to compute $Ax$. Then we need to write the result as a linear combination of the columns of $A$, using the entries of $x$ as coefficients.

## Theoretical Background and Concepts

To multiply a matrix by a vector, we multiply each row of the matrix by the vector and add the matching products.

We can also look at this using columns. Each entry of the vector multiplies the corresponding column of the matrix, and then we add these column vectors. This is called a linear combination.

## Detailed Step-by-Step Solution

### Step 1 — Compute Ax using rows

$$
Ax =
\begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}
\begin{pmatrix} 4 \\ 2 \end{pmatrix}
=
\begin{pmatrix}
2\cdot4 + (-1)\cdot2 \\
1\cdot4 + 3\cdot2
\end{pmatrix}
$$

The first entry is:

$$
2\cdot4 + (-1)\cdot2 = 8 - 2 = 6
$$

The second entry is:

$$
1\cdot4 + 3\cdot2 = 4 + 6 = 10
$$

So the answer is:

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

### Step 2 — Write Ax as a linear combination of columns

The columns of $A$ are:

$$
a_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix},
\qquad
a_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

The entries of $x$ are 4 and 2, so we multiply the first column by 4 and the second column by 2:

$$
Ax = 4a_1 + 2a_2
$$

$$
Ax =
4\begin{pmatrix} 2 \\ 1 \end{pmatrix}
+
2\begin{pmatrix} -1 \\ 3 \end{pmatrix}
=
\begin{pmatrix} 8 \\ 4 \end{pmatrix}
+
\begin{pmatrix} -2 \\ 6 \end{pmatrix}
=
\begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

This means $Ax$ is 4 times the first column plus 2 times the second column of $A$.

## Verification and Consistency Checks

- The multiplication is defined because $A$ has 2 columns and $x$ has 2
