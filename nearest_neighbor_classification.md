# Non-parametric method

###k-NN method
##### Vote
$$\hat{Y} = \frac{1}{k}\sum_{x_i \in N_k(x)}y_i$$ Where :
* $$\hat{Y}$$: prediction of the output.
* $$N_k(x)$$ : the neighborhood of x defined by the k closest points $$x_i$$ in the training sample.
* $$y_i$$ coded as 0 for BLUE and 1 for ORANGE

##### Classify
$$ \hat{G}=
\begin{cases}
ORANGE&\text{  if } \hat{Y}>0.5\\
BLUE&\text{ if }\hat{Y}<0.5
\end{cases}
$$



* The error on the **training data** should be approximate an increasing function of k, and will always be 0 for k = 1

---

### statistical learning theory


