# Linear Algebra Review

## 1. Positive Semidefinite Matrices

### a. Definition
A real symmetric $$p \times p$$ matrix M is positive semidefinie (P.S.D) if

$$Z^TMZ \geq 0 \quad \forall Z \in \Bbb{R}^p$$

It is positive definite (P.D.) if 

$$Z^TMZ > 0 \quad  \forall \quad nonzero \quad Z$$

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
$$z_1^2 + z_2^2 + 4z_1z_2 < 0 if Z_2 = Z_1$$

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

$$= \Bbb{E}[Z \cdot (X-\mu) (X-\mu) \cdot Z]$$

$$= \Bbb{E}[((X-\mu) \cdot Z)^2] \geq 0$$

## 2. Eigenvalues and eigenvectors

### a. Definition
A $$p \times p$$ matrix M has eigenvalue $$\lambda$$, if there is some $$\mu \in \Bbb{R}^p \quad s.t \quad M\mu = \lambda \mu$$

This $$\mu$$ is called the eigenvector corresponding to $$\lambda$$

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




