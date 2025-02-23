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

The feature engineering process involves creating new features that can potentially increase the model's predictive accuracy. Below is a detailed documentation of the features engineered for this project:

1. **Simple Moving Averages (SMA):**
   - **7-Day SMA**: The average price over the last 7 days.
   - **30-Day SMA**: The average price over the last 30 days.
   - **100-Day SMA**: The average price over the last 100 days.
   - **200-Day SMA**: The average price over the last 200 days.
   These averages help smooth out short-term fluctuations and highlight longer-term trends in the data.

2. **Temporal Features:**
   - **Day of the Week**: day name indicating the day of the week.
   - **Week of the Year**: An integer representing the week number within the year.
   - **Month**: An integer (1-12) representing the month of the year.
   - **Year**: The year extracted from the date.

3. **Technical Indicators:**
   - **Relative Strength Index (RSI)**: A momentum oscillator that measures the speed and change of price movements, typically used to identify overbought or oversold conditions.
   - **Moving Average Convergence Divergence (MACD)**: A trend-following momentum indicator that shows the relationship between two moving averages of a security’s price.

4. **Lag Features:**
   - **1-Day Lag**: The price from the previous day.
   - **3-Day Lag**: The price from three days prior.
   - **7-Day Lag**: The price from seven days prior.
   Lag features capture the price momentum and help in understanding how past prices influence future prices.

5. **Target Variable:**
   - **Next Day Price**: The price of the asset on the following day, which serves as the target variable for the prediction models.

These engineered features, combined with thorough preprocessing, form the basis for training machine learning models to predict future EUR/USD prices effectively.


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

