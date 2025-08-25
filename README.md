# Demand-Forecasting-and-Inventory-Optimization

Demand forecasting with ML and inventory optimization using Pulp

## Data

The full dataset comes from the Kaggle competition
[Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting).
Due to file size restrictions, raw data, processed data, and models are not stored in this repository.  
Place the downloaded dataset in this folder before running the notebooks: data/raw

## Project Structure

\- notebooks/

&nbsp; - \*\*01\_EDA.ipynb\*\*: data cleaning and feature engineering

&nbsp; - \*\*02\_Forecasting.ipynb\*\*: demand forecasting using ML regression models

&nbsp; - \*\*03\_Optimization.ipynb\*\*: inventory optimization with PuLP

\- data/: data folders (raw/, processed/)

\- requirements.txt: dependencies

## Setup

Install the required dependencies:

`pip install -r requirements.txt`

## How to Run

1\. Place raw data in data/raw/

2\. Run the notebooks in order (01 → 02 → 03)

3\. The optimized ordering policy is saved under data/processed/

## Project Summary

\- \*\*Forecast accuracy (RMSE):\*\* I trained several linear and tree-based regression models. The best-performing model was a GradientBoostingRegressor, which I further fine-tuned via hyperparameter optimization. On the test set, the model achieved an RMSE of 2,795.82 units, meaning that, on average, the predicted demand deviates from the actual demand by this amount. This level of accuracy supports reliable inventory decisions.



\- \*\*Inventory optimization results:\*\* The model minimizes total cost by balancing purchasing, holding, and shortage penalties. I applied Operations Research principles to analyze the optimization problem using linear programming in three steps:



Business problem: define the operational objective and constraints (e.g., budget, warehouse capacity, service levels).



Mathematical model: formulate the parameters, decision variables, and constraints in a structured LP framework.



Computational model: use the demand forecasts from notebook 02\_Forecasting.ipynb to determine the optimal order quantities in each period so as to minimize total cost.

## Illustrative Example

!\[Inventory Optimization Example](results/figures/inventory\_optimization\_example.png)



\*This plot shows order quantities (Q), inventory levels (I), shortages (S), and forecasted demand over a rolling 24-week horizon, illustrating the output of the optimization model.\*





