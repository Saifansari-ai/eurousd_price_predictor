# eurousd_price_predictor

# Data of the project
## Dataset Overview

The dataset used in this project is focused on predicting the EUR/USD exchange rate. It consists of historical euro-usd price from (jan 2001 to frb 2025) and economic indicators of Europe and USA from (2000 to 2023). The dataset includes various features that are significant for making accurate predictions in foreign exchange markets.

### Data Description

1. **Date**: The specific date for each entry in the dataset. This is important for time-series analysis.
   
2. **Open Price**: The price at which the EUR/USD pair started trading at the beginning of the trading day.
   
3. **High Price**: The highest price reached by the EUR/USD pair during the trading day.
   
4. **Low Price**: The lowest price reached by the EUR/USD pair during the trading day.
   
5. **Close Price**: The price at which the EUR/USD pair ended trading at the close of the trading day.
   
6. **Volume**: The total volume of trading for the EUR/USD pair within the trading day. This can indicate the level of interest or activity in the market.
   
7. **Other Indicators**: This may include technical indicators such as moving averages, RSI, MACD, etc., which are often used by traders to predict future price movements.

### Data Source

euro_usd_historical_data link : https://in.investing.com/currencies/eur-usd-historical-data

economic_indicators of Europe and USA link : https://databank.worldbank.org/reports.aspx?source=2&series=NY.GDP.MKTP.KD.ZG&country=EMU#


### Data Usage

The dataset is used to train and test machine learning models aimed at predicting future EUR/USD prices. The models analyze patterns and trends within the historical data to forecast future movements in the exchange rate.

### Data Preprocessing

Before using the data for model training, several preprocessing steps are performed:

- **Data Cleaning**: Removing missing or erroneous data points to ensure the quality of the dataset.
- **Normalization**: Scaling the data to ensure all features contribute equally to the distance calculations in machine learning algorithms.
- **Feature Engineering**: Creating new features that may enhance the predictive power of the models.

### Conclusion

Understanding the dataset is crucial for building effective predictive models. By leveraging historical data and carefully preprocessing it, the project aims to provide accurate predictions of the EUR/USD exchange rate, which can be beneficial for traders, investors, and financial analysts.

