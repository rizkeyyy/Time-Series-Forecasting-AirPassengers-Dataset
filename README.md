# Time Series Forecasting on AirPassengers Dataset


## Project Overview

This project demonstrates time series analysis and forecasting using the classic AirPassengers dataset (1949–1960).
The main goal is to forecast the number of airline passengers for the next 24 months using ARIMA/SARIMA models.

Key steps performed:

- Data exploration & visualization

- Stationarity check (ADF Test)

- Differencing to achieve stationarity

- ACF & PACF analysis

- ARIMA model selection & diagnostics

- Seasonal ARIMA (SARIMA) modeling

- Forecasting future passenger counts

## Dataset

- Name: AirPassengers.csv

- Description: Monthly totals of international airline passengers from 1949 to 1960.

- Columns:

- Month: Date (monthly)

- Passengers: Number of passengers

## Tools & Libraries

- Python (Jupyter Notebook)

### Libraries:

- pandas, numpy → data handling

- matplotlib, seaborn → visualization

- statsmodels → time series modeling (ADF test, ARIMA, SARIMA)

# Methodology
1. Data Exploration

- Initial plot shows upward trend and clear seasonal pattern.

2. Stationarity Test

- ADF Test on raw data → non-stationary (p-value > 0.9).

- After 1st differencing (d=1) → near-stationary (p-value ≈ 0.05).

- Final choice: d=1 + seasonal differencing (D=1, m=12).

3. ACF & PACF

- Used to identify potential AR (p) and MA (q) terms.

4. ARIMA Modeling

- Candidate models tested: (1,1,0), (1,1,1), (2,1,0), (2,1,1).

- Best ARIMA (based on AIC): ARIMA(2,1,1).

- Residuals checked → not fully white noise.

5. SARIMA Modeling

- Added seasonal terms.

- Best model: SARIMA(2,1,1)(1,1,0,12) with lowest AIC.

- Residual diagnostics & Ljung-Box test → residuals behave like white noise.

6. Forecasting

- Forecasted 24 months ahead (1961–1962).

- Results show continued upward trend with seasonal fluctuations.

# Forecast Plot

Here’s the forecast result with confidence intervals:

## Conclusion

- The AirPassengers dataset exhibits both trend and seasonality.

- After differencing, data became stationary enough for modeling.

- SARIMA(2,1,1)(1,1,0,12) was selected as the best-fit model.

- Forecast indicates continued growth in air travel with strong seasonal peaks.

# How to Run
1. Clone Repository
git clone https://github.com/rizkeyyy/Time-Series-Forecasting-AirPassengers-Dataset.git
cd Time-Series-Forecasting-AirPassengers-Dataset

2. Install Dependencies

- It’s recommended to use a virtual environment.

- pip install -r requirements.txt

👨‍💻 Author

Rizki Ramadhan

Project for portfolio: Time Series Forecasting with ARIMA/SARIMA
