# Linear Algebra Review

## 1. Positive Semidefinite Matrices

### a. Definition
A real symmetric $$p \times p$$ matrix M is positive semidefinie (P.S.D) if

$$Z^TMZ \geq 0 \quad \forall Z \in \Bbb{R}^p$$

It is positive definite (P.D.) if 

$$Z^TMZ > 0 \quad  \forall \quad nonzero \quad Z$$

$$P.D. \subset P.S.D. \subset \text{symmetric matrix} \subset \text{square matrix}$$

__Ex__

PSD or not?

(1)
$$\begin{pmatrix}
1 & 1\\
1 & 1\\
\end{pmatrix}$$

$$\begin{pmatrix}
z_1 & z_2\\
\end{pmatrix}$$
$$\begin{pmatrix}
1 & 1 \\
1 & 1\\
\end{pmatrix}$$
$$\begin{pmatrix}
z_1 \\ z_2\\
\end{pmatrix}$$
=
$$z_1^2 + z_2^2 + 2z_1z_2 \geq 0$$

Is PSD

Note: $$Z^TMZ = \sum_{ij} M_{ij}Z_iZ_j$$

(2)
$$\begin{pmatrix}
1 & 2\\
2 & 1\\
\end{pmatrix}$$

$$\begin{pmatrix}
z_1 & z_2\\
\end{pmatrix}$$
$$\begin{pmatrix}
1 & 2 \\
2 & 1 \\
\end{pmatrix}$$
$$\begin{pmatrix}
z_1 \\ z_2\\
\end{pmatrix}$$
=
$$z_1^2 + z_2^2 + 4z_1z_2 < 0 \text{ if } Z_2 = -Z_1$$

### b. Diagonal matrices

A diagonal matrix is P.S.D $$\Leftrightarrow$$ its entries are $$\geq 0$$

### c. M + N
If M, N are of the same size and PSD, then M+N is PSD

M+N is also symmetric

$$Z^T(M+N)Z = Z^TMZ + Z^TNZ \geq 0$$

### d. Covariance matrices
Let $$X \in \Bbb{R}^p$$ be a random variable.

Mean $$\mu = \Bbb{E}X$$, covariance $$\Sigma = \Bbb{E}[(X-\mu)(X-\mu)^T]$$

__Fact__ $$\Sigma$$ is PSD

__Proof__

(i) $$\Sigma$$ is symmetric

$$\Sigma _{ij} = cov(X_i, X_j) = cov(X_j, X_i) = \Sigma _{ij}$$

(ii) Pick any $$Z \in \Bbb{R}^p$$

$$Z^T\Sigma Z = Z^T \Bbb{E}[(X-\mu)(X-\mu)^T] Z$$

$$= \Bbb{E}[Z^T(X-\mu)(X-\mu)^TZ]$$

$$= \Bbb{E}[(Z^T(X-\mu))(Z^T(X-\mu))^T]$$ where $$Z^T(X-\mu)$$ is a number

$$= \Bbb{E}[(Z^T(X-\mu))^2] \geq 0$$

## 2. Eigenvalues and eigenvectors

### a. Definition
A $$p \times p$$ matrix M has eigenvalue $$\lambda$$, if there is some $$\mu \in \Bbb{R}^p \quad s.t \quad M\mu = \lambda \mu$$

This $$\mu$$ is called the eigenvector corresponding to $$\lambda$$

Real symmetric matrix ==> guaranteed eigenvalue $$\lambda$$ is a real number.



### b.
__Fact__ Let M be any real symmetric $$p \times p$$ matrix

(i) M has p real eigenvalues $$\lambda_1, \cdots, \lambda_p$$ (not necessarily distinct)

(ii) There is a set of p corresponding eigenvectors $$\mu_1, \cdots, \mu_p$$ that form an orthogonal basis of $$\Bbb{R}^p$$, i.e.,

$$||\mu_i|| = 1 \quad \forall i$$

$$\mu_i \mu_j = 0  \quad i\neq j$$

### c. Ex

What are the eigenvalues and eigenvectors of

(1) 
$$\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}$$

$$\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}$$
$$\begin{pmatrix}
x \\
y \\
\end{pmatrix}$$
$$=
\lambda
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
$$

$$2x = \lambda x$$

$$y = \lambda y$$

$$e1 =\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}
$$, eigenvalue 2

$$e2 =\begin{pmatrix}
0 \\
1 \\
\end{pmatrix}
$$, eigenvalue 1

(2)
$$\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}$$

$$e1 =\frac {1} {\sqrt{2}} \begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
$$, eigenvalue 1

