# 🧠 NumPy Mastery Exercises

> **Goal:** Become comfortable thinking in vectors and matrices instead of Python loops.

---

# Level 1 — ndarray Basics

## Exercise 1

Create the following arrays:

* 1D array
* 2D array
* 3D array

Print:

* Shape
* Size
* Number of dimensions
* Data type

---

## Exercise 2

Convert:

```python
[1,2,3,4,5]
```

into

* int32
* float32
* float64

Observe the difference.

---

## Exercise 3

Create arrays using:

* np.zeros()
* np.ones()
* np.empty()
* np.arange()
* np.linspace()
* np.eye()
* np.identity()

Print every output.

---

# Level 2 — Indexing

## Exercise 4

Create:

```text
1 2 3
4 5 6
7 8 9
```

Print:

* First row
* Last row
* First column
* Last column
* Middle element
* Last two columns
* First two rows

---

## Exercise 5

Create a 3D array.

Practice accessing:

* First matrix
* Second matrix
* First row
* Last element
* Entire column

---

# Level 3 — Array Operations

Create:

```python
A = np.array([10,20,30,40,50])
B = np.array([2,4,6,8,10])
```

Perform:

* Addition
* Subtraction
* Multiplication
* Division
* Floor division
* Modulus
* Power

---

## Exercise 6

Without loops calculate

* Square
* Cube
* Square root
* Absolute value

---

# Level 4 — Statistics

Generate

```python
100 random numbers
```

Find

* Mean
* Median
* Standard deviation
* Variance
* Minimum
* Maximum
* Sum

---

## Exercise 7

Generate

```python
1000 random integers
```

Find

* Largest 10
* Smallest 10
* Average
* Count of numbers greater than 500
* Count of even numbers

---

# Level 5 — Shape Manipulation

Create

```python
np.arange(1,25)
```

Convert into

* 2×12
* 3×8
* 4×6
* 6×4
* 8×3
* 12×2

---

## Exercise 8

Practice

* reshape()
* flatten()
* ravel()
* transpose()
* T

Write what changes and what remains the same after each operation.

---

# Level 6 — Boolean Indexing

Create

```python
arr = np.arange(1,51)
```

Find

* Numbers greater than 25
* Even numbers
* Odd numbers
* Multiples of 5
* Numbers between 10 and 30
* Numbers divisible by both 2 and 3

Do not use loops.

---

# Level 7 — Broadcasting

Create

```python
A = np.arange(9).reshape(3,3)
```

Perform

* A + 10
* A * 5
* A + row vector
* A + column vector

Observe broadcasting.

Explain in your own words why broadcasting works.

---

# Level 8 — Random Module

Generate

* Random floats
* Random integers
* Random matrix
* Random binary matrix

Set

```python
np.random.seed(42)
```

Generate the same numbers twice.

Explain why reproducibility is important in Machine Learning.

---

# Level 9 — Mini AI Exercises

## Exercise 1

Normalize

```text
[10,20,30,40,50]
```

using

```text
(x-min)/(max-min)
```

---

## Exercise 2

Standardize

```text
[10,20,30,40,50]
```

using

```text
(x-mean)/std
```

---

## Exercise 3

Generate

```python
1000
```

random student marks.

Find

* Students above 90
* Students below 35
* Average marks
* Top 20 students

---

## Exercise 4

Generate a fake image

```python
(224,224,3)
```

Print

* Shape
* Size
* Dimensions

Explain why images are stored this way.

---

## Exercise 5

Generate

```python
1000 samples
```

Each sample should have

```text
5 features
```

Print

* Shape
* Mean of each feature
* Standard deviation of each feature

This is similar to preparing data before training an ML model.

---

# Level 10 — Performance Challenge

Create

```python
1,000,000 numbers
```

Using

* Python List
* NumPy Array

Measure

* Creation time
* Addition time
* Multiplication time

Write your observations.

---

# Level 11 — Matrix Operations

Create two matrices.

Practice

* Matrix addition
* Matrix subtraction
* Matrix multiplication
* Element-wise multiplication
* Matrix transpose

---

## Exercise

Calculate

* Row sums
* Column sums
* Diagonal sum

without loops.

---

# Level 12 — Real Thinking Questions

Answer these in your own words.

1. Why is NumPy faster than Python lists?

2. What is vectorization?

3. Why do AI libraries use ndarrays?

4. Difference between reshape() and resize()?

5. Difference between flatten() and ravel()?

6. Difference between transpose() and T?

7. What is broadcasting?

8. Why avoid loops in NumPy?

9. What is the difference between an element-wise operation and matrix multiplication?

10. Why is dtype important in Deep Learning?

---

# Final Challenge 🏆

Without watching any tutorial, build a small **Student Analytics System** using only NumPy.

The program should:

* Generate marks for 500 students.
* Calculate average, highest, and lowest marks.
* Count passed and failed students.
* Find the top 10 students.
* Normalize marks.
* Standardize marks.
* Display grade distribution (A, B, C, D, F).
* Calculate the pass percentage.
* Print all results without using Python loops wherever possible.

---

# Mastery Checklist

* [ ] I understand every ndarray property.
* [ ] I can create arrays without documentation.
* [ ] I can slice any dimension confidently.
* [ ] I understand broadcasting.
* [ ] I can reshape arrays mentally.
* [ ] I can filter data using Boolean indexing.
* [ ] I know when NumPy creates a copy vs. a view.
* [ ] I can explain why NumPy is faster than lists.
* [ ] I can solve problems without using loops.
* [ ] I can use NumPy comfortably for Machine Learning preprocessing.

---

> **Rule for Mastery:** If you catch yourself writing a `for` loop, pause and ask: *Can this be done with NumPy vectorization instead?* Building that habit is what separates beginners from engineers who are ready for AI, data science, and high-performance numerical computing.
