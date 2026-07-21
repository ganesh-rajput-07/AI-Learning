# 🐼 PROJECT HIMALAYA — PANDAS MISSION

**Good Morning, Soldier.**

Yesterday you learned to **SEE data**.

Today, you will learn to **CONTROL data**.

NumPy taught you how to work with numbers.

Matplotlib taught you how to visualize them.

Today, Pandas will teach you how to take a **messy real-world dataset** and turn it into something an AI/ML model can actually use.

> Data Scientists don't spend all day training models.
>
> **A large part of the job is understanding, cleaning, transforming, and preparing data.**

Today, we enter the world of **Pandas**.

---

# 🎯 Today's Mission

By the end of today's session, you should be able to:

* Create a Pandas Series
* Create and understand DataFrames
* Load real datasets
* Inspect datasets
* Select rows and columns
* Filter data
* Handle missing values
* Remove duplicates
* Clean data
* Sort data
* Create new features
* Group and aggregate data
* Merge datasets
* Export cleaned data

Most importantly:

> You should be able to take an unfamiliar dataset and start investigating it without fear.

---

# ⏰ SESSION 1 — Pandas Fundamentals

## Learn

Start with:

```python
import pandas as pd
```

Understand:

### Series

```python
pd.Series()
```

Learn:

* What is a Series?
* Index
* Values
* Custom Index

---

### DataFrame

```python
pd.DataFrame()
```

Create DataFrames from:

* Dictionary
* List
* NumPy Array

Understand:

```python
df.shape
df.columns
df.index
df.dtypes
df.values
```

---

### Inspecting Data

Master:

```python
df.head()
df.tail()
df.info()
df.describe()
df.sample()
```

Understand:

> Before manipulating data, **inspect it first**.

---

# 🧪 Mini Exercise 1 — Student Dataset

Create a dataset containing:

```text
Name
Age
Maths
Physics
Chemistry
Attendance
```

Create at least:

```text
20 Students
```

Now answer:

* How many rows?
* How many columns?
* What are the data types?
* What is the average Maths score?
* What is the average Attendance?
* Who has the highest Physics score?
* Who has the lowest Chemistry score?

---

# ⏰ SESSION 2 — Selecting & Filtering Data

Now learn how to extract exactly what you need.

## Selecting Columns

```python
df["Maths"]

df[["Maths", "Physics"]]
```

---

## Selecting Rows

Learn deeply:

```python
df.iloc[]
```

and

```python
df.loc[]
```

Understand:

```text
iloc → position based

loc → label based
```

---

## Boolean Filtering

Learn:

```python
df[df["Maths"] > 80]
```

Multiple conditions:

```python
df[
    (df["Maths"] > 80) &
    (df["Attendance"] > 75)
]
```

Also learn:

```python
&
|
~
```

---

# 🧪 Mini Exercise 2 — Find the Students

Using your Student Dataset:

Find:

* Students with Maths > 80
* Students with Physics < 40
* Students with Attendance < 60
* Students with Maths > 80 AND Physics > 80
* Students with Chemistry > 70 OR Attendance > 90
* Top 5 students based on Maths
* Bottom 5 students based on Attendance

---

# ⏰ SESSION 3 — Cleaning & Transforming Data

This is where Pandas becomes extremely important for AI/ML.

Learn:

## Missing Values

```python
df.isna()
df.isnull()
df.notna()
```

Remove:

```python
df.dropna()
```

Fill:

```python
df.fillna()
```

Understand:

* Mean imputation
* Median imputation
* Why blindly filling missing values can be dangerous

---

## Duplicates

Learn:

```python
df.duplicated()
df.drop_duplicates()
```

---

## Data Types

Learn:

```python
df.dtypes
df.astype()
```

---

## Rename Columns

```python
df.rename()
```

---

## Drop Columns

```python
df.drop()
```

---

## Sorting

```python
df.sort_values()
```

---

