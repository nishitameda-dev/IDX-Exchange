# California Property Close Price Prediction

**Intern:** Nishita Meda
**Organization:** IDX Exchange Data Science Internship
**Data Source:** CRMLS (California Regional Multiple Listing Service)

## Project Overview

This project develops machine learning models to predict the final sale price (ClosePrice) of residential single-family homes in California using historical CRMLS transaction data.

The goal is to identify the property characteristics that most influence home prices and build predictive models capable of estimating sale prices for new properties.

## Objectives

* Explore and understand CRMLS sold property data
* Clean and preprocess property records
* Engineer meaningful predictive features
* Train and compare multiple machine learning models
* Evaluate performance using R², MAPE, and MdAPE
* Document findings and model performance
* (Optional) Build a Streamlit application for price prediction

## Dataset

**Source:** CRMLS Sold Property Data

**Filters Applied:**

* PropertyType = Residential
* PropertySubType = SingleFamilyResidence

**Target Variable:**

* ClosePrice (Final Property Sale Price)

**Note:** Raw datasets are excluded from this repository according to internship guidelines.

## Repository Structure

├── notebooks/

├── scripts/

├── outputs/

├── docs/

├── README.md

└── requirements.txt

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Jupyter Notebook
* XGBoost
* LightGBM

## Models Evaluated

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* XGBoost
* LightGBM

## Evaluation Metrics

* R² Score
* Mean Absolute Percentage Error (MAPE)
* Median Absolute Percentage Error (MdAPE)

## Current Progress

* Repository setup completed
* Dataset access established
* Metadata review in progress
* Exploratory Data Analysis underway

## Author

Nishita Meda

University of Georgia

Computer Science Major, Minor in Law

