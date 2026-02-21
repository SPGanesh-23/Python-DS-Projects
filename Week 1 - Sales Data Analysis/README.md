# Sales Data Analysis Using NumPy Array Operations

## Project Overview

This project focuses on performing **sales data analysis** using the Python libraries **NumPy** and **Pandas**. The objective is to apply array-based numerical computation techniques to extract meaningful insights from a real-world supermarket sales dataset.

In today’s data-driven business environment, organizations rely on statistical analysis to evaluate sales performance, customer behavior, revenue generation, and operational efficiency. This project demonstrates how NumPy’s array operations, broadcasting, indexing, slicing, and vectorized computation can be used to analyze structured sales data effectively.

---

## Problem Statement

Organizations depend on data analytics to understand:

* Sales performance across stores
* Customer purchasing patterns
* Revenue trends
* Statistical distribution of sales

Students are required to analyze a real-world supermarket sales dataset using **NumPy array operations** and statistical functions to derive actionable insights.

The primary objective is to apply:

* NumPy array manipulation
* Indexing and slicing
* Mathematical and statistical functions
* Broadcasting
* Vectorized computation

to extract meaningful business intelligence from sales data.

---

## Technologies Used

* Python
* NumPy
* Pandas
* Google Colab / Jupyter Notebook

---

## Dataset Description

The dataset contains supermarket sales information with the following attributes:

* Product categories
* Quantity sold
* Unit price
* Total sales
* Profit / Gross income
* Store ID
* Store Area
* Items Available
* Daily Customer Count

---

## Implementation Details

### 1. Importing Libraries

```python
import pandas as pd
import numpy as np
```

Pandas is used for data handling, and NumPy is used for numerical and statistical computation.

---

### 2. Loading the Dataset

```python
df = pd.read_csv("Stores.csv")
```

The dataset is loaded into a Pandas DataFrame and then relevant columns are converted into NumPy arrays for computation.

---

### 3. Converting Columns to NumPy Arrays

```python
store_id = df["Store ID"].to_numpy()
store_area = df["Store_Area"].to_numpy()
items_available = df["Items_Available"].to_numpy()
daily_customers = df["Daily_Customer_Count"].to_numpy()
store_sales = df["Store_Sales"].to_numpy()
```

This enables efficient numerical operations using NumPy functions.

---

### 4. Total and Average Sales

```python
total_sales = np.sum(store_sales)
average_sales = np.mean(store_sales)
```

* **Total Sales**: Sum of sales across all stores
* **Average Sales**: Mean sales per store

These metrics help evaluate overall business performance.

---

### 5. Statistical Analysis

```python
print("Mean:", np.mean(store_sales))
print("Median:", np.median(store_sales))
print("Variance:", np.var(store_sales))
print("Standard Deviation:", np.std(store_sales))
```

Statistical measures used:

* **Mean** – Average sales
* **Median** – Central sales value
* **Variance** – Spread of sales data
* **Standard Deviation** – Sales consistency indicator

These metrics help in understanding sales distribution and performance stability.

---

### 6. Broadcasting for Revenue Calculation

```python
df['Revenue'] = df['Store_Sales'] * df['Items_Available']
print(df[['Store ID', 'Revenue']])
```

Using NumPy broadcasting, revenue is calculated by multiplying:

Revenue = Store_Sales × Items_Available

This operation is vectorized and performed efficiently without loops.

---

### 7. Revenue Calculation for a Specific Store (Indexing)

```python
user_input = int(input("Enter Store ID: "))

result = df[df['Store ID'] == user_input]

if not result.empty:
    revenue = result['Store_Sales'] * result['Items_Available']
    print("Revenue for Store ID", user_input, ":", revenue.values[0])
else:
    print("Store ID not found")
```

This demonstrates:

* Boolean indexing
* Conditional filtering
* Dynamic user input handling

---

### 8. Indexing and Slicing

Users can retrieve specific store records using:

```python
index_result = df[df['Store ID'] == user_input]
```

Range-based slicing:

```python
slice_result = df[(df['Store ID'] >= start) & (df['Store ID'] <= end)]
```

This allows targeted analysis of selected store ranges.

---

## Project Objectives Achieved

This project enables students to:

1. Load a real-world sales dataset and convert relevant data into NumPy arrays
2. Perform array operations to calculate total and average sales
3. Use indexing and slicing to extract specific sales records
4. Apply statistical operations such as mean, median, variance, and standard deviation
5. Use broadcasting to calculate revenue from quantity and unit price
6. Implement vectorized computation for efficient data analysis
7. Interpret statistical results to understand sales trends and performance

---

## Key Learning Outcomes

* Efficient numerical computation using NumPy
* Avoiding loops through vectorized operations
* Performing descriptive statistical analysis
* Applying broadcasting for bulk calculations
* Using boolean indexing for conditional data extraction
* Interpreting statistical measures for business insights

---

## Conclusion

The Sales Data Analysis project demonstrates how NumPy array operations can be leveraged for efficient and scalable data analysis. By applying statistical functions, broadcasting, indexing, and vectorized computation, meaningful insights can be extracted from structured sales data.

This project builds a strong foundation in numerical computing and prepares students for advanced data analytics, machine learning, and business intelligence applications.

---

## Author

Shree Pranava Ganesh N R
