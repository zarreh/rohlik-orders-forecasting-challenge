# Rohlik Orders Forecasting Challenge

## Overview

This repository contains my solution to the Rohlik Orders Forecasting Challenge on Kaggle. Rohlik Group, a leading European e-grocery innovator, is revolutionizing the food retail industry by operating across 11 warehouses in the Czech Republic, Germany, Austria, Hungary, and Romania. The challenge focuses on predicting the number of orders (grocery deliveries) at selected warehouses for the next 60 days.

Accurate order forecasts are crucial for planning processes, impacting workforce allocation, delivery logistics, inventory management, and supply chain efficiency. By optimizing forecasts, we can minimize waste and streamline operations, making e-grocery services more sustainable and efficient.

## Project Files

### 1. Exploratory Data Analysis (EDA)
- **File:** [EDA.ipynb](EDA.ipynb)
- **Description:** This notebook contains detailed exploratory data analysis of the provided dataset. It includes data cleaning, visualization, and preliminary insights that form the foundation for building robust forecasting models.
- **Key Skills:** Data wrangling, Data visualization, Statistical analysis, Python (Pandas, Matplotlib, Seaborn).

### 2. Lag Analysis
- **File:** [lag_analysis.ipynb](lag_analysis.ipynb)
- **Description:** This notebook focuses on the analysis of lagged features and their impact on forecasting accuracy. Lag analysis helps in identifying temporal patterns and dependencies in the data.
- **Key Skills:** Time series analysis, Feature engineering, Python (Pandas, Numpy).

### 3. Batch Training
- **File:** [batch_training.ipynb](batch_training.ipynb)
- **Description:** This notebook demonstrates the batch training process of the forecasting models. It includes the implementation of various machine learning algorithms, hyperparameter tuning, and model evaluation.
- **Key Skills:** Machine learning, Model training, Hyperparameter tuning, Python (Scikit-learn, XGBoost).

## Dataset Description

- **Files:**
  - `train.csv`: Historical orders data and selected features.
  - `test.csv`: Test set for prediction.
  - `solution_example.csv`: Sample submission file.
  - `train_calendar.csv`: Calendar data for the training set.
  - `test_calendar.csv`: Calendar data for the test set.

- **Columns:**
  - `warehouse`: Warehouse name.
  - `date`: Date.
  - `orders`: Number of customer orders attributed to the warehouse.
  - `holiday_name`, `holiday`, `shutdown`, `mini_shutdown`, `shops_closed`, `winter_school_holidays`, `school_holidays`, `blackout`, `mov_change`, `frankfurt_shutdown`, `precipitation`, `snow`, `user_activity_1`, `user_activity_2`, `id`.

