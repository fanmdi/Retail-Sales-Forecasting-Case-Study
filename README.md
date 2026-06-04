[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fanmdi/Retail-Sales-Forecasting-Case-Study/blob/main/Retail_Sales_Forcasting_Case_Study.ipynb)

# Retail-Sales-Forecasting-Case-Study
End-to-end retail sales forecasting using Prophet and Random Forest with synthetic Australian retail data.
[Open in Google Colab](https://colab.research.google.com/drive/16Q9JYv8Lj-RKjaq0B0ojDIoOaI5gmY3k?usp=sharing)

## Project Overview

This project demonstrates an end-to-end retail sales forecasting workflow using Python.

The case study generates a synthetic retail sales dataset representing one year of historical sales for a retail environment. It then produces a six-month randomised future forecast for the upcoming 180 days, accounting for known seasonal peaks, holidays, and potential shifts in consumer demand.

The project was prepared as part of a technical skills assessment and uses fully synthetic data. No confidential or real customer data is included.

## Objectives

- Generate one year of realistic synthetic retail sales data
- Include product, store, customer, sales channel, and pricing attributes
- Incorporate Australian public holidays and school holidays
- Add realistic seasonal demand effects
- Build forecasting models using Prophet and Random Forest
- Evaluate model performance using common forecasting metrics
- Generate a 180-day randomised sales forecast
- Produce Power BI-ready output files for reporting and dashboarding

## Dataset Description

The generated dataset includes the following groups of fields:

### Product Attributes

- item_id
- item_name
- department
- category
- class
- size
- unit price
- unit cost
- GST rate

### Store Attributes

- location_id
- location_name
- state
- city
- suburb
- postcode
- latitude
- longitude
- store size
- store format
- parking spaces
- area income level
- population density

### Transaction Attributes

- transaction_date
- customer_type
- sales_type
- sales_channel_type
- sales_quantity
- total sales excluding GST
- total sales including GST
- GST amount
- COGS
- gross profit margin

### Holiday and Seasonal Attributes

- public holiday flag
- school holiday flag
- weekend flag
- Christmas period flag
- New Year period flag
- Easter period flag
- mid-year sales period flag

## Forecasting Approach

Two forecasting approaches were used.

### Prophet

Prophet was used because it is suitable for time-series forecasting and can model:

- Trend
- Weekly seasonality
- Yearly seasonality
- Holiday effects
- Event-based demand changes

### Random Forest

Random Forest was used as a machine learning benchmark because retail demand can be influenced by several non-linear factors, including:

- Lagged demand
- Rolling sales averages
- Weekends
- Public holidays
- School holidays
- Seasonal peaks
- Promotional periods
- Random consumer demand shifts

Using both approaches provides a stronger forecasting comparison. Prophet gives interpretable time-series components, while Random Forest captures feature-based demand patterns.

## Model Evaluation

Both models are evaluated using:

- MAE
- RMSE
- MAPE
- WMAPE
- Forecast Bias
- R²

WMAPE is highlighted because it is commonly used in retail demand forecasting.

## Future Forecast

The final output includes a 180-day randomised future forecast with:

- Forecast date
- Expected sales volume
- Lower forecast bound
- Upper forecast bound
- Holiday indicators
- Seasonal peak indicators
- Random demand shift factor

These outputs are designed to be suitable for Power BI dashboards and retail planning reports.

## Power BI Use Case

The generated outputs can be loaded into Power BI to create dashboards for:

- Daily sales forecast monitoring
- Holiday and seasonal demand impact
- Forecast accuracy tracking
- Inventory planning
- Promotional planning
- Store-level demand review
- Executive reporting

## Files

| File | Description |
|---|---|
| Retail_Sales_Forecasting_Case_Study.ipynb | Main Google Colab notebook |
| retail_sales_180_day_randomised_forecast_prophet.csv | Prophet 180-day forecast output |
| retail_sales_180_day_randomised_forecast_random_forest.csv | Random Forest 180-day forecast output |
| retail_sales_prophet_accuracy_summary.csv | Prophet model accuracy results |
| random_forest_accuracy_summary.csv | Random Forest model accuracy results |
| random_forest_feature_importance.csv | Feature importance from Random Forest |

## Tools and Libraries

- Python
- Pandas
- NumPy
- Faker
- Holidays
- Prophet
- Scikit-learn
- Matplotlib
- Google Colab
- Power BI-ready CSV outputs

## How to Run

1. Open the notebook in Google Colab.
2. Run all cells from top to bottom.
3. The notebook will generate the synthetic dataset, train the models, evaluate accuracy, and produce the 180-day forecast.
4. Output CSV files will be created and can be downloaded or loaded into Power BI.

## Disclaimer

This project uses synthetic retail data created for demonstration purposes only. All product, store, sales, and forecasting outputs are fictional and do not represent actual company performance.
