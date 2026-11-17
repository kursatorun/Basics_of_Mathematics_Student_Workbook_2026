
## Exercise 13 — Solution

Given matrix:

$$
A=\begin{pmatrix}
1&2&3\\
2&5&7\\
1&0&2
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
0&1&1\\
1&0&2
\end{pmatrix}
$$

This operation does not change the determinant.

**Step 2: Apply the second row operation**

$$
R_3\leftarrow R_3-R_1
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&-2&-1
\end{pmatrix}
$$

This operation also preserves the determinant.

**Step 3: Apply the third row operation**

$$
R_3\leftarrow R_3+2R_2
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&0&1
\end{pmatrix}
$$

This operation also does not change the determinant.

**Step 4: Calculate the determinant**

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

All three row operations preserve the determinant because we only added multiples of one row to another row. No row swaps or row scaling were used.
