# Congressional Voting Prediction using Naive Bayes Ensemble

This repository implements a probabilistic classification model using the **Naive Bayes** algorithm to predict political party affiliation (Democrat or Republican). The project features a custom-built **Ensemble Method** to aggregate predictions across multiple data subsets.

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

## 📁 Repository Contents
* `naive_bayes_analysis.Rmd`: The full source code and ensemble logic.
* `README.md`: Project documentation.

## 🚀 How to Run
1. Clone the repository.
2. Install the necessary R packages:
   ```r
   install.packages(c("e1071", "caret", "dplyr", "gmodels"))
