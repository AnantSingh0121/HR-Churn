# Employee Attrition (Churn) Analysis

This project analyzes employee attrition (churn) using the dataset `final.csv`. The analysis includes data preprocessing, feature selection, predictive modeling and evaluation of model performance.

---

## Project Overview

The main objectives of this project are:

* Normalize and preprocess the dataset.
* Identify important features using **Boruta**.
* Build predictive models using:

  * **Logistic Regression**
  * **Decision Trees**
  * **Random Forest**
* Evaluate model performance using:

  * **Accuracy**
  * **Confusion Matrix**
  * **ROC Curve & AUC**
  * **Lift Charts**

---

## Dataset

* File: `final.csv`
* Description: Contains employee data with variables such as:

  * `left` (attrition/churn: 0 = stayed, 1 = left)
  * `satisfactionlevel`
  * `lastevaluation`
  * `numberproject`
  * `averagemontlyhours`
  * `timespendcompany`
  * `Workaccident`
  * `promotionlast5years`

---

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/<username>/Employee-Churn-Analysis.git
cd Employee-Churn-Analysis
```

2. Open the project in **RStudio**.

3. Install required R packages if not already installed:

```r
install.packages(c("Boruta", "ROCR", "rpart", "rpart.plot", "randomForest", "caret", "rattle", "party", "partykit"))
```

4. Open `Churn.Rmd` and run the notebook.

---

## Workflow

1. **Data Preprocessing**

   * Normalized numeric variables using a custom function.
   * Handled missing values and converted the target variable `left` to factor.

2. **Feature Selection**

   * Used `Boruta` to identify important predictors.

3. **Logistic Regression**

   * Trained logistic regression model.
   * Evaluated using confusion matrix, accuracy, ROC curve, AUC and lift charts.

4. **Decision Tree**

   * Built a classification tree using `rpart`.
   * Visualized using `rpart.plot`.
   * Calculated accuracy and misclassification rate.

5. **Random Forest**

   * Trained a random forest classifier using `randomForest`.
   * Evaluated variable importance with `importance()` and `varImpPlot()`.
   * Achieved high accuracy on the validation set.

---

## Results

* **Random Forest Accuracy:** ~0.985
* **Logistic Regression ROC AUC:** 0.813
* Most important features:

  * `satisfactionlevel`
  * `numberproject`
  * `timespendcompany`
  * `averagemontlyhours`
  * `lastevaluation`
  * `Workaccident`
  * `promotionlast5years`

---

## Plots

* ROC Curve
* Lift Chart
* Decision Tree Visualization
* Random Forest Variable Importance Plot

---

This project is licensed under the MIT License.
