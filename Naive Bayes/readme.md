# Congressional Voting Prediction using Naive Bayes Ensemble

This project implements a probabilistic classification model using the **Naive Bayes** algorithm to predict political party affiliation (Democrat or Republican). The project features a custom-built **Ensemble Method** to aggregate predictions across multiple data subsets.

## 🧠 Machine Learning Approach

### 1. Data Sampling & Splitting
To ensure the model is robust and not biased by a single train-test split, the project implements a custom sampling function:
* **Bootstrap-style Sampling:** Generates 5 distinct training and validation sets.
* **Sample Size:** 350 observations per training iteration.

### 2. Naive Bayes Ensemble
Instead of relying on one model, this project builds an **Ensemble of Classifiers**:
* **Base Learners:** 5 separate Naive Bayes models are trained using the `e1071` library.
* **Majority Voting logic:** A custom `predict_party` function aggregates the output of all 5 models and uses a "Majority Vote" mechanism to determine the final predicted class.



### 3. Bayesian Probability logic
The model utilizes the Naive Bayes theorem, which assumes independent predictors to calculate the posterior probability of a class:

$$P(C|X) = \frac{P(X|C)P(C)}{P(X)}$$

This approach is highly effective for categorical voting data (Yes/No/Abstain).

### 4. Evaluation Metrics
The ensemble is evaluated using the `caret` package across all validation subsets. The results include:
* **Mean Accuracy:** The average percentage of correct predictions.
* **Sensitivity (TPR):** The ability to correctly identify a specific party.
* **Specificity (TNR):** The ability to correctly identify the opposing party.

## 🛠️ Tech Stack
- **Language:** R
- **Key Libraries:**
    - `e1071`: Naive Bayes implementation.
    - `caret`: Model evaluation and confusion matrices.
    - `dplyr`: Data manipulation.
    - `knitr`: Professional table rendering.
- **Dataset:** [1984 House Votes Dataset](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/HouseVotes-1984-ButOne.csv)

## 📁 Files
* `naivebayes.Rmd`: R Markdown source with the full analysis.
* `naivebayes.html`: rendered report (code, output and plots).

## 🚀 How to Run
1. Install the required packages in R:
   ```r
   install.packages(c("e1071", "caret", "dplyr"))
   ```
2. Open `naivebayes.Rmd` in RStudio and click **Knit** to build the report. The dataset is read directly from its URL, so no download is needed.

[← Back to all projects](../README.md)
