# Problem 9 — Composing Transformations

## Problem Statement

We are given the matrices

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix},
\qquad
R = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

and the vector

$$
x = \begin{pmatrix}
1 \\
2
\end{pmatrix}.
$$

The matrix $S$ describes a nonuniform scaling, and $R$ describes a 90-degree counterclockwise rotation. We need to compute $RSx$ and $SRx$, compare the results, and explain why the order matters.

## Theoretical Background and Concepts

In a product of matrices applied to a vector, the matrix closest to the vector acts first:

$$
RSx = R(Sx),
\qquad
SRx = S(Rx).
$$

For a vector with coordinates $(a,b)$, the transformations are

$$
S\begin{pmatrix}
a \\
b
\end{pmatrix}
=
\begin{pmatrix}
2a \\
b
\end{pmatrix},
\qquad
R\begin{pmatrix}
a \\
b
\end{pmatrix}
=
\begin{pmatrix}
-b \\
a
\end{pmatrix}.
$$

So $S$ doubles the horizontal coordinate, while $R$ rotates the vector 90 degrees counterclockwise.

## Detailed Step-by-Step Solution

### Step 1 — Compute $RSx$

First apply $S$ to $x$:

$$
Sx =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix}
=
\begin{pmatrix}
2 \\
2
\end{pmatrix}.
$$

Then apply $R$:

$$
RSx =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
2 \\
2
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2
\end{pmatrix}.
$$

### Step 2 — Compute $SRx$

First apply $R$ to $x$:

$$
Rx =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
1
\end{pmatrix}.
$$

Then apply $S$:

$$
SRx =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-2 \\
1
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1
\end{pmatrix}.
$$

### Step 3 — Compare the results

$$
RSx =
\begin{pmatrix}
-2 \\
2
\end{pmatrix}
\ne
\begin{pmatrix}
-4 \\
1
\end{pmatrix}
= SRx.
$$

For $RSx$, we stretch the vector first, then rotate it. For $SRx$, we rotate it first, then stretch it. Since $S$ stretches horizontally but not vertically, changing the order changes the result.

## Verification and Consistency Checks

We can also multiply the matrices first:

$$
RS =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
=
\begin{pmatrix}
0 & -1 \\
2 & 0
\end{pmatrix}.
$$

Then

$$
(RS)x =
\begin{pmatrix}
0 & -1 \\
2 & 0
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2
\end{pmatrix}.
$$

Similarly,

$$
SR =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
=
\begin{pmatrix}
0 & -2 \\
1 & 0
\end{pmatrix}.
$$

Therefore,

$$
(SR)x =
\begin{pmatrix}
0 & -2 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1
\end{pmatrix}.
$$

These results match the step-by-step calculations. Both final answers are $2\times1$ vectors, as expected.
