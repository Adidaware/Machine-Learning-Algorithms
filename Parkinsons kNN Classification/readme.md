# Parkinson's Disease Classification with kNN

A k-Nearest Neighbors classifier that predicts a Parkinson's disease diagnosis from clinical and lifestyle features. The project focuses on careful preprocessing before a distance-based model, then checks the trained model on a separate, unseen validation set.

## 🧪 Pipeline
* **Missing data:** checked each feature's distribution before picking an imputation strategy, then imputed missing values.
* **Outliers:** flagged outliers with z-scores and imputed them, repeating the pass until the data was stable.
* **Correlation:** inspected relationships between features before modeling.
* **Normalization:** scaled all features so that no single variable dominates the Euclidean distance.
* **Model:** stratified train/test split, then `knn()` from the `class` package with **k = 45**.
* **Evaluation:** confusion matrix, accuracy, precision, recall and F1 score. Test accuracy was about **78.5%** (157 of 200 correct).
* **Validation:** the same preprocessing was applied to a new 100-patient dataset, which was then classified with the trained model.

## 🛠️ Tech Stack
- **Language:** R (R Markdown)
- **Libraries:** `class`, `caret`, `gmodels`, `ggplot2`
- **Data:** [Parkinson's diagnostic data](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/parkinsons-diagnostic-data.csv) · [validation set](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/parkinsons-diagnostic-validation-100.csv)

## 📁 Files
* `parkinsons_knn.Rmd`: R Markdown source with the full analysis.
* `parkinsons_knn.html`: rendered report (code, output and plots).

## 🚀 How to Run
1. Install the required packages in R:
   ```r
   install.packages(c("class", "caret", "gmodels", "ggplot2"))
   ```
2. Open `parkinsons_knn.Rmd` in RStudio and click **Knit** to build the report. The dataset is read directly from its URL, so no download is needed.

[← Back to all projects](../README.md)
