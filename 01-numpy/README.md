# NumPy Fundamentals – Arrays, Indexing & Descriptive Statistics

## 📊 Project Overview

This notebook documents hands-on practice with NumPy fundamentals as part of a Python for Data Analytics learning roadmap. It covers creating arrays, inspecting their properties, accessing and slicing elements, calculating descriptive statistics, reshaping arrays, and applying mathematical functions.

All examples use small arrays defined directly in the notebook; no external dataset is required.

## 🛠️ Tools & Technologies

- **Python 3.13.9** – Python version recorded in the notebook metadata.
- **NumPy** – Array creation, numerical operations, and descriptive statistics.
- **Jupyter Notebook** – Interactive coding and saved outputs.

## 🧮 NumPy Concepts Practised

### 1. Creating Arrays & Inspecting Properties

Created one-dimensional arrays and a two-dimensional matrix with `np.array()`, then inspected `shape`, `size`, and `dtype`.

```python
import numpy as np

numbers = np.array([10, 20, 30, 40, 50])
print(numbers.shape)  # (5,)
print(numbers.size)   # 5
print(numbers.dtype)  # int64 in the saved output

matrix = np.array([[1, 2, 3], [3, 2, 1]])
print(matrix.shape)   # (2, 3)
```

### 2. Array Indexing

Practised zero-based indexing in one-dimensional arrays and nested indexing in two-dimensional arrays.

```python
num = np.array([10, 20, 30, 40, 50])
print(num[0])  # 10
print(num[2])  # 30

matrix = np.array([[1, 2, 3], [3, 2, 1]])
print(matrix[0][0])  # 1
print(matrix[1][2])  # 1
```

### 3. Array Slicing

Used start and stop indices, open-ended slices, and full-array slices to select elements.

```python
num = np.array([10, 20, 30, 40, 50])
print(num[0:3])  # [10 20 30]
print(num[1:4])  # [20 30 40]
print(num[2:])   # [30 40 50]
print(num[:3])   # [10 20 30]
print(num[:])    # [10 20 30 40 50]
```

### 4. Descriptive Statistics

Calculated the total, maximum, minimum, mean, population standard deviation, and median for five sample marks. The notebook uses Python built-in functions for the first three operations and NumPy functions for the others.

```python
marks = np.array([65, 70, 85, 90, 55])

print(sum(marks))     # 365
print(max(marks))     # 90
print(min(marks))     # 55
print(np.mean(marks)) # 73.0
print(np.std(marks))  # 12.884098726725126
print(np.median(marks)) # 70.0
```

`np.std()` uses `ddof=0` by default, so this result is the **population** standard deviation.

### 5. Reshaping Arrays

Reshaped a six-element one-dimensional array into two different **two-dimensional** layouts. The original notebook uses the variable names `new_2D` and `new_3D`; despite its name, `new_3D` is also a 2D array.

```python
num = np.array([1, 2, 3, 4, 5, 6])

new_2D = num.reshape(2, 3)
print(new_2D)
# [[1 2 3]
#  [4 5 6]]

new_3D = num.reshape(3, 2)
print(new_3D)
# [[1 2]
#  [3 4]
#  [5 6]]
```

### 6. Mathematical Functions

Practised square, square root, and power calculations with NumPy.

```python
square = np.square(5)
print(square)  # 25

sqrt = np.sqrt(25)
print(sqrt)    # 5.0

pow = np.pow(5, 2)
print(pow)     # 25
```

## 🎯 Skills Demonstrated

- Creating and inspecting NumPy arrays.
- Selecting data with indexing and slicing.
- Calculating basic descriptive statistics.
- Reshaping arrays into different two-dimensional layouts.
- Applying NumPy mathematical functions.

## 📂 Project Files

| File | Description |
|---|---|
| `01_numpy_basics.ipynb` | Notebook containing the exercises and saved outputs. |
| `README.md` | Documentation of the exercises, examples, and learning outcomes. |

## ▶️ How to Run

1. Use Python with Jupyter Notebook or JupyterLab. The notebook records **Python 3.13.9**.
2. Install NumPy 2.0 or later: `pip install "numpy>=2.0"` (`np.pow()` is not available in NumPy 1.x).
3. Open `01_numpy_basics.ipynb` and run the cells in order.

## 📚 Learning Outcome

This practice strengthened my understanding of NumPy arrays, element selection, descriptive statistics, reshaping, and mathematical operations. It provides a foundation for later data cleaning, analysis, and numerical work in Python.
