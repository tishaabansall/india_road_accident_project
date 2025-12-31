# India Road Accident Analysis & Severity Prediction 

An end-to-end data analysis and machine learning project analyzing **3,000+ Indian road accident records** to uncover safety risk patterns and predict accident severity.  
The project combines **EDA, feature engineering, and ML modeling** to derive actionable insights for road safety and policy planning.

---

##  Objective

- Identify high-risk patterns in Indian road accidents  
- Analyze how **time, speed, gender, and demographics** influence accident severity  
- Build interpretable ML models to **predict accident severity levels**

---

## Dataset

- **Source:** Ministry of Road Transport & Highways (MoRTH), India  
- **Time Period:** 2018–2023  
- **Records:** 3,000+ road accidents  

### Key Columns
- State, City  
- Date & Time of Day  
- Accident Severity (Minor / Serious / Fatal)  
- Speed Limit  
- Driver Age, Driver Gender  
- Number of Vehicles, Casualties  
- Alcohol Involvement  
- Accident Location Details  

---

## Project Structure
```text

India_Road_Accident_Project/
│
├── data/
│   ├── india_road_accidents.csv    # Original raw dataset
│   ├── cleaned_accidents.csv       # Dataset after basic cleaning
│   └── final_accidents_ml.csv      # Feature-engineered data for ML
│
├── notebooks/
│   ├── 01_load_data.ipynb          # Data loading & initial inspection
│   ├── 02_data_cleaning.ipynb      # Handling nulls, types, and formatting
│   ├── 03_eda.ipynb                # Exploratory Data Analysis & statistics
│   ├── 04_ml_model.ipynb           # Training & evaluating ML models
│   └── 05_visualizations.ipynb     # Script to generate & save final plots
│
└── plots/                          # Saved visualizations for reporting
    ├── accidents_by_state.png      # Regional distribution of accidents
    ├── confusion_matrix.png        # ML model performance metric
    ├── day_vs_night.png            # Analysis of time-based trends
    ├── gender_vs_severity.png      # Demographics vs outcome severity
    └── speed_vs_severity.png       # Correlation between speed and impact
```

## **Project Workflow**

### 1. Data Loading
- Load CSV into Pandas DataFrame
- Inspect rows, check missing values, and basic statistics

### 2. Data Cleaning
- Handle missing values (Driver Gender, Speed Limit)
- Fix typos and inconsistent strings
- Convert time columns to numeric formats

### 3. Exploratory Data Analysis (EDA)
- Accidents by State/City
- Day vs Night analysis
- Gender-based severity patterns
- Speed vs Severity patterns
- Casualty distributions

---

## **Visualizations**

-Gender vs Severity
-Speed Limit vs Accident Severity
-Number of Accidents by State
-Day vs Night Accident Count
-Random Forest Confusion Matrix

_All plots are saved in the `plots/` directory for reporting._

---

## **4. Feature Engineering**
- `Is_Night` (0=Day, 1=Night)  
- `Severity_Encoded` (0=Minor, 1=Serious, 2=Fatal)  
- Encoded `Driver Gender` numerically  
- Saved final ML-ready dataset: `final_accidents_ml.csv`

---

## **5. Machine Learning**
- **Features used:** `Is_Night`, `Speed Limit`, `Driver Age`, `Driver Gender_Encoded`  
- **Models trained:** Logistic Regression (baseline), Random Forest Classifier  
- **Evaluation:** Classification report, confusion matrix  
- **Insights:**  
  - Night-time and higher speed limits increase accident severity  
  - Driver age and gender influence severity risk  
  - Feature importance from Random Forest highlights actionable safety factors  

---

##  Key Achievements

- Cleaned and structured a real-world Indian accident dataset  
- Engineered meaningful temporal and severity-based features  
- Extracted actionable safety insights from EDA  
- Built interpretable ML models for severity prediction  
- Produced reusable plots suitable for reports and dashboards  

---

##  Future Improvements

- Add geospatial hotspot analysis using **Folium**  
- Incorporate alcohol involvement and vehicle type into ML models  
- Predict accident counts by region and hour  
- Deploy insights via a Streamlit dashboard  

---

##  Tools & Libraries

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- scikit-learn  
- Jupyter Notebook  

---

