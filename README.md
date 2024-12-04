# Time-Series-Forecasting
Project Overview

The objective of this project is to forecast sunspot activity using time series data and build predictive models capable of handling various time granularities (daily, monthly, and yearly). By leveraging Facebook Prophet's additive modeling approach, the project predicts sunspot counts and provides visual and numerical evaluations of the models.

Goals:
Data Agnostic Implementation: Develop a forecasting model adaptable to different time granularities.
Prediction Horizons:
Daily: Predict for 100, 200, and 365 days.
Monthly: Predict for 1, 6, and 9 months.
Yearly: Predict for 1, 10, and 20 years.
Model Tuning:
Forecasting growth (linear, logistic, flat).
Seasonal patterns using the add_seasonality method.
Trend changepoint adjustments.
Evaluation Metrics:
Mean Absolute Error (MAE).
Mean Absolute Percentage Error (MAPE).
Coefficient of Determination (R²).
Dataset

Sunspot data was obtained from the SILSO World Data Center and includes:

Daily Data: Total sunspot numbers recorded daily.
Monthly Mean Data: Average sunspot numbers per month.
Yearly Mean Data: Average sunspot numbers per year.
Dataset Details:
Columns:
Date components (Year, Month, Day).
Fractional year.
Sunspot count (missing values indicated by -1).
Standard deviation of sunspot counts.
Number of observations.
Definitive/provisional indicator.
Data sources:
Daily: SN_d_tot_V2.0.csv
Monthly: SN_m_tot_V2.0.csv
Yearly: SN_y_tot_V2.0.csv
Methodology

Data Preprocessing:
Handle missing values.
Parse and format dates for compatibility with Prophet.
Ensure compatibility with varying time granularities.
Forecasting with Prophet:
Train the model for daily, monthly, and yearly datasets.
Predict sunspot activity for specified horizons based on the time unit.
Incorporate additional seasonalities and tune growth/trend parameters.
Visualization:
Plot historical data alongside forecasts.
Include confidence intervals for future predictions.
Model Evaluation:
Calculate MAE, MAPE, and R² for each model.
Compare model performance across different granularities.
Results

Daily Forecasting:
Predicted sunspot counts for 100, 200, and 365 days into the future.
Monthly Forecasting:
Forecasted values for 1, 6, and 9 months ahead.
Yearly Forecasting:
Long-term predictions for 1, 10, and 20 years.
Detailed evaluations and plots are provided for each dataset.

How to Use

Clone the repository:
git clone https://github.com/your_username/sunspot-forecasting.git
cd sunspot-forecasting
Install required dependencies:
pip install -r requirements.txt
Run the respective Jupyter Notebook for the desired dataset:
daily_forecast.ipynb
monthly_forecast.ipynb
yearly_forecast.ipynb
Future Work

Explore advanced models such as LSTMs for improved forecasting accuracy.
Extend the model to include external data (e.g., solar activity or climatic factors).
Automate hyperparameter tuning using optimization techniques.
