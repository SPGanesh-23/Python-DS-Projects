Titanic Dataset Analysis Using Pandas Series and DataFrames

Project Overview

This project focuses on analyzing the Titanic passenger dataset using the Python library Pandas. The objective is to apply DataFrame and Series operations to clean, manipulate, and explore structured passenger data in order to extract meaningful insights about survival patterns.

In today’s data-driven world, understanding historical datasets like the Titanic passenger records helps students practice real-world data analysis techniques. This project demonstrates how Pandas functions such as indexing, filtering, grouping, merging, and reshaping can be applied to uncover survival trends based on age, gender, class, and embarkation point.

Problem Statement

The Titanic dataset contains detailed passenger information. Students are required to analyze this dataset to answer questions such as:

What factors influenced passenger survival?

How did age, gender, and class affect survival rates?

What patterns emerge when grouping passengers by embarkation location?

How can missing data be handled effectively?

The primary objective is to apply Pandas operations to clean, transform, and analyze the dataset.

Technologies Used

Python

Pandas

NumPy (for numerical support)

Google Colab / Jupyter Notebook

Dataset Description

The dataset contains passenger details with the following attributes:

PassengerId

Name

Sex

Age

Pclass (Passenger Class)

Fare

Survived (0 = No, 1 = Yes)

Embarked (Port of Embarkation)

SibSp (Siblings/Spouses aboard)

Parch (Parents/Children aboard)

Implementation Details

1. Importing Libraries

import pandas as pd

2. Loading the Dataset

df = pd.read_csv("titanic.csv")

3. Series and DataFrame Creation

age_series = df["Age"]
fare_series = df["Fare"]
survived_series = df["Survived"]

4. Data Inspection

df.head()
df.info()
df.describe()

5. Handling Missing Data

df["Age"] = df["Age"].fillna(df["Age"].mean())
df["Embarked"] = df["Embarked"].fillna(df["Embarked"].mode()[0])

6. Indexing and Slicing

df.loc[10, ["Name", "Age", "Fare", "Survived"]]
df.iloc[5:10, [0, 2, 4, 6]]

7. Renaming and Reshaping

df.rename(columns={"Sex": "Gender"}, inplace=True)
pivot_table = df.pivot_table(values="Survived", index="Pclass", columns="Gender", aggfunc="mean")

8. Filtering and Sorting

df[df["Age"] > 30]
df[(df["Gender"] == "female") & (df["Survived"] == 1)]
df.sort_values(by="Fare", ascending=False)

9. Grouping and Aggregation

df.groupby("Gender")["Survived"].mean()
df.groupby("Pclass")["Age"].mean()
df.groupby("Embarked")["Survived"].sum()

10. Merging, Joining, Concatenation

extra_df = pd.DataFrame({
    "Pclass": [1, 2, 3],
    "Category": ["Luxury", "Standard", "Economy"]
})
merged_df = pd.merge(df, extra_df, on="Pclass", how="left")

11. Calculations and Insights

df.groupby("Survived")["Age"].mean()
df["Fare"].max(), df["Fare"].min()
(df["Survived"].sum() / len(df)) * 100

Project Objectives Achieved

Imported and inspected the Titanic dataset.

Cleaned missing values using mean and mode.

Applied indexing and slicing to extract passenger details.

Renamed and reshaped data using pivot tables and melt.

Filtered and sorted passengers based on conditions.

Grouped data to calculate survival rates and averages.

Merged additional datasets for richer analysis.

Calculated survival percentages and identified patterns.

Key Learning Outcomes

Handling missing data effectively.

Using loc and iloc for indexing and slicing.

Applying pivot and melt for reshaping.

Performing grouping and aggregation with groupby().

Combining datasets using merge, join, and concat.

Extracting insights about survival patterns from structured data.

Conclusion

The Titanic Dataset Analysis project demonstrates how Pandas can be leveraged for efficient and insightful data analysis. By applying Series and DataFrame operations, students gain hands-on experience in data cleaning, transformation, and statistical exploration. This project builds a strong foundation in data analytics and prepares learners for advanced applications in machine learning and business intelligence.

Author

Shree Pranava Ganesh N R
