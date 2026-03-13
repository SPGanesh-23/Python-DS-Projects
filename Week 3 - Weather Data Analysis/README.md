# Weather Data Analysis and Seasonal Trend Visualization Using Python

## Project Overview

This project focuses on analyzing historical weather data using the Python libraries **Pandas** and **Matplotlib**. The objective is to apply **Exploratory Data Analysis (EDA)** techniques to clean, manipulate, and visualize weather data in order to identify seasonal patterns and climate trends.

In today’s data-driven world, analyzing environmental datasets helps students understand how raw data can be transformed into meaningful insights. This project demonstrates how Pandas operations such as indexing, filtering, grouping, and data cleaning can be used together with Matplotlib visualizations to explore relationships between weather variables like temperature, humidity, rainfall, and wind speed.

---

## Problem Statement

Weather data is collected continuously across different locations and time periods. However, raw weather records alone do not provide clear insights without proper analysis and visualization.

Students are required to analyze this dataset to answer questions such as:

* How does temperature change over time?
* What seasonal patterns exist in rainfall and humidity?
* Is there a relationship between temperature and humidity?
* How are weather observations distributed across seasons?
* How can missing weather data be handled effectively?

The primary objective is to apply Pandas operations to clean, transform, and analyze the weather dataset while visualizing important climate trends.

---

## Technologies Used

* Python
* Pandas
* NumPy (for numerical operations)
* Matplotlib (for visualization)
* Google Colab / Jupyter Notebook

---

## Dataset Description

The dataset contains weather observations with the following attributes:

* Location
* Date_Time
* Temperature_C (Temperature in Celsius)
* Humidity_pct (Humidity percentage)
* Precipitation_mm (Rainfall in millimeters)
* Wind_Speed_kmh (Wind speed in kilometers per hour)

---

## Implementation Details

### 1. Importing Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
```

### 2. Loading the Dataset

```python
df = pd.read_csv("weather_data.csv")
```

### 3. Data Inspection

```python
df.head()
df.info()
df.describe()
```

### 4. Handling Missing Data

```python
df.fillna(df.mean(numeric_only=True), inplace=True)
```

### 5. Date and Time Processing

```python
df["Date_Time"] = pd.to_datetime(df["Date_Time"])
df["Month"] = df["Date_Time"].dt.month
```

### 6. Creating Seasonal Categories

```python
def get_season(month):
    if month in [12,1,2]:
        return "Winter"
    elif month in [3,4,5]:
        return "Summer"
    elif month in [6,7,8]:
        return "Monsoon"
    else:
        return "Autumn"

df["Season"] = df["Month"].apply(get_season)
```

### 7. Temperature Trend Visualization

```python
plt.plot(df["Date_Time"], df["Temperature_C"])
plt.title("Temperature Trend Over Time")
plt.xlabel("Date")
plt.ylabel("Temperature (°C)")
plt.show()
```

### 8. Seasonal Rainfall Comparison

```python
season_rain = df.groupby("Season")["Precipitation_mm"].mean()
season_rain.plot(kind="bar")
plt.title("Average Rainfall by Season")
plt.show()
```

### 9. Temperature Distribution

```python
plt.hist(df["Temperature_C"], bins=20)
plt.title("Temperature Distribution")
plt.show()
```

### 10. Temperature vs Humidity Relationship

```python
plt.scatter(df["Temperature_C"], df["Humidity_pct"])
plt.title("Temperature vs Humidity")
plt.show()
```

### 11. Seasonal Data Distribution

```python
season_counts = df["Season"].value_counts()

plt.pie(season_counts, labels=season_counts.index, autopct="%1.1f%%")
plt.title("Season Distribution")
plt.show()
```

---

## Project Objectives Achieved

* Imported and inspected the weather dataset.
* Cleaned missing values using statistical methods.
* Performed Exploratory Data Analysis (EDA) on weather parameters.
* Visualized temperature trends using line plots.
* Compared seasonal rainfall using bar charts.
* Analyzed temperature distribution using histograms.
* Studied relationships between temperature and humidity using scatter plots.
* Represented seasonal weather distribution using pie charts.
* Interpreted visual results to identify seasonal patterns.
* Generated insights to understand climate trends.

---

## Key Learning Outcomes

* Understanding the process of **Exploratory Data Analysis (EDA)**.
* Handling and preprocessing real-world weather datasets.
* Working with **date and time data** in Python.
* Creating different types of visualizations using Matplotlib.
* Identifying relationships between environmental variables.
* Extracting meaningful insights from climate data.

---

## Conclusion

The Weather Data Analysis and Seasonal Trend Visualization project demonstrates how Python can be used to analyze environmental datasets effectively. By applying Pandas for data manipulation and Matplotlib for visualization, the project successfully identified seasonal patterns and relationships between weather parameters. This analysis provides valuable insights into climate trends and improves understanding of weather behavior.

---

## Author

**Shree Pranava Ganesh N R**

---