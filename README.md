# Tetouan City Power Consumption Analysis and Prediction

**Author:** Kelvin Chinchilla
**Date:** October 2025

---

## 1. Project Summary

This project analyzes the energy consumption of Tetouan city (Morocco) during the year 2017. The goal is to clean the data, find consumption patterns, and build a Machine Learning model capable of predicting energy demand based on environmental factors.

---

## 2. Methodology

The project was developed in a Python notebook and followed these steps:

* **Load and Clean:** Data (52,416 rows) was loaded, and column names were cleaned. The `DateTime` column was converted into a time-series index.
* **Exploratory Data Analysis (EDA):** Data was resampled to a daily frequency, and relationships were visualized. The key finding was a strong positive correlation between `Temperature` and `Power Consumption`, suggesting high Air Conditioning usage in summer.
* **Feature Engineering:** New features (predictors) were created from the date, such as `hour`, `day_of_week`, and `month`.
* **Modeling (Machine Learning):** A `RandomForestRegressor` model was trained to predict `Zone_1_Power_Consumption`.

---

## 3. Results and Conclusions

### Visual Analysis




### Model Evaluation
The model was trained on 70% of the data and tested on the remaining 30%.

* **Model:** `RandomForestRegressor`
* **Error (RMSE):** **1105.59 W**
* **Average Consumption:** 32,344.97 W

**Conclusion:** The model demonstrated high accuracy (approx. 96.6%), proving capable of predicting energy demand with low error. The most important features for the prediction were Sub_metering_3, Sub_metering_1, Sub_metering_2, and month, indicating that appliance usage (especially heating/cooling) and seasonality are the primary drivers of consumption.
