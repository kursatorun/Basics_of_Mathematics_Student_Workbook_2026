
## Exercise 5 — Solution

Given matrix:

$$
A=\begin{pmatrix}
1&2&3\\
2&1&0\\
-1&4&2
\end{pmatrix}
$$

**Step 1: Apply the first row operation**

$$
R_2\leftarrow R_2-2R_1
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&-3&-6\\
-1&4&2
\end{pmatrix}
$$

This operation does not change the determinant.

**Step 2: Apply the second row operation**

$$
R_3\leftarrow R_3+R_1
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&-3&-6\\
0&6&5
\end{pmatrix}
$$

This operation also does not change the determinant.

**Step 3: Apply the third row operation**

$$
R_3\leftarrow R_3+2R_2
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&-3&-6\\
0&0&-7
\end{pmatrix}
$$

This operation also preserves the determinant.

**Step 4: Calculate the determinant**

The matrix is now upper triangular.

We multiply the diagonal elements:

$$
\det(A)=1\cdot(-3)\cdot(-7)
$$

$$
\boxed{\det(A)=21}
$$

**Conclusion:**

The determinant is **21**.

All three operations were row replacements, so the determinant did not change during the calculations.
