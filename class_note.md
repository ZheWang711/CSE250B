# class note

### Feb 9

* Supported vector machine

By multiply w and b by a constant, once $$wx+b>0$$, it can be larger than any positive number.

let the margin distance between $$wx+b=0$$ and $$wx+b=1$$ is $$\gamma$$,
move point $$z$$ on $$wx+b=1$$ by $$\gamma$$ units towards the direction over $$-w$$, it would be in plane $$wx+b=0$$, thus $$\gamma = 1 / |w|$$


$$\frac{1}{2} ||w||^2$$ is convex function, since its second derivative is identity matrix!

For convex optimazation problem, dual problem has same solution (optimal value) with the original problem, although they seems completely different.

Most of the weights $$\alpha$$ is zero, the weight is not zero iff $$y^i(w*x^i + b) = 1$$ ??

For convex optimazation, learn ECE273.


* Iris data set:
    * w is 2d
    * b is only a number
* What if the data is not linearly separable?
    * If we just run the precepton -> never converge
    * Introduce a slack variable for each point
    * For each point that is not correctly classified, use a little slack
    * maximize the margin in the mean while minimize the sum of the slack
    * $$0 <= \alpha_i <= C$$, not a single point can contribute too much!
    * C: the trade off of minimizing slack and maximizing $$\gamma$$
    * All the not separable data are going to be in supported vectors
---


