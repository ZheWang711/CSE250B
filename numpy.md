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
    
    ```
