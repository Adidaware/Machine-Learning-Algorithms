# Financial Portfolio Forecasting & Time-Series Analysis

This project focuses on quantitative financial analysis, specifically forecasting the price of "Bond B" using historical portfolio data. It demonstrates proficiency in data engineering with SQL, time-series smoothing, and seasonality-adjusted trend modeling.

## 📈 Analytical Workflow

### 1. Data Engineering & SQL Integration
* **Time-Series Preparation:** Converted raw strings into standard Date objects for precise temporal analysis.
* **SQL Aggregation:** Utilized the `sqldf` library to perform SQL-based grouping, calculating the average monthly price for specific assets.

### 2. Time-Series Smoothing (WMA)
To reduce market noise and emphasize recent price action, a **Weighted Moving Average (WMA)** was implemented.
* **Weights:** `[0.1, 0.2, 0.2, 0.5]` (Linear weighting favoring the most recent 4 months).
* **Library:** `TTR` (Technical Trading Rules).



### 3. Model Backtesting (MAE)
To validate the accuracy of the WMA forecast, I implemented a backtesting loop to calculate the **Mean Absolute Error (MAE)**:

$$MAE = \frac{1}{n} \sum_{t=1}^{n} |Actual_t - Forecast_{t-1}|$$.

### 4. Seasonality & Trend Analysis
The project accounts for cyclical patterns by dividing the fiscal year into three seasons:
* **Seasonal Index (SI):** Calculated by comparing seasonal means against the overall global mean.
* **Trend Projection:** A linear regression model ($y = mx + b$) was fit to the seasonal data to predict future baselines.
* **Seasonally Adjusted Forecast:** The final forecast combines the linear trend with the appropriate Seasonal Index for higher precision.

## 🛠️ Tech Stack
- **Language:** R
- **Libraries:** - `sqldf`: SQL querying on R DataFrames.
    - `TTR`: Technical analysis and smoothing.
    - `stats`: Linear modeling (`lm`).
- **Data Source:** [Financial Portfolio Dataset](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/financial_portfolio_data.csv)

## 📁 Files
* `Forecasting.Rmd`: R Markdown source with the full analysis.

## 🚀 How to Run
1. Install the required packages in R:
   ```r
   install.packages(c("sqldf", "TTR", "RSQLite"))
   ```
2. Open `Forecasting.Rmd` in RStudio and click **Knit** to build the report. The dataset is read directly from its URL, so no download is needed.

[← Back to all projects](../README.md)
