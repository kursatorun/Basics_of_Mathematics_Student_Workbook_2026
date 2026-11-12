# Problem 7 — Identity Matrix, Zero Matrix, and Powers

## Problem Statement

We are given:

$$
A = \begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

We need to compute $AI$, $IA$, $A+0$, $A^2$, and $A^3$. We also need to explain the roles of the identity matrix and the zero matrix, and describe the pattern in the powers of $A$.

## Theoretical Background and Concepts

For this problem, the identity matrix and the zero matrix are:

$$
I = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix},
\qquad
0 = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
$$

Multiplying a matrix by the identity matrix leaves it unchanged. Adding the zero matrix also leaves it unchanged.

Matrix powers mean repeated matrix multiplication:

$$
A^2 = AA,
\qquad
A^3 = A^2 A
$$

This is not the same as taking the power of each entry separately.

## Detailed Step-by-Step Solution

### Step 1 — Compute AI and IA

$$
AI =
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
=
\begin{pmatrix}
2\cdot1+1\cdot0 & 2\cdot0+1\cdot1 \\
0\cdot1+2\cdot0 & 0\cdot0+2\cdot1
\end{pmatrix}
=
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

$$
IA =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
=
\begin{pmatrix}
1\cdot2+0\cdot0 & 1\cdot1+0\cdot2 \\
0\cdot2+1\cdot0 & 0\cdot1+1\cdot2
\end{pmatrix}
=
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

So $AI=IA=A$. The identity matrix is the neutral element for matrix multiplication, just like 1 for ordinary numbers.

### Step 2 — Compute A plus the zero matrix

We add the entries in the same positions:

$$
A+0 =
\begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0
\end{pmatrix}
=
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

The zero matrix is the neutral element for matrix addition, just like 0 for ordinary numbers.

### Step 3 — Compute A squared

We multiply $A$ by itself, using rows and columns:

$$
A^2 =
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

$$
A^2 =
\begin{pmatrix}
2\cdot2+1\cdot0 & 2\cdot1+1\cdot2 \\
0\cdot2+2\cdot0 & 0\cdot1+2\cdot2
\end{pmatrix}
=
\begin{pmatrix}
4 & 4 \\
0 & 4
\end{pmatrix}
$$

### Step 4 — Compute A cubed

We multiply $A^2$ by $A$:

$$
A^3 =
\begin{pmatrix}
4 & 4 \\
0 & 4
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

$$
A^3 =
\begin{pmatrix}
4\cdot2+4\cdot0 & 4\cdot1+4\cdot2 \\
0\cdot2+4\cdot0 & 0\cdot1+4\cdot2
\end{pmatrix}
=
\begin{pmatrix}
8 & 12 \\
0 & 8
\end{pmatrix}
$$

### Step 5 — Describe the pattern

The first three powers are:

$$
A = \begin{pmatrix}2 & 1 \\ 0 & 2\end{pmatrix},
\qquad
A^2 = \begin{pmatrix}4 & 4 \\ 0 & 4\end{pmatrix},
\qquad
A^3 = \begin{pmatrix}8 & 12 \\ 0 & 8\end{pmatrix}
$$

The diagonal entries are 2, 4, and 8, so they follow the powers of 2. The bottom-left entry stays zero.

The top-right entries are 1, 4, and 12. These fit the pattern:

$$
1=1\cdot2^0,
\qquad
4=2\cdot2^1,
\qquad
12=3\cdot2^2
$$

The general pattern is:

$$
A^n =
\begin{pmatrix}
2^n & n2^{n-1} \\
0 & 2^n
\end{pmatrix},
\qquad n\geq1
$$

We can see why the pattern continues by multiplying this form by $A$. The new diagonal entries become $2^{n+1}$, and the top-right entry becomes:

$$
2^n\cdot1 + n2^{n-1}\cdot2
= 2^n+n2^n
= (n+1)2^n
$$

The bottom-left entry stays zero, so the next power has the same form.

## Verification and Consistency Checks

- All the matrices are $2\times2$, so the addition
