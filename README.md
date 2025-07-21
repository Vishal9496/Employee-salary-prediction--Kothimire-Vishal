# Employee Salary Prediction - Vishal Kothimire

## Introduction
This initiative involves forecasting employee salaries through a Linear Regression approach, incorporating data examination, graphical representations, model development, and an accessible Streamlit-based web tool for dynamic predictions.

## Contents
- Overview of the Project
- Key Features
- Repository Files
- Data Source
- Setup Instructions
- How to Use
- Details on the Model
- Tools and Technologies

## Overview of the Project
The primary objective is to construct a machine learning system for approximating an employee's yearly earnings. Key steps include:

- Loading and Examining Data: Gaining insights into the employee dataset's layout and properties.
- Data Preparation: Identifying and addressing any absent entries or repeated records.
- In-Depth Data Analysis (EDA): Creating visuals to highlight patterns, such as gender breakdowns, job rating spreads, mean salaries across departments or nations, and overtime patterns.
- Model Development: Constructing a Linear Regression model with "Years" and "Job Rate" as inputs to forecast "Annual Salary".
- Model Preservation: Storing the developed model for future applications.
- Streamlit Interface: Designing an easy-to-use web app for entering "Years" and "Job Rate" to receive instant salary estimates.

## Key Features
- Thorough examination of employee information.
- Visual tools for spotting data patterns.
- A Linear Regression system for salary forecasting.
- Streamlit-powered app for straightforward predictions.
- Saved model for quick reuse and deployment.

## Repository Files
- prediction.ipynb: A Jupyter notebook covering the full workflow:
  - Importing the Employees.xlsx file.
  - Basic data checks (head, tail, info, shape, isna, duplicated).
  - Producing charts like gender pie charts, histograms for job rates and overtime, bar graphs for average salaries by department and job rates by country.
  - Dividing data into train and test groups.
  - Developing the LinearRegression model.
  - Assessing with Mean Absolute Error.
  - Exporting the model as linearmodel.pkl via joblib.

- my_app.py: Streamlit script that:
  - Offers inputs for "Years" and "Job Rate".
  - Imports the saved linearmodel.pkl.
  - Computes the salary prediction from user data.
  - Presents the result clearly.

- Employees.xlsx: The core dataset for model training and testing, featuring employee details like "Years", "Job Rate", and "Annual Salary".

- linearmodel.pkl: The pickled Linear Regression model, created in prediction.ipynb and utilized in my_app.py for efficient predictions.

## Data Source
Employees.xlsx serves as the project's dataset, holding employee details essential for salary forecasting.

Find the source dataset on Kaggle under Company Employees Dataset.

## Setup Instructions
Install required libraries via pip if needed (e.g., pandas, matplotlib, scikit-learn, joblib, streamlit).

## How to Use
### Executing the Notebook (prediction.ipynb)
1. Launch Jupyter: `jupyter notebook`
2. Access prediction.ipynb in the browser.
3. Run every cell to analyze data, train the model, and create linearmodel.pkl.

### Launching the Streamlit App (my_app.py)
- Confirm linearmodel.pkl is present (generate it via the notebook if missing).
- Start the app: `streamlit run my_app.py`
- The browser will show the Salary Prediction App; enter values for "Years" and "Job Rate", then click to predict.

## Details on the Model
Utilizing scikit-learn's Linear Regression:

Inputs (X):
- Years: Probably indicates experience or service length.
- Job Rate: A score reflecting job aspects like performance or difficulty.

Output (y):
- Annual Salary: The value being estimated.

The model learns linear connections between inputs and salary for accurate predictions on fresh data.

## Tools and Technologies
- Python
- Pandas (data handling)
- Matplotlib (visuals)
- Scikit-learn (Linear Regression)
- Joblib (model serialization)
- Streamlit (web app creation)
- NumPy (array and numerical tasks)
