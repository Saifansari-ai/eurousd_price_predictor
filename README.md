# eurousd_price_predictor

# Data of the project
## Dataset Overview

The dataset used in this project is focused on predicting the EUR/USD exchange rate. It consists of historical euro-usd price from (jan 2000 to frb 2025) and economic indicators of Europe and USA from (2000 to 2023). The dataset includes various features that are significant for making accurate predictions in foreign exchange markets.

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

## Exploratory Data Analysis (EDA)

The EDA process is a critical step in any data project. It allows us to gain insights into the data distribution, identify patterns, and discover relationships between variables. In this project, the EDA process was essential for understanding the historical EUR/USD data and identifying the most informative features for predicting future prices.

### Feature Engineering

The feature engineering process was used to create new features that may enhance the predictive power of the models. The following features were created:

* **Moving Averages**: The moving averages of the Price feature were calculated to capture the trend and momentum of the data. The moving averages were calculated using different time windows, such as 10, 20, 30, 50, and 100 days.
* **Relative Strength Index (RSI)**: The RSI was calculated to capture the strength of the trend. The RSI was calculated using a 14-day time window.
* **Bollinger Bands**: The Bollinger Bands were calculated to capture the volatility of the data. The Bollinger Bands were calculated using a 20-day time window and a standard deviation of 2.
* **Momentum**: The momentum of the data was calculated by taking the difference between the current price and the previous price.
* **Volume Features**: The volume features were created by taking the moving averages of the Vol. feature. The volume features were calculated using different time windows, such as 10, 20, 30, 50, and 100 days.

The feature engineering process resulted in a total of 15 features, which were then used to train and test the machine learning models.

### Normalization

The normalization process was used to scale the data to ensure all features contribute equally to the distance calculations in machine learning algorithms. The normalization process was performed using the Min-Max Scaler, which scales the data to a range of [0,1]. The Min-Max Scaler was used to normalize the following features:

* Price
* Open
* High
* Low
* Vol.
* Moving Averages
* RSI
* Bollinger Bands
* Momentum
* Volume Features

The normalization process resulted in a dataset where all features have the same scale, which is essential for training machine learning models.

