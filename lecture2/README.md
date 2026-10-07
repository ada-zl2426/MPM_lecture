# lecture2

Learning numpy basics

1)  import numpy as np -> import numpy library and rename it as np
2)  a = np.array([0, 1, 2]) -> create numpy array [0, 1, 2]
3)  b = np.array(a) -> copy numpy array, a to b
4)  ndarray is a data type -> All numpy arrays are type: ndarray
5)  np.arange(start, stop, step) -> create a numpy array with numbers of fixed step size
    - Note: np.arange(5) == np.arange(0, 5, 1)
    - Note: stop is not included
6)  np.linspace(start, stop, n.o points) -> creates evenly spaced numbers between a start and end value
    - Note: stop is included
7)  np.zeros(n) -> create an array with n zeros
8)  np.ones(n) -> create an array with n ones
9)  np.ones(n) -> create a n x n identity matrix
10) a.ndim -> output the number of dimensions of array a
11) a.shape -> output the number of element in each dimension
12) a.dtype -> output the data type of the element inside the array
13) a.size -> output the numner of elements in the array
14) pprint -> pretty print is used to display array in a neater format
15) mat = np.array(alist, complex) -> used to display elements in complex format
16) a[1, 0, 1] -> access elements in the array
17) c[1, 0, ...] -> ... means include remaining dimensions
18) slice(start, stop, step) -> to extract elements from array
19) a = np.array([-2, 6, 2]), b = a -> means assigning 2 names to a single array and not copying, therefore if a is changed, b is changed too
20) c = a.copy() -> copy array a to c
21) a = np.array([1, 2, 3, 4]), b = a[1:3] -> b is a view of a, once value of b is changed, a will be changed
    - Note: x.base is y is used to check whether the array x is a view of y
    - view means new array is not storing a seperate copy but is referencing from the original array 
22) .resize() creates a new copy
23) .reshape() creates a view
24) @ is matmul, * is element wise mul
25) Vectorization means doing an operation on an entire NumPy array at once instead of writing a Python loop yourself.
26) a3 = np.concatenate((a1,a2),axis=1) -> concat means combine, axis = 0 means combine via row and axis = 1 means combine via col
27) Advance indexing means creating row and col array, then combine both array and extract from the original array
    - Note: creates a copy and not view
28) rng = np.random.default_rng() -> use numpy to create a random number generator
    - a = rng.random(10) -> uniform distribution from (0, 1)
    - s = rng.normal(loc=5, scale=2, size=(5, 5)), loc=mean, scale=SD
29) np.savetxt(
        'savedata.txt',
        np.stack((x, y), axis=1),
        header='DATA',
        footer='END',
        fmt='%d %1.4f'
    )
    - create a txt file with #DATA as header #END as end
    - stack means combine both array in new dim
30) np.save()  -> save array into a numpy file
31) np.load()  -> load the numpy file 
32) import numpy.linalg as la -> import LA capabilities
33) la.norm -> find norm of vector, la.solve-> Ax=B, solve x, la.det-> determinant, la.inv -> find inverse, la.eig -> get eigenvalues and eigenvectors
34) %timeit -n <iterations> -r <repeats>  <code_snippet> -> repeat X iterations R times and measure the mean time and SD
35) p = Polynomial([0, 1, 0, -1/3]) -> \[p(x)=0+1x+0x^2-\frac13x^3\]

Learning Scipy library

1)  import scipy.linalg as sla -> more functions as compared to numpy.linalg
2)  