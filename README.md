#  Assignment 1 – Big Data Analytics  
##  Uber Fares Dataset Analysis – January & February

Name: Niyonshimira Jean Marie  
Student ID: 27197  
Course: INSY 8413 Introduction to Big Data Analytics  
Title: `assignment1_bigdataanalytics`  
Instructor: Eric Maniraguha  
Date:24 July 2025

---

## Dataset Information

- Source: [Kaggle - Uber Fares Dataset](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)
- File Used: `Uber-Jan-Feb-FOIL.csv`
- Rows: 354  
- Columns:
  - `dispatching_base_number` :Base company dispatching the trips
  - `date` :Date of trips
  - `active_vehicles` : Number of vehicles on duty
  - `trips` : Number of trips completed

---

##  Data Cleaning & Feature Engineering (Python)

Performed in **Jupyter Notebook**:

###  Steps:
1. Converted `date` to datetime format.
2. Checked and confirmed no missing values.
3. Generated descriptive statistics (mean, median, mode, standard deviation).
4. Identified and visualized outliers.
5. Created new columns:
   - `year`, `month`, `day`, `day_of_week`
   - `is_peak` : Boolean for weekends
   - `base_encoded` : Numeric encoding of dispatching base

###  Output Files:
- `cleaned_uber_fares.csv` : Cleaned data
- `enhanced_uber_fares.csv` : Cleaned + feature engineered data

---


##  Key Insights

- Weekends (peak days) showed higher trip volumes.
- Dispatching base B02598 had the most trips.
- February had a slight increase in active vehicles.
- Outliers suggest specific high-demand days (possibly holidays or promotions).

## all result images :
<img width="933" height="494" alt="two datasetbeing tansformed" src="https://github.com/user-attachments/assets/a89877ed-8a5a-49d2-a800-3e259e5beece" />

<img width="1024" height="1024" alt="Database Schema Visualization" src="https://github.com/user-attachments/assets/3529ee30-b592-447b-9466-64e46d32bd0b" />

<img width="927" height="434" alt="power bi dashaboard" src="https://github.com/user-attachments/assets/55a8d14d-f8b0-4865-b5b5-32a4bdca50e2" />

<img width="1536" height="1024" alt="images of diagrams" src="https://github.com/user-attachments/assets/edbde003-e022-444c-ab13-e175547bc8dd" />
<img width="1536" height="1024" alt="Uber Trip Insights -  Dashboard" src="https://github.com/user-attachments/assets/4db6798d-f624-4f8f-b621-9d0ca6fa4ac7" />

