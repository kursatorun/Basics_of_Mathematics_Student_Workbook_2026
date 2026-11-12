# Problem 7 — Identity Matrix, Zero Matrix, and Powers

## Problem Statement

We have the matrix:

$$
A=\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

We need to find $AI$, $IA$, $A+0$, $A^2$, and $A^3$. We also need to explain the identity matrix, zero matrix, and the pattern in the powers of $A$.

## Theoretical Background and Concepts

The identity matrix $I$ works like 1. When we multiply a matrix by $I$, it stays the same.

The zero matrix works like 0. Adding it to a matrix does not change anything.

For powers, we multiply the matrix by itself.

## Detailed Step-by-Step Solution

### Step 1 — Find AI and IA

$$
I=\begin{pmatrix}1&0\\0&1\end{pmatrix}
$$

$$
AI=
\begin{pmatrix}2&1\\0&2\end{pmatrix}
\begin{pmatrix}1&0\\0&1\end{pmatrix}
=
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

$$
IA=
\begin{pmatrix}1&0\\0&1\end{pmatrix}
\begin{pmatrix}2&1\\0&2\end{pmatrix}
=
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

So $AI=IA=A$.

### Step 2 — Find A + 0

$$
A+0=
\begin{pmatrix}2&1\\0&2\end{pmatrix}
+
\begin{pmatrix}0&0\\0&0\end{pmatrix}
=
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

So $A+0=A$.

### Step 3 — Find A²

$$
A^2=A\cdot A
$$

$$
A^2=
\begin{pmatrix}2&1\\0&2\end{pmatrix}
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

Calculate:

- $2(2)+1(0)=4$
- $2(1)+1(2)=4$
- $0(2)+2(0)=0$
- $0(1)+2(2)=4$

$$
A^2=\begin{pmatrix}4&4\\0&4\end{pmatrix}
$$

### Step 4 — Find A³

$$
A^3=A^2\cdot A
$$

$$
A^3=
\begin{pmatrix}4&4\\0&4\end{pmatrix}
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

Calculate:

- $4(2)+4(0)=8$
- $4(1)+4(2)=12$
- $0(2)+4(0)=0$
- $0(1)+4(2)=8$

$$
A^3=\begin{pmatrix}8&12\\0&8\end{pmatrix}
$$

### Step 5 — Explain the pattern

We have:

$$
A=\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

$$
A^2=\begin{pmatrix}4&4\\0&4\end{pmatrix}
$$

$$
A^3=\begin{pmatrix}8&12\\0&8\end{pmatrix}
$$

I can
