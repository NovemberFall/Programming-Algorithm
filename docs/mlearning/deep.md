## Minimal example

- Simple Linear Regression,  Minimal example

- 1. Import the relevant libraries:


```py
import numpy as np          # mathematical operations
import matplotlib.pyplot as plt      # nice graphs
from mpl_toolkits.mplot3d import Axes3D  # nice 3D graphs
```


- 2. Generate random input data to train on

```py
observations = 1000

xs = np.random.uniform(low = -10, high = 10, size = (observations, 1))
# np.random.unifor(low, high, size) draw a random value from the interval
# (low, hight), where each number has an equal chance to be selected

zs = np.random.uniform(-10, 10, (observations, 1))

inputs = np.column_stack((xs, zs))

print(inputs.shape)
```

![](img/2020-10-10-16-36-35.png)

![](img/2020-10-10-16-38-54.png)



- 3. Create the targets we will aim at

```py
# targets = f(x, z) = 2 * x - 3 * z + 5 + noise
# you can try different functions for homework
```

![](img/2020-10-10-18-14-00.png)





- 4. Plot the training data


































