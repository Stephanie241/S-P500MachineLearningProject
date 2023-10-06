# S&P 500 Financial Companies Stock Price Analysis Machine Learning Project

## Overview
This Python script performs regression analysis on the weekly adjusted stock price data of the top 5 S&P 500 financial companies. It uses historical stock price data obtained from Alpha Vantage via API requests and provides regression analysis results such as Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2) for a given target variable (e.g., 'Open', 'Close', 'Low').

### Visualisation of the Entire Project:
![Screenshot 2023-10-05 12](https://github.com/Stephanie241/S-P500MachineLearningProject/assets/144491602/51308e59-4f83-463f-ad24-f8d315b98eff)

### Examples of Regression Models produced for different companies over time against varying price metrics: 
![Screenshot 2023-10-05 130418](https://github.com/Stephanie241/S-P500MachineLearningProject/assets/144491602/6e06d4d4-ad03-4a71-9e90-693a03507075)

## Project Structure
The project consists of the following components:

### Main Python Script
- This is the main script that orchestrates the data collection, analysis, and visualisation.
- It imports necessary libraries such as pandas, requests, matplotlib, and sklearn for data manipulation, web scraping, visualisation, and regression analysis.
- The script is divided into several sections, each serving a specific purpose.

### Web Scraping
- The `get_symbols` function scrapes the list of S&P 500 companies from Wikipedia based on optional filter criteria such as GICS Sector.
- The `GetWeeklyAdjustedPrice` function retrieves the weekly adjusted stock price data for a given company symbol from Alpha Vantage.

### Data Visualisation
- The `PriceTimeSeries` function visualises the weekly stock price time series for a selected target variable (e.g., 'High') of a specific company.

### Regression Analysis
- The `perform_regression` function performs regression analysis on the stock price data.
- It supports three types of regression models: Linear Regression, K-Nearest Neighbors (KNN) Regression, and Support Vector Regression (SVR).
- The function calculates evaluation metrics (MSE, MAE, R2) and visualises the observed vs. predicted values.
- It also provides predictions for the selected target variable at a specified future time point.

## Usage
To use this script and perform regression analysis on the weekly stock price data of S&P 500 financial companies, follow these steps:

1. Make sure you have the required Python libraries installed. You can install them using `pip`:

  `pip install pandas requests matplotlib scikit-learn`

2. Run the `sp500_financial_regression.py` script in your Python environment.

3. The script will:
- Scrape the top 5 S&P 500 financial companies.
- Retrieve weekly adjusted stock price data for each of these companies from Alpha Vantage.
- Visualise the stock price time series for a selected target variable.
- Perform regression analysis on the data, allowing you to choose the regression model type (linear, KNN, or SVR).
- Display evaluation metrics and predictions for a future time point.

4. You can customize the target variable, model type, and other parameters within the script to analyze different aspects of the data.

## Dependencies
- Python 3.x
- Libraries: pandas, requests, matplotlib, scikit-learn

## Data Sources
- S&P 500 company list: [Wikipedia](https://en.wikipedia.org/wiki/List_of_S%26P_500_companies)
- Weekly adjusted stock price data: [Alpha Vantage API](https://www.alphavantage.co/)

Please note that the Alpha Vantage API key used in the script is for demonstration purposes only. You should obtain your own API key for extended use and adhere to any usage limits or terms of service set by Alpha Vantage.
