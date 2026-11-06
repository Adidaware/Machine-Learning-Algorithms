# Parkinson's Disease Classification: Decision Tree, Random Forest & Logistic Regression

This project compares three classifiers for predicting a Parkinson's disease diagnosis and combines them into a majority-vote ensemble.

## 🧠 Approach
* **EDA and preprocessing:** examined class balance, encoded categorical features and imputed missing values.
* **Decision tree:** an `rpart` model, visualized with `rpart.plot`. It reached about **89.8% validation accuracy**.
* **Random forest:** a `randomForest` model trained on the imputed data.
* **Logistic regression:** a `glm` binomial model.
* **Ensemble:** combines the three models' predictions by majority vote, scored with precision, recall and F1 on the validation set.

## 🛠️ Tech Stack
- **Language:** R (R Markdown)
- **Libraries:** `rpart`, `rpart.plot`, `randomForest`, `caret`, `ggplot2`
- **Data:** [Parkinson's diagnostic data](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/parkinsons-diagnostic-data.csv) · [validation set](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/parkinsons-diagnostic-validation-100.csv)

## 📁 Files
* `parkinsons_classifiers.Rmd`: R Markdown source with the full analysis.
* `parkinsons_classifiers.html`: rendered report (code, output and plots).

## 🚀 How to Run
1. Install the required packages in R:
   ```r
   install.packages(c("rpart", "rpart.plot", "randomForest", "caret", "ggplot2"))
   ```
2. Open `parkinsons_classifiers.Rmd` in RStudio and click **Knit** to build the report. The dataset is read directly from its URL, so no download is needed.

[← Back to all projects](../README.md)
