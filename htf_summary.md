# HTF summary

## 1 Introduction

### Example 1: Email Spam
Objective: To design an automatic spam detector that
could filter out spam before clogging the users’ mailboxes.

*Supervised Learning* problem, *Classification* problem

### Example 2: Prostate Cancer
Objective: predict the log of PSA (lpsa) from a number of measurements including log cancer volume (lcavol), log prostate weight lweight, age, log of benign prostatic hyperplasia amount lbph, seminal vesicle invasion svi, log of capsular penetration lcp, Gleason score gleason, and percent of Gleason scores 4 or 5 pgg45

*Supervised Learning* problem, *Regression* problem

### Example 3: Handwritten Digit Recognition
Objective: predict, from the 16 × 16 matrix of pixel
intensities, the identity of each image (0, 1, . . . , 9) quickly and accurately.

*Supervised Learning* problem, *Classification* problem

### Example 4: DNA Expression Microarrays
*Supervised Learning* problem, *Regression* problem, with two categorical predictor variables—genes and samples—with the response variable being the level of expression.

*Unsupervised* learning problem. For example, for question (a) above, we think of the samples as points in 6830–dimensional space, which we want to cluster together in some way.

## 2 Overview of Supervised Learning
### 2.1 Introduction
* Supervised Learning: Using *inputs*, which is measured or featured to predict the value of *outputs*
* *Inputs* are also called *predictors*, *independent values*, *features*
* *Outputs* are also called *responses*, *dependent variables*

### 2.2 Variable Types and Terminology
#### Output type:
* Quantitative: in Regression problems
* Qualitative/Categorical/Discrete/factors: in Classification problems

#### Input type:
* Quantitative
* Qualitative

#### Notations:
* X: Input, generic

X $$ =
\begin{pmatrix}
X_1\\
X_2\\
...\\
X_j\\
...\\
X_n
\end{pmatrix}
$$

* Y: Quantitative Output, generic
* G: Qualitative Output, generic

$$ G = \{G_1, G_2,...,G_j,...G_n \}$$

* x: Obversed
* **X**: Matrices

**X** $$ = 
\begin{pmatrix}
x_1^T\\
x_2^T\\
...\\
x_j^T\\
...\\
x_N^T
\end{pmatrix}
$$

### 2.3 Two Simple Approaches to Prediction: Least Squares and Nearest Neighbors
#### 2.3.1 Linear Models and Least Squares
$$ Inputs: X^T = \{X_1, X_2,..., X_p\}$$

$$ Predict: \hat{Y} = \hat{\beta_0} + \Sigma_{j=1}^{p}X_j\hat{\beta_j}=X^T\hat{\beta_0}$$

$$ Residual\ Sum\ of\ Squares\ RSS(\beta) = \Sigma_{i=1}^{N}(y_i-x_i^T\beta)^2=(y-X\beta)^T(y-X\beta)$$

To minimize RRS: $$\frac{\partial{RRS(\beta)}}{\partial{\beta}}=0\Rightarrow X^T(y-X\beta)=0\Rightarrow X^TX\hat{\beta}=X^Ty$$

For Quantitative Output: $$ \hat{y_i}=x_i^T \hat{\beta} $$

For Qualitative Output: $$ \hat{g_i}=
\begin{cases}
label1&\quad \hat{y_i}>0.5\\
label2&\quad \hat{y_i}<0.5
\end{cases}
$$

#### 2.3.2 Nearest-Neighbor Methods
