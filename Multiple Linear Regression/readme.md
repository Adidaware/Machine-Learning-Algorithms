# Multiple Linear Regression

This project builds and compares several multiple linear regression models on a synthetic dataset, then evaluates them on a held-out validation set.

## 📈 Approach
* **EDA:** checked for missing values and outliers.
* **Multicollinearity:** checked with variance inflation factors (`car::vif`).
* **Preprocessing:** scaled the numeric features and encoded the categorical ones.
* **Feature selection and modeling:** trained three candidate models (adjusted R² ≈ 0.99).
* **Ensemble:** combined the candidates' predictions into a single ensemble model.
* **Validation:** reports the MSE on a 500-row validation set and checks residual normality.

## 🛠️ Tech Stack
- **Language:** R (R Markdown)
- **Libraries:** `car`, base `stats` (`lm`)
- **Data:** [training data](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/synth-data.csv) · [validation set](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/synth-data-validation-500.csv)

## 📁 Files
* `multiple_linear_regression.Rmd`: R Markdown source with the full analysis.
* `multiple_linear_regression.html`: rendered report (code, output and plots).

## 🚀 How to Run
1. Install the required packages in R:
   ```r
   install.packages(c("car"))
   ```
2. Open `multiple_linear_regression.Rmd` in RStudio and click **Knit** to build the report. The dataset is read directly from its URL, so no download is needed.

[← Back to all projects](../README.md)
