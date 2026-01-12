# Linear Regression for Binary Classification

## Evaluation and Visualization

**Dataset:** student_mat.csv

---

## 1. Introduction

This project focuses on applying Linear Regression to a binary classification problem using the Student Mat dataset. The goal is to predict student performance by classifying students into two categories based on academic outcomes. Although Linear Regression is mainly used for predicting continuous values, it is adapted here for classification by converting predictions into binary labels using a fixed threshold.

The project is designed as a learning exercise to understand how regression models can be evaluated from a classification perspective, along with proper performance analysis and visualization.

**Objectives:**

* Preprocess and analyze the Student Mat dataset
* Train a Linear Regression model
* Convert regression outputs into binary classes
* Evaluate performance using regression and classification metrics
* Visualize results for better interpretation

---

## 2. Dataset Description

* **Dataset Name:** Student Mat Performance Dataset
* **File Name:** student_mat.csv
* **Domain:** Education

### Key Attributes

* Demographic information
* Study time and attendance
* Academic and personal factors
* Final grade related attributes

The dataset contains both numeric and categorical features, making preprocessing a critical step before model training.

---

## 3. Libraries and Tools Used

* Pandas for data loading and manipulation
* NumPy for numerical operations
* Scikit learn for model training and evaluation
* Matplotlib for visualization
* Seaborn for statistical plots

---

## 4. Data Preprocessing

### 4.1 Binary Target Creation

A binary target variable is created from the final grade by using the median value:

* 1 represents performance above the median
* 0 represents performance below or equal to the median

The target column is named **above_median_performance**.

### 4.2 Feature Selection

* The original grade column is removed from the feature set
* The binary target is separated as y
* Remaining attributes are used as input features X

### 4.3 Handling Categorical and Missing Data

* Categorical features are encoded into numeric form
* Missing values are handled using mean imputation
* All features are converted into a numeric format compatible with Linear Regression

---

## 5. Train Test Split

The dataset is split into:

* Training set: 80 percent
* Testing set: 20 percent
* Random state set for reproducibility

---

## 6. Model Training

A Linear Regression model is trained on the training dataset. The model produces continuous outputs that represent prediction scores rather than direct class labels.

---

## 7. Prediction Strategy

### 7.1 Continuous Predictions

The trained model generates continuous values for each test sample.

### 7.2 Binary Predictions

Predictions are converted into binary labels using a threshold value:

* Values greater than or equal to 0.5 are labeled as 1
* Values below 0.5 are labeled as 0

---

## 8. Evaluation Metrics

### 8.1 Regression Metrics

* Mean Squared Error
* R squared score

### 8.2 Classification Metrics

* Confusion Matrix
* Accuracy
* Precision
* Recall
* F1 Score

These metrics help evaluate the model from both regression and classification viewpoints.

---

## 9. ROC Curve and AUC

The ROC curve is plotted using continuous predictions to analyze the tradeoff between true positive rate and false positive rate. The Area Under the Curve value summarizes the overall classification ability of the model.

---

## 10. Visualizations

### 10.1 Confusion Matrix Heatmap

A heatmap is used to visualize correct and incorrect classifications for both classes.

### 10.2 Classification Metrics Bar Chart

A bar chart compares accuracy, precision, recall, and F1 score to provide a clear performance overview.

---

## 11. Results Summary

* The model shows reasonable recall for identifying high performing students
* Accuracy and precision are moderate
* R squared score is relatively low, highlighting limitations of Linear Regression for classification
* ROC AUC indicates performance slightly better than random guessing

---

## 12. Limitations

* Linear Regression is not ideal for classification tasks
* Threshold based classification can lead to misclassification
* Feature relationships may not be linear

---

## 13. Future Improvements

* Replace Linear Regression with Logistic Regression
* Apply advanced models such as Random Forest or SVM
* Perform feature scaling and hyperparameter tuning
* Improve feature engineering and encoding techniques

