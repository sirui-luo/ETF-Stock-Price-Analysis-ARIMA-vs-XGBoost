# ETF-Stock-Price-Analysis-ARIMA-vs-XGBoost
This project provides a comprehensive time series analysis and forecasting of the VanEck Vectors Africa Index ETF (AFK) stock price. The analysis uses historical daily closing prices from July 2008 to November 2017, sourced from Kaggle. The primary objective is to build and evaluate a robust forecasting model and compare the performance of a classical statistical model with a machine learning approach.

Key Features

**Data Analysis**: The project begins with a thorough exploratory analysis of the AFK ETF closing prices, including data visualization and splitting the data into training and testing sets. The total sample size is 2,346 data points.

**ARIMA Modeling**: A detailed, step-by-step process is followed to build an ARIMA model.

The data undergoes a log transformation to stabilize variance.

Stationarity is checked using the Augmented Dickey-Fuller (ADF) test, which initially shows the series is non-stationary.


First-differencing is applied to achieve stationarity, identifying an integration order of d=1.


ACF, PACF, and EACF plots are analyzed to identify candidate model orders.

The final model, an ARIMA(0,1,1), is selected based on the lowest AIC/BIC values and coefficient significance.

**XGBoost Modeling**: For comparison, an XGBoost model is also developed to forecast the stock price.

The model uses engineered features such as time-based features (month, year), lag values, and rolling means.

**Model Evaluation and Comparison**: Both models are used to forecast the final 10 days of the dataset.

Performance is measured using the Root Mean Squared Error (RMSE).

The ARIMA model's residuals are diagnosed using the Ljung-Box test, which confirms they behave like white noise (p-value = 0.4523), indicating a good model fit.

<img width="858" height="594" alt="image" src="https://github.com/user-attachments/assets/15cd3c08-9e8e-41a6-9020-fa0d0aafbf53" />

<img width="712" height="460" alt="image" src="https://github.com/user-attachments/assets/2d3d97e2-fe35-4a52-803d-5c1f80a98e86" />

<img width="698" height="480" alt="image" src="https://github.com/user-attachments/assets/3fdeae8e-45f0-4cf9-baa3-0f1c56900c2e" />



