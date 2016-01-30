# Multivariate Gaussian

## Univariate Gaussian
$$var(x) = \Bbb{E}(X - \mu)^2 = \Bbb{E}(X^2) - \mu^2,  where \mu = \Bbb{E}(X)$$

$$std(X) = \sqrt{var(X)}$$

$$cov(X, Y) = \Bbb{E}[(X-\mu_{x})(Y-\mu_{y})] = \Bbb{E}[XY] - \mu_{x}\mu_{y}$$

The Univariate Gaussian

$$N(\mu, \sigma^2)$$
$$p(x) = \frac{1} {(2\pi\sigma^2)^{1/2}} exp(- \frac{(x-\mu)^2} {2\sigma^2})$$

## Multivariate Gaussian

$$N(\mu, \Sigma)$$ Gaussian in $$\Bbb{R}^p$$

Density $$p(x) = \frac {1} {(2\pi)^{p/2}|\Sigma|^{1/2}} exp(-\frac{1}{2} (x-\mu)^T\Sigma^{-1}(x-\mu))$$

$$\Sigma_{ij} = \Sigma_{ji} = cov(X_{i}, Y_{j})$$ if $$i \neq j$$

$$\Sigma_{ii} = var(X_{i})$$

In matrix / vector form: $$\mu = \Bbb{E}X$$ and $$\Sigma = \Bbb{E}(X- \mu)(X - \mu)^T$$



