# Feb 11 -- Kernel

## review
* Can we kernelize everything?
    * Algorithm only does data with dot product
    * ... (slides)


* Primal form: represent the data in actual space
* Dual form: represent in combination data form


## Kernalize SVM
* It seems that we can do kernelize on primal form
* can do kernel trick on dual form

* input:
    * matrix of dot product $$\phi(x^{(i)})*\phi(x^{(j)})$$
    * labels: $$y$$

## Polynomial decision boundries

* $$p^d$$ terms.
* kernel trick: $$\phi(x)\phi(z) = (1+x*z)^d$$
* kernel function: think it as some measure of similarity
* SVM do not require data to be separable, because the boundry $$C$$
* In general , solution of SVM is unique (independent with order of data), in perception is not (depend on the order).


## How to deal with data that cannot represented by vector

Embed the sequence into some same uniquious space (infinite dimensions).

Substring: a sequence of words (e.g. "Hello", "Hello World")
Infinitely many coordinates.(at most $$n^2$$ no zero)

Support vector ==> weighted vote by similarity ==> like "prototype selection in NN".

* to check whether a similarity function is OK ==> check if all the egenivales of matrix $$K$$ are >= 0.

* $$UU^T = K$$, where ith row of U is $$\phi(x_i)$$


