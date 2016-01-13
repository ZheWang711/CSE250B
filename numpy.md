# numPy

* Concepts
    * main object: homogeneous multidimensional array.
    * **axes**: dimensions.
    * ```numpy.array``` is also called ```ndarray```
    * 


* Attribute (```ndarray.XXX```)
    * ```ndlm```: the number of axes(dimensions) if the array.
    * `shape`: a tuple of integers indicating the size of the array in each dimension.
    * `size` total number of elements of the array
    * `itemsize` size in bytes of each element of the array
    * `dtype` an object describing the type of the elements in the array

* Creation
    * import 
    ```python
    import numpy as np
    ```

    * create an array: `array()`, `zeros()`, `ones()`, `empty()`, `arrange()`, `linspace()`.
    ```python
    A = np.array([1,2,3])   # from python list
    B1 = np.array([[1,2],[3,4]])
    
    B2 = np.array([[1,3],[3,4]])    # create from nested list
    
    zeros = np.zeros( (3,4) )   # 3*4 matrix with all elements 0
    ones = np.zeros( (3,4) )    # 3*4 matrix with all elements 1
    unintialized = np.empty( (3,4) )    # 3*4 matrix with all elements uninitialized
    
    np.arange(0, 2, 0.3)    # (start, end, step), in this case array([ 0. ,  0.3,  0.6,  0.9,  1.2,  1.5,  1.8])
    
    np.linspace(0, 2, 9)    # 9 numbers from 0 to 2 (inclusive) in this case array([ 0.0, 0.25, 0.5,..., 2.])
    ```
    
* [Linear Algebra ](http://docs.scipy.org/doc/numpy-1.10.0/reference/routines.linalg.html)`(numpy.linalg)`
    * `dot(a, b)`: dot peoduct of two arrays
    * `linalg.matrix_power(M, n)`: raise a square matrix to the power n
    * `linalg.det(a)`: compute the determinant of an array.
    * `linalg.solve(a, b)`: Solve a linear matrix equation, or system of linear scalar equations
    * `linalg.inv(a)`: compute the (multiplicative) inverse of a matrix
    


