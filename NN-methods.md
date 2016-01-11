# Nearest-Neighbor Methods

## 2.4 Statistical Decision Theory
__Loss function__: $$L(Y,f(X))$$  
From loss function, we decide a f(x) solution, which is the minimum point.

##Squared Error Loss##
$$L_2(Y,f(X)) = (Y −f(X))^2$$   
This leads us to a criterion for choosing f,  
$$EPE(f) = E(Y − f(X))^2$$  
$$\int[y-f(x)]^2Pr(dx, dy)$$  
The solution is  
$$f (x) = E(Y |X = x)$$  

## Absolute Error Loss
$$L_1(Y, f(X)) = E|Y −f(X)|$$  
The solution is  
$$f (x) = median(Y |X = x)$$  


As $$N, k \to \infty$$ such that $$k/N \to 0$$, $$\hat{f}(x) \to E(Y|X = x)$$  
Seems we have a universal approximator.  

