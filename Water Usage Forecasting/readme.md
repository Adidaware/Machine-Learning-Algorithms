# Water Usage Forecasting

This project forecasts average daily water usage from monthly data covering February 2022 to November 2024.

## 📈 Approach
* **Exploration:** plotted the monthly series and fit a linear trend line.
* **Model:** a Holt-Winters exponential smoothing model (`HoltWinters`), with the fitted values plotted against the actual series.
* **Forecast:** a two-month forecast with 95% prediction intervals, made with the `forecast` package.

## 🛠️ Tech Stack
- **Language:** R (R Markdown)
- **Libraries:** `forecast`, `knitr`
- **Data:** [Water usage dataset](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/WaterUsage-02-22-to-11-24.csv)

## 📁 Files
* `water_usage_forecasting.Rmd`: R Markdown source with the full analysis.
* `water_usage_forecasting.html`: rendered report (code, output and plots).

## 🚀 How to Run
1. Install the required packages in R:
   ```r
   install.packages(c("forecast", "knitr"))
   ```
2. Open `water_usage_forecasting.Rmd` in RStudio and click **Knit** to build the report. The dataset is read directly from its URL, so no download is needed.

[← Back to all projects](../README.md)
