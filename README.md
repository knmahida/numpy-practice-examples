# numpy-practice-examples

A beginner-friendly collection of hands-on NumPy practice examples — covering array creation, indexing, reshaping, random numbers, boolean masking, arithmetic operations, and common NumPy functions. Perfect for learning NumPy fundamentals used in data science and scientific Python.

## Quick start

- Open the notebook `Numpy.ipynb` in Jupyter or VS Code and run the cells interactively.
- The examples use only the NumPy package; install it with pip if you don't have it:

```bash
pip install numpy
```

## What this repo shows (selected examples)

Below are a few representative examples copied from `Numpy.ipynb`. They demonstrate typical NumPy workflows with short explanations.

### 1) Basic setup and array creation

```python
import numpy as np
print('NumPy version:', np.__version__)

# From a Python list
my_list = [1, 2, 3, 4, 5]
arr = np.array(my_list)
# Range and stepped ranges
arr_range = np.arange(0, 11)
arr_step2 = np.arange(0, 11, 2)

# Zeros and ones
zeros_3 = np.zeros(3)
zeros_3x3 = np.zeros((3, 3))
ones_3 = np.ones(3)
```

Short explanation: use `np.array`, `np.arange`, `np.zeros`, and `np.ones` to construct arrays of different shapes and contents.

### 2) Random numbers

```python
# Uniform random floats
rand5 = np.random.rand(5)
rand_2x3 = np.random.rand(2, 3)

# Standard normal samples
randn5 = np.random.randn(5)

# Random integers
rand_int = np.random.randint(100)
rand_ints_1_100 = np.random.randint(1, 100, 10)
```

Short explanation: `np.random.rand`, `np.random.randn`, and `np.random.randint` generate random samples for testing and simulation.

### 3) Reshaping and basic statistics

```python
arr = np.array([1, 2, 3, 4, 5, 4, 6, 7, 8])
arr_reshaped = arr.reshape(3, 3)
arr_max = arr.max()
arr_min = arr.min()
arr_argmax = arr.argmax()
arr_argmin = arr.argmin()
```

Short explanation: reshape arrays with `.reshape()` and get simple statistics with `.max()`, `.min()`, `.argmax()`, and `.argmin()`.

### 4) Indexing, slicing, and boolean masking

```python
a = np.arange(1, 11)
print(a[8])        # single element
print(a[1:5])      # slice
slice_a = a[1:6]
copy = slice_a.copy()  # independent copy

# 2D indexing
arr_2d = np.array([[1,2,3],[4,5,6],[7,8,9]])
print(arr_2d[0, 1])

# Boolean mask
filtered_a = a[a > 5]
```

Short explanation: NumPy supports integer and comma-based indexing for multi-dimensional arrays; boolean masks filter values efficiently.

### 5) Vectorized arithmetic and ufuncs

```python
# Elementwise arithmetic
a_plus_a = a + a
a_minus_a = a - a
a_times_a = a * a
a_squared = a ** 2

# Universal functions
sqrt_a = np.sqrt(a)
exp_a = np.exp(a)
sin_a = np.sin(a)
cos_a = np.cos(a)
```

Short explanation: NumPy performs elementwise operations and provides fast universal functions (ufuncs) for math operations.

## Run the notebook

If you have Jupyter installed, run:

```bash
jupyter notebook Numpy.ipynb
```

Or open the file in VS Code and run cells inline.

## Notes

- This README highlights selected examples; open `Numpy.ipynb` for the full, runnable notebook with printed outputs and small explanatory comments.
- If you'd like, I can add a short rendered example output section or convert the notebook into a plain `.py` script.
