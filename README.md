# Rohlik Orders Forecasting Challenge

## Project Overview

This repository contains my solution to the [Rohlik Orders Forecasting Challenge](https://kaggle.com/competitions/rohlik-orders-forecasting-challenge) on Kaggle. The challenge involves predicting the number of grocery delivery orders at various Rohlik warehouses across Europe over the next 60 days. This project is crucial for improving workforce allocation, delivery logistics, inventory management, and overall supply chain efficiency. By providing accurate forecasts, we aim to help Rohlik Group minimize waste, streamline operations, and enhance their e-grocery services.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Installation](#installation)
3. [Project Structure](#project-structure)
4. [Data Description](#data-description)
5. [Approach](#approach)
6. [Results](#results)
7. [Conclusion](#conclusion)
8. [Contact](#contact)

## Installation

To replicate the results or further develop this project, you'll need to install the required Python libraries. Ensure you have Python 3.8 or later installed.

```bash
pip install -r requirements.txt
```

## Project Structure

The repository is organized as follows:

- `1_EDA.ipynb` - Exploratory Data Analysis: Initial exploration of the dataset, data cleaning, and visualization.
- `2_lag_analysis.ipynb` - Lag Analysis: Examination of lagged features to identify temporal dependencies.
- `3_preprocess_feature_engineering.ipynb` - Preprocessing & Feature Engineering: Data preprocessing and creation of additional features to enhance model performance.
- `4_batch_training.ipynb` - Batch Training: Implementation of various machine learning models and hyperparameter tuning.
- `5_Recursive_forecast.ipynb` - Recursive Forecasting: Recursive techniques for making multi-step forecasts.
- `data/` - Contains the datasets used in the project.
- `outputs/` - Includes model predictions and evaluation results.
- `requirements.txt` - Lists the Python dependencies required to run the notebooks.

## Data Description

The project utilizes several key datasets provided by the competition organizers:

- `train.csv`: Historical data on warehouse orders.
- `test.csv`: Test set for forecasting future orders.
- `train_calendar.csv`: Calendar data including public holidays and warehouse-specific events.
- `test_calendar.csv`: Calendar data for the test period.

### Key Columns

- `warehouse`: Name of the warehouse.
- `date`: Date of the orders.
- `orders`: Number of customer orders.
- `holiday_name`, `holiday`, `shutdown`, etc.: Various features indicating holidays, warehouse operations, weather conditions, and user activity.

## Approach

### 1. Exploratory Data Analysis (EDA)

In the EDA phase, I performed an initial exploration of the data to understand its structure, distribution, and potential challenges. This included handling missing values, outlier detection, and visualizing key trends over time.

### 2. Lag Analysis

Next, I focused on creating lagged features to capture temporal dependencies. Lagged variables are crucial for time series forecasting as they help in capturing trends and seasonality in the data.

### 3. Preprocessing & Feature Engineering

In this phase, I preprocessed the data by scaling, encoding categorical variables, and creating additional features such as moving averages, day-of-week indicators, and interaction terms.

### 4. Batch Training

This phase involved training multiple machine learning models, including Gradient Boosting Machines (GBM), XGBoost, and LSTM networks. I performed extensive hyperparameter tuning and cross-validation to optimize model performance.

### 5. Recursive Forecasting

For the final step, I employed recursive forecasting techniques to generate multi-step forecasts. This approach allowed the model to make predictions over an extended period while maintaining accuracy.

## Results

The models were evaluated using the Mean Absolute Percentage Error (MAPE) metric, which is the competition’s chosen evaluation metric. The final model achieved a competitive MAPE score, demonstrating its ability to accurately predict future orders.

Key highlights include:
- **Best Model:** XGBoost with lag features and recursive forecast.
- **MAPE Score:** 5.54% on the test set.
- **Notable Observations:** Lag features and calendar effects significantly improved forecast accuracy.

## Conclusion

The Rohlik Orders Forecasting Challenge provided an excellent opportunity to apply and refine advanced time series forecasting techniques. The final model successfully captured the temporal patterns in the data, contributing to more efficient and sustainable e-grocery delivery operations.

## Contact

Feel free to reach out if you have any questions or would like to discuss potential collaborations:

- **Email:** ali@zarreh.ai
- **LinkedIn:** www.linkedin.com/in/ali-zarreh
