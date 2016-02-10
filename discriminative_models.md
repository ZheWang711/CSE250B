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



