# 📊 Assignment 1 – Big Data Analytics  
## 🚖 Uber Fares Dataset Analysis – January & February

Name: Niyonshimira Jean Marie  
Student ID: 27197  
Course: INSY 8413 – Introduction to Big Data Analytics  
Title: `assignment1_bigdataanalytics`  
Instructor: Eric Maniraguha  
Date:24 July 2025

---

## 📁 Dataset Information

- Source: [Kaggle - Uber Fares Dataset](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)
- File Used: `Uber-Jan-Feb-FOIL.csv`
- Rows: 354  
- Columns:
  - `dispatching_base_number` — Base company dispatching the trips
  - `date` — Date of trips
  - `active_vehicles` — Number of vehicles on duty
  - `trips` — Number of trips completed

---

## 🧹 Data Cleaning & Feature Engineering (Python)

Performed in **Jupyter Notebook**:

### ✔️ Steps:
1. Converted `date` to datetime format.
2. Checked and confirmed no missing values.
3. Generated descriptive statistics (mean, median, mode, standard deviation).
4. Identified and visualized outliers.
5. Created new columns:
   - `year`, `month`, `day`, `day_of_week`
   - `is_peak` — Boolean for weekends
   - `base_encoded` — Numeric encoding of dispatching base

### 📤 Output Files:
- `cleaned_uber_fares.csv` — Cleaned data
- `enhanced_uber_fares.csv` — Cleaned + feature engineered data

---

## 📊 Power BI Visualizations

### Dashboard Visuals Created:

1. **Line Chart** – Daily Trip Trends
   - `date` vs `trips`

2. **Bar Chart** – Trips by Day of Week
   - `day_of_week` vs `trips`

3. **Column Chart** – Peak vs Off-Peak Analysis
   - `is_peak` vs `trips`

4. **Pie/Column Chart** – Trips by Dispatching Base
   - `dispatching_base_number` vs `trips`

5. **KPI Cards** – Summary Stats
   - Total Trips
   - Average Daily Trips
   - Total Active Vehicles

6. **Slicers** – Interactive Filters
   - `month`, `day_of_week`, `dispatching_base_number`

---

## 🎯 Key Insights

- **Weekends** (peak days) showed higher trip volumes.
- **Dispatching base B02598** had the most trips.
- February had a slight increase in active vehicles.
- Outliers suggest specific high-demand days (possibly holidays or promotions).

---
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv("Uber-Jan-Feb-FOIL.csv")

# Convert 'date' column to datetime format
df['date'] = pd.to_datetime(df['date'])

# Check for missing values
print(df.isnull().sum())

# Descriptive statistics
print(df.describe())

# Add new columns
df['year'] = df['date'].dt.year
df['month'] = df['date'].dt.month
df['day'] = df['date'].dt.day
df['day_of_week'] = df['date'].dt.day_name()
df['is_peak'] = df['day_of_week'].isin(['Saturday', 'Sunday'])

# Encode base number as numeric
df['base_encoded'] = df['dispatching_base_number'].astype('category').cat.codes

# Export cleaned data
df.to_csv("cleaned_uber_fares.csv", index=False)

# Export enhanced data
df.to_csv("enhanced_uber_fares.csv", index=False)

# Outlier visualization
plt.figure(figsize=(10, 5))
sns.boxplot(data=df, x='trips')
plt.title("Outliers in Trip Count")
plt.savefig("trip_outliers_boxplot.png")
plt.show()




