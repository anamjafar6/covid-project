# Prediction of COVID-19 Trends Using Machine Learning Models

## Author Information

* **Author**: Anam Jafar
* **Dataset Source**: Our World in Data (OWID)
* **Creation Date**: 9 January 2025
* **Purpose**: Analysis and forecasting of COVID-19 trends (cases, deaths, vaccinations).



## 1. Introduction

The COVID-19 pandemic has had a significant impact globally, creating the need for reliable forecasting of cases, deaths, and vaccinations. 
This project applies machine learning techniques to the **Our World in Data (OWID) COVID-19 dataset** to predict future values of key indicators. By leveraging historical data, the project provides insights that can support planning and decision-making.


## 2. Dataset Overview

The **OWID COVID-19 dataset** is a comprehensive global database containing epidemiological, vaccination, demographic, and socioeconomic information.

* **Size**: 350,085 entries, 67 features
* **Data Coverage**: Over 200 countries and territories
* **Time Span**: Daily data from early 2020 to the present

**Key Features**:

* **Epidemiological Data**: Total cases, new cases, total deaths, new deaths
* **Vaccination Data**: Total vaccinations, new vaccinations, people vaccinated
* **Demographics and Socioeconomic Indicators**: Population density, GDP per capita, median age, HDI
* **Health Infrastructure**: Hospital beds per thousand, stringency index

Dataset Source: [Our World in Data COVID-19 Dataset](https://ourworldindata.org/coronavirus)



## 3. Objectives

The project focuses on predicting:

1. Total COVID-19 cases
2. Total deaths
3. Total vaccinations

Two machine learning models are implemented:

* **Linear Regression** (baseline)
* **Random Forest Regressor** (improved performance)


## 4. Methodology

### Data Preprocessing

* Missing values handled using median imputation
* Selected features: new cases, new deaths, new vaccinations, stringency index, population density, GDP per capita, median age, HDI
* Train-test split: 80% training, 20% testing

### Model Training

* Linear Regression for baseline comparisons
* Random Forest Regressor for non-linear relationships

### Evaluation Metrics

* **Mean Squared Error (MSE)**
* **R² Score**



## 5. Results

### Total Cases

| Model                   | MSE      | R² Score |
| ----------------------- | -------- | -------- |
| Linear Regression       | 1.35e+15 | 0.1608   |
| Random Forest Regressor | 1.40e+14 | 0.9131   |

### Total Deaths

| Model                   | MSE      | R² Score |
| ----------------------- | -------- | -------- |
| Linear Regression       | 1.17e+11 | 0.3115   |
| Random Forest Regressor | 8.38e+9  | 0.9508   |

### Total Vaccinations

| Model                   | MSE      | R² Score |
| ----------------------- | -------- | -------- |
| Linear Regression       | 4.82e+17 | 0.2300   |
| Random Forest Regressor | 8.55e+16 | 0.8635   |

**Summary**: Random Forest significantly outperformed Linear Regression across all prediction tasks.



## 6. Discussion

* Random Forest demonstrated high accuracy in predicting cases, deaths, and vaccinations.
* Linear Regression struggled with the non-linear patterns in the dataset.
* Predictions highlight the potential of ensemble methods for public health forecasting.



## 7. Limitations

* Predictions rely on historical data and do not account for sudden policy changes, new variants, or shifts in vaccine distribution.
* Some features (e.g., ICU admissions, testing rates) were missing or incomplete.
* Countries with sparse data may produce less reliable results.



## 8. Conclusion

This project shows the effectiveness of machine learning for COVID-19 forecasting. Random Forest Regressor provided strong performance and captured complex data relationships, making it a more reliable model than Linear Regression.



## 9. Future Work

* Incorporate lagged features (e.g., 7-day averages)
* Experiment with advanced models such as XGBoost, Gradient Boosting, and LSTMs
* Perform hyperparameter tuning for Random Forest to improve accuracy



## 10. References

1. Our World in Data COVID-19 Dataset: [https://ourworldindata.org/coronavirus](https://ourworldindata.org/coronavirus)
2. Scikit-learn Documentation: [https://scikit-learn.org](https://scikit-learn.org)
