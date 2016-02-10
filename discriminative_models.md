# Discriminative Models

## 1. A closer look at $$L(W)$$

### a. Loss function for Logistic Regression

$$L(W) = \sum_{i=1}^{n} ln(1+e^{-y^{(i)}(w\cdot x^{(i)})})$$

To minimize, just set derivative to zero,right?

### b.
There are p partial derivatives

$$\frac {\partial L} {\partial w_1}$$, $$\cdots$$, $$\frac {\partial L} {\partial w_p}$$

Assemble into a vector:

$$\triangledown L = (\frac {\partial L} {\partial w_1}, \cdots, \frac {\partial L} {\partial w_p})$$

$$\triangledown L(W) = - \sum_{i=1}^n y^{(i)} x^{(i)} \frac {1} {1 + e^{y^{(i)} (w \cdot x^{(i)})}}$$

### c.
In general,

$$\triangledown L(W) = 0 \Leftrightarrow w$$ is a local optimum.
Plus L(W) is convex, local opt $$\Leftrightarrow$$ global opt.

## 2. Convexity

### a.

__Def:__ A function $$f: \Bbb{R}^p \to \Bbb{R}$$ is convex if for all $$a, b \in \Bbb{R}^p$$, and all $$0 \leq \theta \leq 1$$, the following:

$$f(\theta a + (1-\theta)b) \leq \theta f(a) + (1-\theta)f(b)$$

f ins concave $$\Leftrightarrow$$ -f is convex.

### b. Testing Convexity
Suppose $$f: \Bbb{R}^p \to \Bbb{R}$$ is twice differentiable.

i.e. the second partial derivatives $$\frac {\partial^2 f} {\partial x_i \partial x_j}$$ exist everywhere, suppose moreover that these are continuous.

For any $$Z \in \Bbb{R}^p$$, the Hessian $$H(Z)$$ is the matrix of second derivatives of $$Z$$:

$$H_jk = \frac {\partial^2 f} {\partial Z_j \partial z_k}$$


