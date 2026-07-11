# Day 02

## 🎯 Mission

Learn **NumPy**, the foundation of numerical computing in Python and one of the core building blocks of AI, Machine Learning, and Deep Learning.

---

# ⏰ Hour 1 — Concepts + Coding

## Module 1: `ndarray`

Understand:

* What is an `ndarray`?
* Difference between a Python `list` and a NumPy `ndarray`
* Dimensions
* `shape`
* `size`
* `ndim`
* `dtype`

Practice:

```python
import numpy as np

arr = np.array([1, 2, 3])

print(arr)
print(arr.shape)
print(arr.dtype)
print(arr.ndim)
print(arr.size)
```

---

## Module 2: Array Creation

Write code for each function yourself:

```python
np.array()
np.zeros()
np.ones()
np.empty()
np.arange()
np.linspace()
np.eye()
np.identity()
np.random.rand()
np.random.randint()
```

Create at least one example for every function.

---

## Module 3: Indexing & Slicing

Practice:

* 1D Arrays
* 2D Arrays
* 3D Arrays

Examples:

```python
arr[0]
arr[-1]
arr[1:5]
arr[:, 1]
arr[1, :]
arr[0:2, 1:3]
```

Understand what each operation returns.

---

# ⏰ Hour 2 — NumPy Operations

## Arithmetic

Practice:

```python
+
-
*
/
//
%
**
```

---

## Statistics

Learn and practice:

```python
np.mean()
np.median()
np.std()
np.var()
np.max()
np.min()
np.sum()
```

---

## Shape Operations

Practice:

```python
reshape()
flatten()
transpose()
T
ravel()
```

---

## Boolean Indexing

```python
arr > 5
arr[arr > 5]
```

Understand why Boolean indexing is useful for filtering data efficiently.

---

# 🎯 Mini Project

Create a folder:

```text
day02_numpy_lab
```

Complete the following exercises:

### Q1

Create a **5×5 matrix** and print:

* Shape
* Size
* Data type

---

### Q2

Generate **100 random integers** and find:

* Maximum
* Minimum
* Mean
* Standard Deviation

---

### Q3

Create a **10×10 identity matrix**.

---

### Q4

Normalize the array:

```text
[10, 20, 30, 40, 50]
```

Formula:

```text
(x - min) / (max - min)
```

---

### Q5

Without using loops, find all even numbers in an array.

---

# 📚 Notes

Create:

```text
NumPy_Notes.md
```

For every topic, answer these four questions:

* What is it?
* Why do we need it?
* Where is it used in AI?
* One code example.

---

# 🏗️ GitHub

Inside your `AI-Engineer-Journey` repository, add:

```text
Math/
Python/
NumPy/
Day02/
```

Commit and push everything.

---

# 🎯 Bonus Challenge

Generate **1,000,000 numbers**.

Measure execution time using:

1. A Python `list`
2. A NumPy array

Compare the performance and write your observations.

---

# 📈 Day 02 Scoreboard

| Metric          | Target      |
| --------------- | ----------- |
| Study Time      | 2 Hours     |
| Coding Time     | 90+ Minutes |
| Notes Completed | ✅           |
| GitHub Commit   | ✅           |
| CodeWars        | 5+ Problems |
| Mini Project    | ✅           |

---

# 📜 Day 02 Reminder

> A carpenter does not become great by buying better tools. He becomes great by mastering the tools he already has.

Today's tool is **NumPy**. Master it thoroughly, because the concepts you learn here will make PyTorch, TensorFlow, and other AI frameworks much easier to understand.
