# Health Data Analysis and Modeling

This repository contains a Google Colab notebook that performs analysis and builds machine learning models on health data. The project focuses on predicting key health metrics and classifying walking steadiness based on various health indicators.

## Project Overview

The goal of this project is to explore a dataset containing daily health information and apply regression and classification techniques to understand the relationships between different health metrics and predict certain outcomes.

## Data

The analysis is based on **personal health data exported from Apple Health**. The data is loaded from CSV files. The primary data source used for modeling is the `cleaned_daily_health_data` which includes various health metrics such as step count, heart rate, distance, walking speed, physical effort, and walking steadiness.

## Modeling Tasks

The notebook (health_data_modeling.ipynb) performs the following modeling tasks:

1.  **Predicting Active Energy Burned (Regression)**:
    *   **Target**: Active Energy Burned
    *   **Features**: Step Count, Heart Rate, Distance Walking Running, Walking Speed, Walking Step Length, Physical Effort
    *   **Models**: Linear Regression, Random Forest, XGBoost
    *   **Key Finding**: The Linear Regression model performed best for this task, achieving an R² of 0.8157, indicating a strong ability to explain the variance in Active Energy Burned.
2.  **Predicting Walking Speed (Regression)**:
    *   **Target**: Walking Speed
    *   **Features**: Step Count, Heart Rate, Distance Walking Running, Walking Step Length, Physical Effort, Walking Heart Rate Average, Walking Asymmetry Percentage, Walking Double Support Percentage, Stair Ascent Speed, Stair Descent Speed, Weekday
    *   **Models**: Linear Regression, Random Forest, XGBoost
    *   **Key Finding**: The Random Forest model was the best performer for predicting Walking Speed with an R² of 0.8212 and the lowest MAE and RMSE.
3.  **Classifying Walking Steadiness (Classification)**:
    *   **Target**: Walking Steadiness (Binarized into 'Low Steadiness' and 'High Steadiness')
    *   **Features**: Step Count, Heart Rate, Distance Walking Running, Walking Speed, Walking Step Length, Physical Effort, Walking Heart Rate Average, Walking Asymmetry Percentage, Walking Double Support Percentage, Stair Ascent Speed, Stair Descent Speed, Weekday
    *   **Models**: Logistic Regression, Random Forest, XGBoost
    *   **Key Finding**: Based on ROC AUC and F1-score, the Random Forest model showed relatively better performance for classifying Walking Steadiness, although overall classification performance was moderate, likely due to class imbalance.
4.  **Classifying Active vs. Sedentary Days (Classification)**:
    *   **Target**: Activity Level (Binarized into 'Sedentary' and 'Active' based on ActiveEnergyBurned or StepCount)
    *   **Features**: Step Count, Heart Rate, Distance Walking Running, Walking Speed, Walking Step Length, Physical Effort
    *   **Models**: Logistic Regression, Random Forest, XGBoost
    *   **Metrics**: Accuracy, Precision, Recall, F1-score, ROC AUC
    *   **Visual**: Confusion Matrix
    *   **Key Finding**: The Random Forest model demonstrated the best overall performance for classifying Active vs. Sedentary days, with the highest Accuracy (0.8152), F1-score (0.8251), and ROC AUC (0.8948), indicating a good balance of precision and recall and overall ability to distinguish between the two classes.
5.  **Classifying Stress Levels (Classification)**:
    *   **Target**: Stress Level (Binarized into 'Low Stress' and 'High Stress' based on HeartRateVariabilitySDNN)
    *   **Features**: Step Count, Heart Rate, Distance Walking Running, Walking Speed, Walking Step Length, Physical Effort, Walking Heart Rate Average, Walking Asymmetry Percentage, Walking Double Support Percentage, Stair Ascent Speed, Stair Descent Speed, Weekday, Apple Sleeping Breathing Disturbances
    *   **Models**: Logistic Regression, Random Forest, XGBoost
    *   **Key Finding**: The Random Forest model performed best for classifying High Stress vs. Low Stress days, achieving the highest ROC AUC (0.7621) and F1-score (0.6304), indicating a better ability to distinguish between the two classes compared to the other models.

## Notebook Structure

The notebook is organized into sections for data loading, feature engineering, and separate sections for each modeling task including data preparation, model training, evaluation, comparison, and visualization.

## How to Use

1.  Clone this repository to your local machine or open the notebook directly in Google Colab.
2.  Ensure you have the necessary CSV data files in the specified directory (or update the data loading path). **Note: This analysis uses personal health data exported from Apple Health.**
3.  Run the cells sequentially to reproduce the analysis and modeling results.

Feel free to explore the code, modify the models, or perform further analysis on the data. I will be constantly updating this project for practice.
