
## Exercise 15 — Solution

Given two invertible 2×2 matrices:

$$
\det(A)=-2,\qquad \det(B)=3
$$

We need to calculate:

$$
\det(B^{-1}A^TB)
$$

**Step 1: Use the product property**

The determinant of a product is the product of the determinants.

$$
\det(XYZ)=\det(X)\det(Y)\det(Z)
$$

Therefore:

$$
\det(B^{-1}A^TB)=\det(B^{-1})\det(A^T)\det(B)
$$

**Step 2: Use the inverse property**

The determinant of an inverse matrix is:

$$
\det(B^{-1})=\frac{1}{\det(B)}
$$

Since det(B) = 3:

$$
\det(B^{-1})=\frac13
$$

**Step 3: Use the transpose property**

The determinant of a transpose is equal to the determinant of the original matrix.

$$
\det(A^T)=\det(A)
$$

Therefore:

$$
\det(A^T)=-2
$$

**Step 4: Substitute the values**

$$
\det(B^{-1}A^TB)=\frac13\cdot(-2)\cdot3
$$

$$
=\frac{-6}{3}
$$

$$
\boxed{\det(B^{-1}A^TB)=-2}
$$

**Step 5: Explain the cancellation**

The factors involving B cancel because:

$$
\det(B^{-1})\det(B)=\frac13\cdot3=1
$$

So we get:

$$
\det(B^{-1}A^TB)=\det(A^T)=\det(A)
$$

**Conclusion:**

$$
\boxed{\det(B^{-1}A^TB)=-2}
$$

The final answer is **-2**. We used the product, inverse, and transpose properties without calculating the matrix entries.
