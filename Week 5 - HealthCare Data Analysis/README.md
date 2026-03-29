# **HealthCare Analysis System**  
*Exploratory Data Analysis (EDA) & Risk Classification using Synthetic Health Data*

---

## **Overview**
Manual analysis of patient vitals is inefficient and prone to error. This project addresses the need for automated healthcare analytics by generating and analyzing a synthetic dataset of 10,000 patients.

By simulating real-world health parameters, this system identifies patterns, detects high-risk individuals, and provides data-driven insights to support clinical decision-making while maintaining data privacy.

The workflow includes:

- Large-Scale Data Generation: Creating 10,000 unique patient records.
- Data Cleaning: Handling missing values, type consistency, and outlier detection.
- Risk Classification: Categorizing patients into Low, Medium, and High Risk based on medical thresholds.
- Comparative Analysis: Grouping health conditions by Age and Gender.
- Advanced Visualization: Mapping correlations between vitals using Heatmaps and Scatter plots.

---

## **Dataset**
Source: Synthetic dataset generated using Python
Description: Contains a comprehensive health profile for each patient like Blood Pressure, Sugar Level, Cholesterol	and Heart Rate.

Dataset Features
Patient_ID	
Age	
Gender	
Blood_Pressure	
Sugar_Level	
Cholesterol	
Heart_Rate
Risk_Level

The dataset simulates real-world academic performance data for 250 students.
---

## **Objectives**
1. Synthetic Simulation: Generate a robust dataset that mimics real-world medical distributions.
2. Statistical Profiling: Calculate mean, median, and standard deviation for all vital signs.
3. Risk Stratification: Build logic to flag patients who exceed safe medical thresholds.
4. Relationship Mapping: Study correlations, such as:
      Blood Pressure vs. Age
      Cholesterol vs. Heart Rate
5. Visual Insights: Utilize a suite of charts (Histograms, Box plots, and Heatmaps) to identify health trends and outliers.

---

## **Project Highlights**

### **1. Data Generation**
- Generation: 10,000 records created using NumPy and Pandas.
- Cleaning: Handled data types, ensured consistency, and performed outlier detection for medical anomalies.

### **2. Exploratory Data Analysis (EDA)**
- Vital Analysis: Distribution of Blood Pressure and Sugar levels across different age groups.
- Risk Categorization: Logical flagging of patients requiring immediate medical attention.
- Demographic Study: Comparing health metrics between Male and Female cohorts.
- EDA helps understand academic performance patterns and variations.

### **3. Visualization**
The project includes:

- Histograms: To visualize the distribution of health parameters.
- Box Plots: For identifying medical outliers in cholesterol and heart rate.
- Heatmaps: To find correlations between age and rising blood pressure.
- Scatter Plots: Analyzing the relationship between sugar levels and risk categories.
- Visualizations make insights clear and easy to interpret. 

---

## **Tools and Technologies**
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- Jupyter Notebook
- CSV File Storage

---

## **Results**

### **Key Findings**
- Vital Correlations: Analysis shows a positive correlation between increasing Age and higher Blood Pressure and Cholesterol levels.
- Risk Distribution: Out of 10,000 patients, approximately 13% were classified as High Risk due to elevated sugar or heart rate metrics.
- Gender Trends: Preliminary data suggests variations in average Heart Rate and Cholesterol between male and female patient cohorts.
- Outlier Detection: Box plots successfully identified extreme cases of hypertension (BP > 170) and hyperglycemia (Sugar > 190).

### **Interpretation**
- Risk Stratification: The automated classification helps healthcare providers prioritize patients needing immediate intervention.
- Predictive Indicators: Strong relationships between health parameters allow for better early-warning systems for chronic conditions.
- Data Consistency: The synthetic generation successfully mimics real-world medical data distributions, making it a viable tool for testing diagnostic software.
- Decision Support: Structured EDA provides clear visual evidence to support clinical health monitoring and resource allocation.

The structured EDA approach improves clarity, reproducibility, and analytical quality of student performance analysis.
---

## **Author**
**Shree Pranava Ganesh**  
Student at Kamaraj College
Thoothukudi, Tamil Nadu
