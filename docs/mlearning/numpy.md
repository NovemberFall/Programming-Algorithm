## NumPy

- Numpy is a Linear Algebra Libray for Python, the reason it is so important for Data Science
  with Python is that almost all of the libraries in the PyData Ecosystem rely on NumPy as one
  of their main building blocks
- Numpy has bindings to C libraries.


- NumPy arrays are the main way we will use Numpy throughout the course
- Numpy arrays essentially come in two flavors: vectors and matrices.
- Vectors are strictly 1-d arrays and matrices are 2-d (but you should note a matrix can still
  have one row or one column)

---


### Lecture 4 , exmaple

```py
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

observations_nr = 1000  # We select how many samples/observations we need (observations_nr)
x_values = np.random.uniform(low = -10, high = 10, size = (observations_nr, 1))
z_values = np.random.uniform(low = -10, high = 10, size = (observations_nr, 1))
# We use np.random.uniform to generate these values

inputs = np.column_stack((x_values, z_values)) 
# We use np.column_stack to literally stack two vectors in a matrix

# print(inputs)
```


#### numpy.random.uniform() in Python

- [Syntax](https://www.geeksforgeeks.org/numpy-random-uniform-in-python/)


