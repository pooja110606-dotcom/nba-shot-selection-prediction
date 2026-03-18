# NBA Shot Selection Prediction

## Project Overview

This project focuses on predicting whether an NBA shot attempt will be successful using machine learning techniques. The model leverages shot-level data, player information, and game context to estimate scoring probability.

In addition to traditional supervised learning, this project incorporates **semi-supervised learning techniques** to utilize both labeled and unlabeled data, improving model performance and generalization.

---

## Problem Statement

Shot selection is a critical factor in basketball performance. Understanding the probability of a successful shot helps teams optimize offensive strategies and improve decision-making.

The objective of this project is to build a predictive model that determines whether a shot will result in a score based on various features such as distance, location, and game situation.

---

## Dataset Description

The dataset contains detailed shot-level information, including:

* Shot distance
* Shot location (court coordinates)
* Shot type (2PT / 3PT)
* Player information
* Game context (quarter, time remaining, etc.)

### Target Variable

SHOT_RESULT
0 → Missed Shot
1 → Successful Shot

---

## Project Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Data Preprocessing
5. Handling Missing Values
6. Feature Encoding & Scaling
7. Semi-Supervised Learning
8. Model Training
9. Model Evaluation

---

## Semi-Supervised Learning (Key Highlight)

This project uses **semi-supervised learning** to improve model performance by leveraging unlabeled data.

### Approach:

* Train an initial model on labeled data
* Generate pseudo-labels for unlabeled data
* Combine labeled and pseudo-labeled data
* Retrain the model on the expanded dataset

This approach helps improve generalization when labeled data is limited.

---

## Modeling Decisions & Justifications

### Why Semi-Supervised Learning

The dataset contained missing labels for shot outcomes. Instead of discarding unlabeled data, semi-supervised learning was used to leverage both labeled and unlabeled samples.

Pseudo-labeling was applied to maximize data utilization and improve model performance.

---

### Why SMOTE Was Not Used

SMOTE (Synthetic Minority Oversampling Technique) was intentionally not used.

Reason:

* Synthetic samples combined with pseudo-labeled data can introduce noise
* This may negatively affect model performance

Instead, tree-based models (Random Forest, XGBoost) were used as they naturally handle class imbalance.

---

### Why Outliers Were Not Removed

Outliers such as extreme shot distances were retained.

Reason:

* These values represent real-world basketball scenarios
* Removing them would reduce model realism and introduce bias

Keeping outliers ensures better real-world applicability.

---

## Feature Engineering

Key features include:

* Shot distance
* Shot zone
* Shot type (2PT / 3PT)
* Player position
* Game situation

These features significantly influence shot success probability.

---

## Models Used

* Logistic Regression
* Random Forest
* XGBoost
* Semi-Supervised Learning Model

---

## Model Evaluation

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score

---

## Key Insights

* Shot distance is a major factor affecting success rate
* Shots closer to the basket have higher success probability
* Three-point shots have lower success rates but higher reward
* Semi-supervised learning improves performance by utilizing additional data

---

## Technologies Used

Python
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn
XGBoost

---


## Results

The models successfully capture patterns in shot selection and scoring probability. Semi-supervised learning enhances performance by utilizing both labeled and unlabeled data.

---

## Future Improvements

* Advanced feature engineering (court zones, tracking data)
* Deep learning models
* Real-time prediction systems
* Interactive dashboards

---

## Conclusion

This project demonstrates how machine learning and semi-supervised learning techniques can be applied to sports analytics. It provides actionable insights that can improve player performance and team strategies.



