# Apple-Health-Sleep-Analysis

**An evolving data analysis project analyzing personal health data from Apple Health — showcasing exploratory data analysis (EDA), predictive modeling, and continuous learning.**

---

## Project Overview
This repository contains Jupyter notebooks and scripts that analyze daily health metrics exported from **Apple Health** — including sleep duration, heart rate, and physical activity — to uncover insights, build predictive models, and sharpen data science skills.  
All code and analysis are updated regularly as part of my **continuous learning journey**.

---

## Key Modeling Tasks
Each task includes:
- Data preparation  
- Model training (Linear Regression, Random Forest, XGBoost)  
- Evaluation and comparison

### 1. Predict Active Energy Burned (Regression)
- **Target**: `ActiveEnergyBurned`
- **Best performer**: Linear Regression — *R² = 0.8157*

### 2. Predict Walking Speed (Regression)
- **Target**: `WalkingSpeed`
- **Best performer**: Random Forest — *R² = 0.8212*

### 3. Classify Walking Steadiness
- **Target**: `WalkingSteadiness` (Low vs High)
- **Best performer**: Random Forest — Balanced ROC AUC and F1 (moderate overall due to class imbalance)

### 4. Classify Active vs Sedentary Day
- **Target**: Based on step count or energy burned
- **Best performer**: Random Forest — Accuracy: 0.8152, F1-score: 0.8251, ROC AUC: 0.8948

### 5. Classify Stress Level (based on HRV)
- **Target**: `HeartRateVariabilitySDNN` (High vs Low stress)
- **Best performer**: Random Forest — ROC AUC: 0.7621, F1-score: 0.6304

---

## Repository Structure

- **notebooks/** – Exploratory analysis, modeling workflows, and visualizations  
- **requirements.txt** – Python dependencies  
- **README.md** – Project documentation

---

## How to Run
1. Clone the repo or open in **Google Colab**
2. Ensure your **cleaned health data CSV** (e.g., `cleaned_daily_health_data.csv`) is in the correct folder
3. Open and run the notebooks in order — starting with EDA, then modeling

> **Note**: All personal data is anonymized or aggregated to protect privacy. Raw Apple Health export files are **not included**.

---

## Continuous Learning Roadmap
Planned improvements:
- Advanced feature engineering  
- Additional target variables for prediction  
- Time-series forecasting  
- Interactive dashboards (Tableau, PowerBI)

---

## 🤝 Contributing
This project is open to feedback, ideas, and suggestions!  
Feel free to fork the repository, create pull requests, or open issues.

---

