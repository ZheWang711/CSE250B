# homework1

| vector |  $$\Sigma = \{x_1, x_2, ... x_n \}$$ Then $$\Sigma^m = \{x_{i_1}x_{i_2}... x_{i_m} | x_{i_j} \in \Sigma\} $$ |
| -- | -- |
| 0:2 | 1:2 |

## CNN (Condensed Nearest Neighbour)

* Divide the training set data into 3 types:
    * **Outliers**: points which would not be recognized as the correct types if added to the database later.
    * **Prototypes**: minimum set of points required in the training set for all the other non-outlier points to be correctly recognised.
    * **Absorbed points**: points which are not outliers and would be corrected recognised based just on the set of prototype points.


* New samples only need to be compared with prototype points

* CNN Algorithm
    1. remove ourlier: check if it is recognised as the correct class or not (after removing it from the training data)
    2. make a new database called prototype
    3. pick any point from the original set, see if it is recognized as the correct class based on the points in the new database:
        * Correct: it is an absorbed point
        * Incorrect: remove from the original set, and add to the 