# 🧪 Mini Exercise 3 — Messy Dataset

Create a deliberately messy dataset.

Include:

* Missing marks
* Duplicate students
* Incorrect data types
* Extra spaces in names
* Invalid attendance values
* Incorrect capitalization

Example:

```text
" Ganesh "
"ganesh"
"GANESH"
```

Your mission:

```text
Messy Dataset
      ↓
Find Problems
      ↓
Clean Missing Values
      ↓
Remove Duplicates
      ↓
Fix Data Types
      ↓
Clean Text
      ↓
Remove Invalid Data
      ↓
Clean Dataset
```

Write down:

> What problems did you find?

> Why did you choose your particular cleaning method?

---

# ⏰ SESSION 4 — Creating New Features

Learn how to create new information from existing data.

Example:

```python
df["Total"] = (
    df["Maths"] +
    df["Physics"] +
    df["Chemistry"]
)
```

Then:

```python
df["Percentage"] = df["Total"] / 3
```

Create:

```text
Total
Percentage
Pass/Fail
Performance
```

---

## Learn

```python
apply()
```

and

```python
map()
```

Understand when to use them.

---

# 🧪 Mini Exercise 4 — Student Intelligence

Create:

### Pass/Fail

```text
Pass → Percentage >= 40
Fail → Percentage < 40
```

### Performance

```text
Excellent
Good
Average
Poor
```

Now create:

```text
Total
Percentage
Pass/Fail
Performance
```

Questions:

* What percentage of students passed?
* How many students are Excellent?
* How many students are Poor?
* What is the average percentage of passing students?

---

# ⏰ SESSION 5 — GroupBy & Aggregation

Now learn one of the most important Pandas concepts.

```python
df.groupby()
```

Understand:

```python
mean()
sum()
count()
min()
max()
```

And:

```python
agg()
```

---

# 🧪 Mini Exercise 5 — Employee Analytics

Create:

```text
Name
Department
Salary
Experience
Age
```

At least:

```text
30 Employees
```

Answer:

* Average salary
* Highest salary
* Lowest salary
* Average salary per department
* Employee count per department
* Highest paid employee per department
* Department with highest average salary
* Average experience per department

---

# ⏰ SESSION 6 — Combining Data

Real-world data rarely comes in one perfect table.

Learn:

## Concatenation

```python
pd.concat()
```

## Merge

```python
pd.merge()
```

Understand:

```text
inner
left
right
outer
```

Also understand:

```python
df.join()
```

---

# 🧪 Mini Exercise 6 — Customer Analytics

Create two datasets.

### Customers

```text
customer_id
name
city
```

### Orders

```text
order_id
customer_id
amount
```

Merge them.

Find:

* Total spending per customer
* Top 5 customers
* Revenue per city
* Average order value
* Customers with no orders

---

# ⏰ SESSION 7 — Real Dataset Investigation

Now we stop creating fake data.

Find a real CSV dataset.

Recommended:

```text
Titanic Dataset
```

or

```text
Student Performance Dataset
```

Load it:

```python
df = pd.read_csv("dataset.csv")
```

Now investigate it like a Data Scientist.

---

# 🔎 Data Investigation Checklist

Answer:

### Dataset Structure

* How many rows?
* How many columns?
* What are the column names?

### Data Types

* Which columns are numerical?
* Which are categorical?
* Which are dates?

### Data Quality

* Are there missing values?
* Are there duplicates?
* Are there invalid values?

### Statistics

* Mean
* Median
* Minimum
* Maximum
* Standard deviation

### Relationships

Ask:

* Which features might be related?
* Which columns might be useful for prediction?
* Which columns might be irrelevant?

---

# 🔥 BOSS FIGHT — Pandas Data Preparation Pipeline

This is today's main mission.

Take one real dataset.

Build this pipeline:

