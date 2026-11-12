# Problem 3 — When Can Matrices Be Multiplied?

## Problem Statement

The matrix sizes are:

$$
A_{2\times3}, \qquad B_{3\times4}, \qquad C_{4\times2}, \qquad D_{2\times2}
$$

We need to check whether the products below are defined. If a product is defined, we also need to find its size and explain why.

$$
AB,\quad BA,\quad BC,\quad CB,\quad AC,\quad CA,\quad AD,\quad DA
$$

## Theoretical Background and Concepts

We can multiply two matrices when the number of columns of the first matrix equals the number of rows of the second matrix.

In short, the inside numbers must match. The outside numbers give the size of the answer:

$$
(m\times n)(n\times p)\longrightarrow m\times p
$$

## Detailed Step-by-Step Solution

### 1. AB

$$
(2\times3)(3\times4)
$$

The inside numbers are both 3, so the product is defined. The result has size $2\times4$.

### 2. BA

$$
(3\times4)(2\times3)
$$

The inside numbers are 4 and 2. They do not match, so the product is undefined.

### 3. BC

$$
(3\times4)(4\times2)
$$

The inside numbers are both 4, so the product is defined. The result has size $3\times2$.

### 4. CB

$$
(4\times2)(3\times4)
$$

The inside numbers are 2 and 3. They do not match, so the product is undefined.

### 5. AC

$$
(2\times3)(4\times2)
$$

The inside numbers are 3 and 4. They do not match, so the product is undefined.

### 6. CA

$$
(4\times2)(2\times3)
$$

The inside numbers are both 2, so the product is defined. The result has size $4\times3$.

### 7. AD

$$
(2\times3)(2\times2)
$$

The inside numbers are 3 and 2. They do not match, so the product is undefined.

### 8. DA

$$
(2\times2)(2\times3)
$$

The inside numbers are both 2, so the product is defined. The result has size $2\times3$.

## Verification and Consistency Checks

I checked the inside numbers again for each product. They match for $AB$, $BC$, $CA$, and $DA$, but not for the other four products.

For the defined products, I also checked the outside numbers:

- $AB$: 2 rows and 4 columns.
- $BC$: 3 rows and 2 columns.
- $CA$: 4 rows and 3 columns.
- $DA$: 2 rows and 3 columns.

Also, $AB$ is defined but $BA$ is not. This shows that we need to check each order separately.