$$e2 =\frac {1} {\sqrt{2}} \begin{pmatrix}
1 \\
-1 \\
\end{pmatrix}
$$, eigenvalue -1

### d. Remark

A $$p \times p$$ matrix M represents a linear transformation given by $$x \mapsto Mx$$

This transformation is completely determined by its behavior on any p linearly independent vectors (because all other vectors are linear combinations of these)

If M has eigenvalue $$\lambda _i$$ and orthogonal eigenvectors $$\mu_i$$ and $$N\mu_i = \lambda_i\mu_i \forall i$$ then $$N = M$$

### e.
__Fact__ Let M be a symmetric $$p \times p$$ matrix with eigenvalues $$\lambda_i$$ and orthogonal eigenvectors $$\mu_i$$, then "spectral decomposition"

(i)
$$M = \begin{pmatrix}
| & | & & |\\
\mu_1 & \mu_2 & \cdots & \mu_p \\
| & | & & |\\
\end{pmatrix}
\begin{pmatrix}
 \lambda_1  & \cdots  & 0\\
 \vdots  & \ddots & \vdots \\
 0 &\cdots & \lambda_p
 \\
\end{pmatrix}
\begin{pmatrix}
- & \mu_1^T & - \\
- & \mu_2^T & - \\
  & \vdots  &   \\
- & \mu_p^T & - \\
\end{pmatrix}
$$

(ii)

$$M = \lambda_1\mu_1\mu_1^T + \lambda_2\mu_2\mu_2^T + \cdots + \lambda_p\mu_p\mu_p^T$$

Check (i)

$$\begin{pmatrix}
| & | & & |\\
\mu_1 & \mu_2 & \cdots & \mu_p \\
| & | & & |\\
\end{pmatrix}

\underbrace{
\begin{pmatrix}
 \lambda_1  & \cdots  & 0\\
 \vdots  & \ddots & \vdots \\
 0 &\cdots & \lambda_p
 \\
\end{pmatrix}

\underbrace{
\begin{pmatrix}
- & \mu_1^T & - \\
- & \mu_2^T & - \\
  & \vdots  &   \\
- & \mu_p^T & - \\
\end{pmatrix}
\begin{pmatrix}
| \\
\mu_1\\
| \\
\end{pmatrix}
}_{\begin{pmatrix}1\\0\\\vdots\\0\\\end{pmatrix}}

}_{\begin{pmatrix}\lambda_1\\0\\\vdots\\0\\\end{pmatrix}}
$$

$$(\lambda_1\mu_1\mu_1^T + \cdots + \lambda_p \mu_p \mu_p^T)\mu_i = (\lambda_i \mu_i \mu_i^T \mu_i) = \lambda_i \mu_i$$

__Ex__

A $$2 \times 2$$ matrix N has eigenvalue-eigenvector pairs

1, $$\frac 1 {\sqrt{2}}\begin{pmatrix}
1\\
1\\
\end{pmatrix}$$

2, $$\frac 1 {\sqrt{2}}\begin{pmatrix}
1\\
-1\\
\end{pmatrix}$$

What is N?

$$N = \frac 1 2 \begin{pmatrix}
1 & 1\\
1 & -1
\end{pmatrix}
\begin{pmatrix}
1 & 0\\
0 & 2
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
1 & -1
\end{pmatrix}
$$

## 3. Which matrices are PSD?

### (a)
__Fact__ Let M $$\in \Bbb{R}^{p \times p}$$ be a real symmetric matrix

(i) M is P.S.D. $$\Leftrightarrow$$ all its eigenvalues $$\lambda_i$$ are $$\geq 0$$

(ii) M is P.D. $$\Leftrightarrow$$ all $$\lambda_i > 0$$

__Proof__

Let's do (i), the other is similar

$$\Rightarrow$$ Say M is P.S.D

$$\therefore$$ $$\mu_i^T M \mu_i \geq 0$$

By spectral decomposition

$$\mu_i^T M \mu_i = \mu_i^T (\lambda_1 \mu_1 \mu_1^T + \cdots + \lambda_p \mu_p \mu_p^T) \mu_i = \mu_i ^T (\lambda_i \mu_i) = \lambda_i ||\mu_i||^2 = \lambda_i$$

$$\lambda_i \geq 0$$

$$\Leftarrow$$ Say all $$\lambda_i \geq 0$$

Pick any $$Z \in \Bbb{R} ^p$$

We'll show $$Z^T M Z \geq 0$$

