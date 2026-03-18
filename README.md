# NBA Shot Selection Prediction

## Project Overview

This project focuses on predicting whether an NBA shot attempt will be successful using machine learning techniques. The model leverages shot-level data, player information, and game context to estimate scoring probability.

In addition to traditional supervised learning, this project incorporates **semi-supervised learning techniques** to utilize both labeled and unlabeled data, improving model performance and generalization.

---

## Problem Statement

In basketball analytics, shot selection plays a crucial role in team performance. Understanding the probability of a successful shot helps coaches and players make better strategic decisions.

The objective of this project is to build a predictive model that determines whether a shot will result in a score based on various features such as distance, location, and game situation.

---

## Dataset Description

The dataset contains detailed information about each shot attempt, including:

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

The project follows a structured machine learning pipeline:

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

This project uses **semi-supervised learning** to improve performance by leveraging unlabeled data.

### Approach:

* Train an initial model on labeled data
* Predict pseudo-labels for unlabeled data
* Combine labeled and pseudo-labeled data
* Retrain the model

This method helps improve generalization when labeled data is limited.

---

## Feature Engineering

Important features used in the model include:

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

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score

---

## Key Insights

* Shot distance is a major factor affecting success rate
* Shots closer to the basket have higher success probability
* Three-point shots have lower success rates but higher reward
* Semi-supervised learning improves model performance by utilizing additional data

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

## Project Structure

nba-shot-selection-prediction

├── README.md
├── requirements.txt
├── data/
├── notebooks/
├── src/
├── models/
└── reports/

---

## Results

The machine learning models successfully capture patterns in shot selection and scoring probability. The inclusion of semi-supervised learning enhances performance by leveraging additional unlabeled data.

---

## Future Improvements

* Advanced feature engineering (court zones, tracking data)
* Deep learning models
* Real-time prediction systems
* Interactive dashboards

---

## Conclusion

This project demonstrates how machine learning and semi-supervised learning techniques can be applied to sports analytics. It provides valuable insights into shot selection and helps improve decision-making in basketball.



