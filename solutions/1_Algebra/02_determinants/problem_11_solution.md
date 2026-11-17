
## Exercise 11 — Solution

Given matrix:

$$
A=\begin{pmatrix}
1&2&3\\
1&3&4\\
1&4&6
\end{pmatrix}
$$

**Step 1: Create zeros in the first column**

Apply the row operations:

$$
R_2\leftarrow R_2-R_1
$$

$$
R_3\leftarrow R_3-R_1
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&2&3
\end{pmatrix}
$$

Both operations preserve the determinant.

**Step 2: Create another zero**

Apply:

$$
R_3\leftarrow R_3-2R_2
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&0&1
\end{pmatrix}
$$

This operation also preserves the determinant.

**Step 3: Calculate the determinant**

The matrix is now upper triangular.

For a triangular matrix, the determinant is the product of its diagonal elements.

$$
\det(A)=1\cdot1\cdot1
$$

$$
\boxed{\det(A)=1}
$$

**Conclusion:**

The determinant is **1**.

All row operations used were of the form:

$$
R_i\leftarrow R_i+cR_j,\quad i\neq j
$$

These operations do not change the determinant.
