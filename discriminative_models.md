# Discriminative Models

## 1. A closer look at $$L(W)$$

### a. Loss function for Logistic Regression

$$L(W) = \sum_{i=1}^{n} ln(1+e^{-y^{(i)}(w\cdot x^{(i)})})$$

To minimize, just set derivative to zero,right?

### b.
There are p partial derivatives

$$\frac {\partial L} {\partial w_1}$$, $$\cdots$$, $$\frac {\partial L} {\partial w_p}$$

Assemble into a vector:

$$\triangledown L(W) = (\frac {\partial L} {\partial w_1}, \cdots, \frac {\partial L} {\partial w_p})$$

$$\frac {\partial{L}} {\partial{w_j}} = \sum _{i=1} ^n \frac {e^{-y^{(i)}(w \cdot x^{(i)})}} {1 + e^{-y^{(i)}(w \cdot x^{(i)})}} (-y^{(i)}x_j^{(i)})$$

$$= - \sum _{i=1} ^n y^{(i)} x_j ^{(i)} \frac 1 {1 + e^{y^{(i)}(w \cdot x^{(i)})}}$$
Thus:

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

$$H_{jk} = \frac {\partial^2 f} {\partial Z_j \partial z_k}$$ $$(\triangledown^2 f)$$

Then
- H is symmetric
- f  is convex $$\Leftrightarrow H(Z)$$ is PSD $$\forall z \in \Bbb{R}^p$$

### c. Logistic Regression
$$L(W) = \sum_{i=1}^{n} ln(1+e^{-y^{(i)}(w\cdot x^{(i)})})$$

$$\frac {\partial L} {\partial w_j} = - \sum_{i=1}^n y^{(i)} x_j^{(i)} \frac {1} {1 + e^{y^{(i)} (w \cdot x_j^{(i)})}}$$

$$\frac {\partial^2 L} {\partial w_k \partial w_j} = \sum_{i=1}^n x_j^{(i)} x_k^{(i)} \frac 1 {1 + e^{w\cdot x^{(i)}}} \frac 1 {1 + e^{-w \cdot x^{(i)}}}$$

Suppose we can find vectors $$v_1, \cdots, v_p$$ such that:

$$\frac {\partial^2 L} {\partial w_j \partial w_k} = v_j \cdot v_k$$

Then the Hessian is PSD

Define $$v_1, \cdots, v_p \in \Bbb{R}^n$$ as follows.

$$V_{ji} = X_j^{(i)} \sqrt{\frac 1 {(1+e^{w \cdot x^{(i)}}) (1+e^{-w \cdot x^{(i)}})}}$$

Notice $$H_{jk} = \frac {\partial^2 L} {\partial w_j \partial w_k} = v_j\cdot v_k$$

$$\Rightarrow H = 
\begin{pmatrix}
- &v_1& -\\
&\vdots& \\
-&v_p&- \\
\end{pmatrix}
\begin{pmatrix}
| & & |\\
v_1 &\dots&v_p\\
| & & |\\
\end{pmatrix}
$$

$$\Rightarrow$$ $$H$$ is PSD

__Fact:__ Any matrix of the form $$VV^T$$ is PSD

Check

(1) Symmetric: $$(VV^T)^T = VV^T$$

(2) For any $$Z \in \Bbb{R}^p$$

$$Z^TVV^TZ = (Z^TV)(V^TZ) = (V^TZ)^T(V^TZ) = ||V^TZ||^2 \geq 0$$

## 3. Gradient Descent

### a.
$$W_0 = 0$$, $$t = 0$$

While $$\triangledown L(W_t) \not\approx 0:$$

$$\quad W_{t+1} = W_t - \eta _t \triangledown L(W_t)$$

$$\quad t = t+ 1$$

$$\eta _t$$ is the step size at time $$t$$

### b. Rationale

(i) "Differentiable" $$\equiv$$ "locally linear"

(ii) For small displacements $$U \in \Bbb{R}^p$$

$$L(W+U) \approx L(W) + U \cdot \triangledown L(W)$$

If $$U = - \eta \triangledown L(W)$$

$$L(W+U) \approx L(W) - \eta ||\triangledown L(W)||^2 < L(W)$$

$$\eta $$ not too small and not too large.

### c. Logistic Regression

$$\triangledown L(W) = - \sum y^{(i)} x ^{(i)} Pr_w(-y^{(i)} | x ^ {(i)})$$

Valid only in a small neighbourhood

$$W_{t+1} = W_t + \eta _t - \sum _{i=1}^n y^{(i)} x ^{(i)} Pr_w(-y^{(i)} | x ^ {(i)})$$

## 4. Newton-Raphson

### a. 
Unconstrained minimization again

$$w_0 = 0$$, $$t = 0$$

While $$\triangledown L(w_t) \not\approx 0$$:

$$\quad w_{t+1} = w_t - \eta _t H^{-1} (w_t) \triangledown L(w_t)$$


### b. Rationale
(i) Second-order Taylor expansion

For small u,

$$L(w+u) \approx L(w) + u \cdot \triangledown L(w)$$

$$\quad \quad \quad \quad \quad \quad \quad \quad+ \frac 1 2 u^T H(w) u$$

(ii) What is the minimum of this quadratic approximation?

Set derivative to zero



