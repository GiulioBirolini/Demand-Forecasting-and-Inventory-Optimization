# Demand-Forecasting-and-Inventory-Optimization

Demand forecasting with ML and inventory optimization using PuLP.

## Data

The full dataset comes from the Kaggle competition [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting).  
Due to file size restrictions, raw data, processed data, and models are not stored in this repository.  
Place the downloaded dataset in this folder before running the notebooks: `data/raw`

## Project Structure

- `notebooks/`  
  - **01_EDA.ipynb**: data cleaning and feature engineering  
  - **02_Forecasting.ipynb**: demand forecasting using ML regression models  
  - **03_Optimization.ipynb**: inventory optimization with PuLP  

- `data/`: data folders (`raw/`, `processed/`)  
- `requirements.txt`: dependencies  

## Setup

Install the required dependencies:

```bash
pip install -r requirements.txt


