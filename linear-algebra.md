# Linear Algebra Review

## Positive Semidefinite Matrices

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

Mean $$\mu = \Bbb{E}X$$, covariance $$\Sigma = [(X-\mu)(X-\mu)^T]$$

__Fact__ $$\Sigma$$ is PSD

__Proof__

(i) $$\Sigma$$ is symmetric

$$\Sigma _{ij} = cov(X_i, X_j) = cov(X_j, X_i) = \Sigma _{ij}$$







