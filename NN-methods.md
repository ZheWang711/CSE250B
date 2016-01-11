# Nearest-Neighbor Methods

## 2.4 Statistical Decision Theory
__Loss function__: $$L(Y,f(X))$$  
From loss function, we decide a f(x) solution, which is the minimum point.

##Squared Error Loss##

### start here hehehe
###

The solution is  
$$f (x) = E(Y |X = x)$$  
$$\hat{f} (x) = Ave(y_i|x_i ∈ N_k(x))$$

As $$N, k \to \infty$$ such that $$k/N \to 0$$, $$\hat{f}(x) \to E(Y|X = x)$$  
Seems we have a universal approximator.  

## Absolute Error Loss
$$L_1(Y, f(X)) = E|Y −f(X)|$$  
$$EPE (f) = E(L_1(Y, f(x))) = E|Y - f(X)|$$  

The solution is  
$$\hat{f} (x) = median(Y |X = x)$$  

## Output is Categorical Variable G
* An estimate $$\hat{G}$$ will assume values in $$G$$, the set of possible classes.
* Our loss function can be represented by a $$K × K$$      matrix $$L$$, where $$K = card(G)$$. $$L$$ will be zero on the diagonal and nonnegative elsewhere, where $$L(k,l)$$ is the price paid for classifying an observation belonging to class $$G_k$$ as $$G_l$$.

$$EPE = E[L (G, \hat{G} (X))]$$  
$$EPE = E_X \sum_{k=1}^{K} L[G_k, \hat{G} (X)]Pr(G_k|X)$$  
$$\hat{G} (X) = G_k if Pr(G_k|X = x) = max Pr(g|X = x).$$  
This is known as the __Bayes classifier__, and says that we classify to the most probable class, using the conditional distribution $$Pr(G|X)$$  
The error rate of the __Bayes classifier__ is called the __Bayes rate__. 