 ## Disease Prediction Using Machine Learning

This project focuses on predicting various diseases based on a given set of symptoms using several machine learning classification algorithms. The goal is to build robust models that can accurately identify the disease from symptomatic data.

## Introduction
Accurate and early disease prediction can significantly improve healthcare outcomes. This project leverages machine learning techniques to develop a predictive model that takes patient symptoms as input and outputs a likely disease prognosis. We explore multiple classification algorithms to determine the most effective approach.

## Dataset
The dataset used in this project consists of:
- **`Training.csv`**: Contains symptom data and corresponding disease prognoses for model training.
- **`Testing.csv`**: Contains unseen symptom data for evaluating the trained models.

Each row represents a patient, and columns represent symptoms (binary: 1 if present, 0 if absent) and the target 'prognosis' (disease name).

## Preprocessing
The following preprocessing steps were applied to the data:
1.  **Missing Value Handling**: The 'Unnamed: 133' column in the training data, which contained only `NaN` values, was dropped.
2.  **Duplicate Removal**: Duplicate rows in the training dataset were removed to prevent data leakage and improve model generalization.
3.  **Label Encoding**: The categorical 'prognosis' column (target variable) was transformed into numerical labels using `sklearn.preprocessing.LabelEncoder` to make it suitable for machine learning algorithms.

## Exploratory Data Analysis (EDA)
EDA was performed to understand the dataset characteristics:
-   **Distribution of Prognoses**: Visualized the frequency of each disease in the training set.
-   **Top 20 Most Frequent Symptoms**: Identified and plotted the most common symptoms.
-   **Feature Correlation Heatmap**: A heatmap was generated to show the correlation between different symptoms.

## Models Used
Several classification models were trained and evaluated:
-   **RandomForestClassifier**
-   **LogisticRegression**
-   **DecisionTreeClassifier**
-   **Support Vector Machine (SVC)**
-   **Gaussian Naive Bayes**
-   **XGBoost Classifier**

## Results
The models were evaluated based on their accuracy on the test set. Here's a summary of their performance:

| Model                  | Accuracy |
|:-----------------------|:---------|
| RandomForestClassifier | 1.00000  |
| SVC                    | 1.00000  |
| GaussianNB             | 1.00000  |
| LogisticRegression     | 0.97619  |
| DecisionTreeClassifier | 0.97619  |
| XGBoostClassifier      | 0.97619  |

**RandomForestClassifier**, **SVC**, and **Gaussian Naive Bayes** achieved perfect accuracy on the given test set. A prediction example with the RandomForestClassifier was demonstrated.


