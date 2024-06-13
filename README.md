## <div align="center">Parkinson's Disease UPDRS Score Prediction
## <div align="center">![Intro](images/park.png)

This repository contains the code and data used to predict the Unified Parkinson’s Disease Rating Scale (UPDRS) scores based on voice features. The project aims to compare the performance of various regression models in predicting UPDRS scores and determine the best model for this task.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Models and Methodology](#models-and-methodology)
- [Results](#results)
- [Conclusion](#conclusion)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [License](#license)

## Introduction

Parkinson's disease is a neurodegenerative disorder that affects movement and can significantly impair the quality of life. Accurate prediction of UPDRS scores can help in better understanding the progression of the disease and in developing effective treatment plans.

## Dataset

The dataset consists of various voice features from 20 persons with Parkinson's (6 female, 14 male) and 20 healthy individuals (10 female, 10 male). From all subjects, multiple types of sound recordings (26 voice samples including sustained vowels, numbers, words, and short sentences) are taken. A group of 26 linear and time-frequency based features are extracted from each voice sample. The UPDRS score of each patient, which is determined by an expert physician, is also available in this dataset.

## Models and Methodology

The following models were evaluated:

1. **Multiple Linear Regression (MLR)**
2. **Ridge Regression**
3. **Lasso Regression**
4. **Random Forest Regression**

### Methodology

1. **Data Preparation**: The data was split into training and testing sets.
2. **Model Evaluation**: Each model was trained on the training set and evaluated on the testing set using Mean Squared Error (MSE) as the performance metric.
3. **Hyperparameter Tuning**: GridSearchCV was used to find the best hyperparameters for Ridge, Lasso, and Random Forest models.
4. **Feature Selection**: Correlation-based feature selection was applied to improve the MLR model.

## Results

- **Initial MLR Model**: MSE = 214.19
- **Ridge Regression**: MSE = 212.51
- **Lasso Regression**: MSE = 212.95
- **Random Forest (Tuned)**: MSE = 186.62

## Conclusion

The best Multiple Linear Regression (MLR) model was achieved using Ridge regression with an MSE of 212.51. However, the Random Forest model, especially after hyperparameter tuning, significantly outperformed all MLR models, achieving a much lower MSE of 186.62. This indicates that while Ridge regression is the best MLR model, more complex models like Random Forests offer superior predictive performance for this dataset.

