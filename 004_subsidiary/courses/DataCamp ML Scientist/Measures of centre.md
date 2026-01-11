#core/artificialintelligence

## Mean

The mean is the sum of all values in a dataset divided by the number of values. It represents the average value of the dataset.

In Python with NumPy, you can calculate the mean using the `numpy.mean()` function.

```python
import numpy as np

data = [1, 2, 3, 4, 5]
mean = np.mean(data)

print("Mean:", mean)
```

## Median

The median is the middle value in a sorted dataset. If the dataset has an odd number of values, the median is the middle element; otherwise, it is the average of the two middle elements.

In Python with NumPy, you can calculate the median using the `numpy.median()` function.

```python
import numpy as np

data = [1, 2, 3, 4, 5]
median = np.median(data)

print("Median:", median)
```

## Mode

The mode is the value(s) that appear most frequently in a dataset. A dataset can have one mode (unimodal), two modes (bimodal), or more (multimodal).

In Python, you can find the mode using the `scipy.stats.mode()` function from the SciPy library.

```python
from scipy import stats

data = [1, 2, 2, 3, 3, 3, 4, 5]
mode = stats.mode(data)

print("Mode:", mode.mode)
```

Note: The `mode()` function returns a `ModeResult` object that includes the mode value(s) and the count(s) of each mode. To access the mode(s), use the `mode` attribute as shown in the example above.

Remember to import the necessary libraries (`numpy` and `scipy.stats`) before using these functions.
