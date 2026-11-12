# Problem 9 — Composing Transformations

## Problem Statement

We are given:

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix},
\qquad
R = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix},
\qquad
x = \begin{pmatrix}
1 \\
2
\end{pmatrix}
$$

The matrix $S$ stretches the horizontal coordinate by a factor of 2 and leaves the vertical coordinate unchanged. The matrix $R$ rotates a vector by 90 degrees counterclockwise.

We need to compute $RSx$ and $SRx$, compare the results, and explain geometrically why the order matters.

## Theoretical Background and Concepts

When applying a product of matrices to a vector, the rightmost matrix acts first:

$$
RSx = R(Sx),
\qquad
SRx = S(Rx)
$$

For a general vector, these transformations work as follows:

$$
S\begin{pmatrix}a\\b\end{pmatrix}
=
\begin{pmatrix}2a\\b\end{pmatrix}
$$

$$
R\begin{pmatrix}a\\b\end{pmatrix}
=
\begin{pmatrix}-b\\a\end{pmatrix}
$$

So $S$ doubles the horizontal coordinate, while $R$ turns the vector 90 degrees counterclockwise.

## Detailed Step-by-Step Solution

### Step 1 — Compute RSx

First, apply $S$ to $x$:

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
2\cdot1+0\cdot2 \\
0\cdot1+1\cdot2
\end{pmatrix}
=
\begin{pmatrix}
2 \\
2
\end{pmatrix}
$$

Next, apply $R$ to this result:

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
0\cdot2+(-1)\cdot2 \\
1\cdot2+0\cdot2
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2
\end{pmatrix}
$$

### Step 2 — Compute SRx

First, apply $R$ to $x$:

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
0\cdot1+(-1)\cdot2 \\
1\cdot1+0\cdot2
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
1
\end{pmatrix}
$$

Next, apply $S$ to this result:

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
2\cdot(-2)+0\cdot1 \\
0\cdot(-2)+1\cdot1
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1
\end{pmatrix}
$$

### Step 3 — Compare and explain geometrically

The results are different:

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
= SRx
$$

For $RSx$, the point first moves from $(1,2)$ to $(2,2)$ because of the horizontal stretch. Rotating it then gives $(-2,2)$.

For $SRx$, the point first rotates from $(1,2)$ to $(-2,1)$. The horizontal stretch then gives $(-4,1)$.

The order matters because $S$ stretches only horizontally, not equally in all directions. Rotating changes which part of the vector lies in the horizontal direction, so stretching before or after the rotation produces different results.

## Verification and Consistency Checks

We can check the answers by calculating the matrix products first:

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
\end{pmatrix}
$$

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
\end{pmatrix}
$$

Similarly:

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
\end{pmatrix}
$$

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
\end{pmatrix}
$$

These match the step-by-step results. Both answers are $2\times1$ vectors, as expected.

A common mistake is applying the leftmost matrix first. In $RSx$, we must apply $S$ first, then $R$.
