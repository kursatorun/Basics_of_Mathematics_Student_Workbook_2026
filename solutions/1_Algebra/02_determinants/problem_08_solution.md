
## Exercise 8 — Solution

Given:

$$
\det(A)=3,\qquad \det(B)=-5
$$

We need to calculate det(AB), det(BA), and det(A⁻¹B).

**Step 1: Calculate det(AB)**

We use the product property:

$$
\det(AB)=\det(A)\cdot\det(B)
$$

$$
=3\cdot(-5)
$$

$$
\boxed{\det(AB)=-15}
$$

**Step 2: Calculate det(BA)**

Using the same property:

$$
\det(BA)=\det(B)\cdot\det(A)
$$

$$
=(-5)\cdot3
$$

$$
\boxed{\det(BA)=-15}
$$

**Step 3: Calculate det(A⁻¹B)**

Since det(A) = 3 is not zero, A is invertible.

For an inverse matrix:

$$
\det(A^{-1})=\frac{1}{\det(A)}
$$

Therefore:

$$
\det(A^{-1}B)=\det(A^{-1})\cdot\det(B)
$$

$$
=\frac{1}{3}\cdot(-5)
$$

$$
\boxed{\det(A^{-1}B)=-\frac{5}{3}}
$$

**Step 4: Explanation**

Even though matrix multiplication is generally not commutative (AB ≠ BA), their determinants are equal because multiplication of numbers is commutative.

$$
\det(A)\det(B)=\det(B)\det(A)
$$

**Conclusion:**

$$
\det(AB)=-15
$$

$$
\det(BA)=-15
$$

$$
\det(A^{-1}B)=-\frac{5}{3}
$$
