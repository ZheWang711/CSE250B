# Nearest-Neighbor Methods

## 2.4 Statistical Decision Theory
__Loss function__: $$L(Y,f(X))$$  
__Squared error loss__: $$L(Y,f(X)) = (Y −f(X))^2$$  
This leads us to a criterion for choosing f,  
$$EPE(f) = E(Y − f(X))^2$$  
$$\int[y-f(x)]^2Pr(dx, dy)$$  

From loss function, we decide a f(x) solution.  

As $$N, k \to \infty$$ such that $$k/N \to 0$$, $$\hat{f}(x) \to E(Y|X = x)$$  
Seems we have a universal approximator.  

