# Crop-Price-Prediction

This project focuses on predicting crop prices in Rajasthan by analyzing multiple agricultural datasets collected for the year 2018–2019. The aim is to create a reliable machine learning model that can forecast prices using patterns derived from real-world environmental and market data.

The approach combines multiple sources of agricultural information, applies necessary preprocessing, conducts detailed analysis, selects useful features, and tests different regression models to compare their performance.

## Dataset Used

The data was taken from Kaggle and includes:
https://www.kaggle.com/datasets/suraj520/agricultural-data-for-rajasthan-india-2018-2019/data

## Project Structure

### 1. Data Integration

Merged information from:
- Crop production data
- Water usage statistics
- Soil analysis reports
- Market price history

### 2. Preprocessing Steps

- Removed missing and duplicate values
- Encoded categorical columns
- Scaled numerical data using MinMaxScaler
- Extracted day-of-year from date fields to add seasonal insights

### 3. Exploratory Data Analysis

- Created profile reports using ydata-profiling
- Visualized crop-wise and seasonal price variations
- Checked correlations between different variables

### 4. Feature Selection

- Applied Random Forest Regressor to rank and select the most important features affecting crop prices

## Models Applied

The following regression models were implemented and optimized using GridSearchCV:
- XGBoost Regressor
- LightGBM Regressor
- Gradient Boosting Regressor

## Evaluation Metrics

Models were evaluated using:
- R² Score (to measure prediction accuracy)
- Mean Squared Error (to measure error)

### Model Scores:

| Model                   | R² Score | Mean Squared Error |
|------------------------|----------|---------------------|
| Gradient Boosting      | 0.9844   | 0.000281            |
| XGBoost Regressor      | 0.9799   | 0.000362            |
| LightGBM Regressor     | 0.9476   | 0.000945            |
