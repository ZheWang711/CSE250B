# Generative model classification

* **Parametrized**: Classifiers with a **fixed** number of *parameters* can represent a **limited** set of functions.
    * Generative: model individual classes
    * Discriminative: mode the decision boundary between the classes


#### Summation rule

* $$A_1, ... A_k$$ are disjoint events ( non-overlap )
* For any other evenr $$E$$: $$P(E) = P(E, A_1)+P(E,A_2)+...+P(E, A_k)$$

#### Generative models

* Unknown distribution $$X*Y$$, generating a point $$(x, y)$$:
    * choose y then choose x given y
    * $$P(y=j|x) = \frac{P(y=j)*P(x|y=j)}{P(x)} = \frac{\pi_jP_j(x)}{\sum_{i=1}^k \pi_iP_i(x)}$$
    * bayes-optimal prediction: $$h^*(x)=argmax_j(\pi_jP_j(x))$$


