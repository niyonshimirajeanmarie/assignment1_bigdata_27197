#  Uber Fares Dataset Analysis – Power BI Dashboard

Assignment 1 – INSY 8413: Introduction to Big Data 
**Name:** Niyonshimira Jean Marie  
**Student ID:** 27197  
**Instructor:** Eric Maniraguha  
**Group:** A  

---

##  Dataset Information

 **Source:** [Kaggle – Uber Fares Dataset](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)  
**File Used:** `Uber-Jan-Feb-FOIL.csv`  
 **Rows:** 354  
 **Columns:**
   `dispatching_base_number`: Base company dispatching trips  
`date`: Date of trip  
`active_vehicles`: Number of vehicles in service  
`trips`: Number of completed trips  

---

##  Data Cleaning & Feature Engineering

Data preparation was conducted using **Python in Jupyter Notebook**.

### Steps:
1. Converted `date` column to datetime format
2. Checked for missing values (none found)
3. Generated descriptive statistics (mean, median, mode, std deviation)
4. Identified and visualized outliers
5. Created additional features:
    `year`, `month`, `day`, `day_of_week`
   `is_peak` (True if weekend)
   `base_encoded` (numeric encoding of base)

### Output Files:
 `cleaned_uber_fares.csv`: Cleaned data  
`enhanced_uber_fares.csv`: Feature-enhanced data  

---

##  Power BI Dashboard

The cleaned dataset was imported into **Power BI** for visualization and analysis.

### Key Insights:
**Weekends** saw higher trip volumes
 **Base B02598** dispatched the most trips
 **February** had a slight rise in active vehicles
 **Outliers** suggest high-demand days (e.g., holidays, promotions)

---

##  Sample Visualizations

###  Data Transformation

<img width="933" height="494" alt="two datasetbeing tansformed" src="https://github.com/user-attachments/assets/80f54de2-9f2a-4150-8e32-eb11bd60987e" />

###  Database Schema
<img width="1024" height="1024" alt="Database Schema Visualization" src="https://github.com/user-attachments/assets/269eb71e-9106-420b-8075-f15fa0ec4fcb" />


###  Final Power BI Dashboard


<img width="1536" height="1024" alt="Uber Trip Insights -  Dashboard" src="https://github.com/user-attachments/assets/5564c060-b60d-4cbd-8018-2e679804aa0a" />


---

## ✅ Conclusion

This project demonstrated the use of Python for data cleaning and **Power BI** for visual storytelling, providing key business insights from Uber's operational data.

---

## 📎 License

This project is for academic purposes under **AUCA - INSY 8413** 