$$Z^T M Z = Z^T (\lambda_1 \mu_1 \mu_1^T + \cdots + \lambda_p \mu_p \mu_p^T)Z = \sum_{i=1}^{p} \lambda_i (Z^T \mu_i)(\mu_i^T Z) $$
$$= \sum_{i=1}^{p} \lambda_i (Z \cdot \mu_i)^2 \geq 0$$

### (b) Any form of $$VV^T$$ is $$P.S.D.$$

* Symmetric: $$(VV^T)^T = VV^T$$
* $$z^TVV^Tz = (z^TV)(z^TV)^T = (z^TV)^2$$ since $$z^TV$$ is a real number


## 4. Projection and basis change
### a. Projection
What is the projection of a vector $$x \in \Bbb{R}^p$$ onto direction $$\mu$$? ($$||\mu|| = 1$$)

Dot product $$x\cdot\mu$$

### b. Plane
What is the projection of x onto the plane defined by direction $$\mu_1$$, $$\mu_2$$ that are orthogonal to each other?

$$||\mu_1|| = ||\mu_2|| = 1$$, $$\mu_1 \cdot \mu_2 = 0$$

$$(x \cdot \mu_1, x \cdot \mu_2)$$

### c.
Let $$\mu_1, \cdots , \mu_p$$ be an orthogonal basis of $$\Bbb{R}^p$$, i.e., $$\mu_i \cdot \mu_j = \begin{cases}1 \quad if \quad i = j\\
0 \quad i \neq j \\ 
\end{cases}$$

Write $$x \in \Bbb{R}^p$$ in this basis:

$$\begin{pmatrix}
x \cdot \mu_1 \\
x \cdot \mu_2 \\
\vdots \\
x \cdot \mu_p \\
\end{pmatrix}
= 
\underbrace{
\begin{pmatrix}
- & \mu_1^T & - \\
- & \mu_2^T & - \\
& \vdots & \\
- & \mu_p^T & - \\
\end{pmatrix}
}_{Q^T}
\begin{pmatrix}
| \\ 
x \\
| \\
\end{pmatrix}
$$

$$Q^TQ = I$$ ; $$QQ^T = I$$

$$Q$$ is orthogonal

### d.
__Ex__
Write $$(x,y) \in \Bbb{R}^2$$ in the basis $$\frac 1 {\sqrt2}\begin{pmatrix}1\\1\\\end{pmatrix}$$, $$\frac 1 {\sqrt2}\begin{pmatrix}1\\-1\\\end{pmatrix}$$

$$(x,y) \mapsto \frac 1 {\sqrt2} \begin{pmatrix} x+y\\x-y\\ \end{pmatrix}$$

## 5. Multivariate Gaussian
### a.
$$N(\mu, \Sigma)$$ in $$\Bbb{R}^p$$, Mean $$\mu \in \Bbb{R}^p$$, Covariance $$\Sigma \in \Bbb{R}^{p\times p}$$

Density $$p(x) = \frac {1} {(2\pi)^{p/2}|\Sigma|^{1/2}} exp(-\frac{1}{2} (x-\mu)^T\Sigma^{-1}(x-\mu))$$

### b. Easy case
(i) Spherical $$\Sigma = \sigma^2 I$$

(ii) Diagonal $$\Sigma = diag(\lambda_1, \cdots, \lambda_p)$$

(iii) General $$\Sigma$$

Write $$\Sigma = \begin{pmatrix}
| & | & & |\\
\mu_1 & \mu_2 & \cdots & \mu_p \\
| & | & & |\\
\end{pmatrix}
\begin{pmatrix}
 \lambda_1  & \cdots  & 0\\
 \vdots  & \ddots & \vdots \\
 0 &\cdots & \lambda_p
 \\
\end{pmatrix}
\begin{pmatrix}
- & \mu_1^T & - \\
- & \mu_2^T & - \\
  & \vdots  &   \\
- & \mu_p^T & - \\
\end{pmatrix}
$$

(I) $$|\Sigma| = \lambda_1 \cdots \lambda_p$$

(II) What is $$\Sigma^{-1}$$

$$(Q \Lambda Q^T)(Q \Lambda^{-1} Q^T) $$

$$= Q \Lambda Q^TQ \Lambda^{-1}Q^T = Q \Lambda \Lambda^{-1} Q^T = QQ^T = I$$

(III) Contours of equal density

$$(x-\mu)^T \Sigma^{-1} (x-\mu) = c$$

$$\Leftrightarrow$$ $$(X^T\Sigma^{-1}X) = c$$

$$\Leftrightarrow$$ $$(X^TQ) \Sigma^{-1}(Q^TX) = c$$

$$\Leftrightarrow$$ $$Z^T \Sigma^{-1}Z = c$$