```text
Load Dataset
      ↓
Inspect Dataset
      ↓
Understand Columns
      ↓
Check Data Types
      ↓
Check Missing Values
      ↓
Check Duplicates
      ↓
Clean Data
      ↓
Filter Data
      ↓
Create New Features
      ↓
GroupBy Analysis
      ↓
Merge External Data
      ↓
Final Clean Dataset
      ↓
Export Dataset
```

Export:

```python
df.to_csv("cleaned_data.csv", index=False)
```

---

# 🧠 FINAL AI ENGINEER QUESTIONS

At the end, answer these in your notes:

### 1.

What is the difference between:

```text
NumPy Array
```

and

```text
Pandas DataFrame
```

---

### 2.

When would you use:

```text
loc
```

vs

```text
iloc
```

---

### 3.

What is the difference between:

```text
dropna()
```

and

```text
fillna()
```

---

### 4.

Why can missing data be dangerous for ML?

---

### 5.

What is the difference between:

```text
merge()
```

and

```text
concat()
```

---

### 6.

Why is `groupby()` useful in Data Analysis?

---

### 7.

Why do we clean data before training an ML model?

---

### 8.

What is a feature?

---

### 9.

What is a target?

---

### 10.

If you receive a completely unknown CSV file tomorrow, what will you do first?

Your answer should look like:

```text
Load
↓
Inspect
↓
Understand
↓
Clean
↓
Analyze
↓
Transform
↓
Prepare for ML
```

---

# 💻 CODEWARS MISSION

Minimum:

```text
8 Problems
```

Focus on:

* Lists
* Dictionaries
* Strings
* Loops
* Functions
* Conditions

**No AI help.**

First think.

Then code.

Then optimize.

---

# 📂 GITHUB STRUCTURE

Create:

```text
AI-Engineer-Journey/

├── Day01/
├── Day02/
├── Day03/
│
└── Pandas/
    │
    ├── pandas_basics.py
    ├── selection_filtering.py
    ├── data_cleaning.py
    ├── feature_engineering.py
    ├── groupby_analysis.py
    ├── merge_join.py
    ├── real_dataset_analysis.py
    ├── cleaned_data.csv
    └── README.md
```

---

# 🎯 TODAY'S DELIVERABLES

By the end of today's mission:

✅ Pandas Series

✅ DataFrames

✅ Dataset Inspection

✅ Selection & Filtering

✅ `loc` / `iloc`

✅ Missing Values

✅ Duplicate Handling

✅ Data Cleaning

✅ Feature Creation

✅ `apply()` / `map()`

✅ `groupby()`

✅ `merge()`

✅ Real Dataset Analysis

✅ Cleaned Dataset

✅ 8 CodeWars

✅ GitHub Commit

---

# 🏆 FINAL TEST

I will give you a completely unknown dataset.

You should be able to:

> **Load it → Understand it → Find problems → Clean it → Analyze it → Transform it → Prepare it for Machine Learning.**

If you can do that without blindly searching every line of code,

**Pandas Mission: COMPLETE.**

---

# 🗺️ PROJECT HIMALAYA

```text
Python Foundation        ✅
        ↓
Vector Mathematics       ✅
        ↓
NumPy                    ✅
        ↓
Matplotlib               ✅
        ↓
Pandas                   ← TODAY
        ↓
Statistics
        ↓
Scikit-Learn
        ↓
Machine Learning
        ↓
Deep Learning
        ↓
PyTorch
        ↓
NLP
        ↓
Transformers
        ↓
LLMs
        ↓
RAG
        ↓
AI Agents
        ↓
MLOps
        ↓
AI System Design
        ↓
AI Engineer Interviews
        ↓
₹50K+ Target
        ↓
PROJECT HIMALAYA 🏔️
```

**Today's mindset:**

> Don't try to memorize Pandas.
>
> **Use Pandas until manipulating data becomes natural.**
>
> Today you are not becoming a Pandas developer.
>
> **You are becoming someone who can take raw data and make it useful for AI.**
