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
   - **14-Day Lag**: The price from fourteen days prior.
   - **30-Day Lag**: The price from thirty days prior.
   Lag features capture the price momentum and help in understanding how past prices influence future prices.

5. **Target Variable:**
   - **Next Day Price**: The price of the asset on the following day, which serves as the target variable for the prediction models.

6.  **Volatility Metrics:**
   - **Bollinger Bands**: A volatility indicator that consists of a middle band (SMA) and two outer bands (standard deviations away from the SMA). It helps identify overbought or oversold conditions.
   - **Average True Range (ATR)**: A measure of volatility that calculates the average range between the high and low prices over a specified period, providing insights into market volatility.


These engineered features, combined with thorough preprocessing, form the basis for training machine learning models to predict future EUR/USD prices effectively.


### Visualization on Feature Engineered columns



1. **Visualization of SMA_7 vs SMA_30 and SMA_100 vs SMA_200:**
   - Create line plots of the SMA_7 vs SMA_30 and SMA_100 vs SMA_200 to visualize the relationship between the two pairs of short-term and long-term simple moving averages.
   - Analyze the plots to identify any trends, patterns, or insights that can be used to improve the prediction models.

2. **Visualization of Volatility on Weekdays, Week of Year, and Months:**
   - Create barplots of the  weekdays to get the volatility throughout the week 
   - create line plot on the week and months of the year to get long term volatility.
   - Analyze the plots to identify any trends, patterns, or insights that can be used to improve the prediction models.


3. **Visualization of RSI_14 vs Price**

- **Objective**: To identify overbought and oversold conditions in the EUR/USD market.
- **Method**: Plot the 14-day RSI along with the price data.
- **Analysis**:
  - The RSI is a momentum oscillator that ranges from 0 to 100, with values above 70 indicating overbought conditions and values below 30 indicating oversold conditions.
  - By visualizing the RSI_14 against the price, we can detect potential reversal points and assess market momentum.

4. **Visualization of MACD vs Signal Line**

- **Objective**: To capture trend changes and generate buy or sell signals.
- **Method**: Plot the MACD line and the Signal line on the same graph.
- **Analysis**:
  - The MACD is calculated by subtracting the 26-period exponential moving average (EMA) from the 12-period EMA, while the Signal line is the 9-period EMA of the MACD.
  - Crossing of the MACD above the Signal line is considered a bullish signal, while crossing below is considered bearish.
  - By visualizing these indicators, we can identify trends and potential trading opportunities.

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

