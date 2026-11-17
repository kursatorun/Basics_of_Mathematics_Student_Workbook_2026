
## Exercise 2 — Solution

Given matrix:

$$
A=\begin{pmatrix}
1&2&-1\\
0&3&4\\
2&1&5
\end{pmatrix}
$$

**Step 1: Using Sarrus' rule**

Positive diagonals:

$$
1\cdot3\cdot5+2\cdot4\cdot2+(-1)\cdot0\cdot1
$$

$$
=15+16+0=31
$$

Negative diagonals:

$$
(-1)\cdot3\cdot2+2\cdot0\cdot5+1\cdot4\cdot1
$$

$$
=-6+0+4=-2
$$

Now subtract:

$$
\det(A)=31-(-2)
$$

$$
\boxed{\det(A)=33}
$$

**Step 2: Verification using row operations**

First:

$$
R_3\leftarrow R_3-2R_1
$$

$$
\begin{pmatrix}
1&2&-1\\
0&3&4\\
0&-3&7
\end{pmatrix}
$$

Then:

$$
R_3\leftarrow R_3+R_2
$$

$$
\begin{pmatrix}
1&2&-1\\
0&3&4\\
0&0&11
\end{pmatrix}
$$

These row operations do not change the determinant.

The matrix is now upper triangular, so:

$$
\det(A)=1\cdot3\cdot11=33
$$

**Conclusion:**

The determinant is **33**. Both methods give the same result.
