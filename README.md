# Titanic Survival Prediction with Conformal Prediction

## Overview
This project extends classical machine learning classification on the Titanic dataset by applying Conformal Prediction — a framework for uncertainty quantification that provides statistically guaranteed prediction sets.

Unlike standard models that output a single class label, Conformal Prediction outputs a set of plausible labels with a guaranteed coverage rate.

## Project Structure
The notebook is divided into two parts:

Part 1: Classical ML Classification
- Exploratory Data Analysis (EDA)
- Feature engineering
- Logistic Regression vs Decision Tree comparison
- Best accuracy: 79.78% (Decision Tree)

Part 2: Conformal Prediction
- Split Conformal Prediction implemented from scratch
- Non-conformity scores based on class probabilities
- 90% confidence level (alpha = 0.1)
- Empirical coverage: 93.26%

## Key Results
| Method | Metric | Value |
|--------|--------|-------|
| Logistic Regression | Accuracy | 76.40% |
| Decision Tree | Accuracy | 79.78% |
| Conformal Prediction | Coverage | 93.26% |
| Conformal Prediction | Certain predictions | 38.8% |
| Conformal Prediction | Uncertain predictions | 61.2% |

## Dataset
- Source: Stanford University (titanic.csv)
- 887 passengers, 8 features
- No missing values

## Technologies
Python, Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn

## Motivation
Standard ML models predict a single label without indicating confidence. Conformal Prediction addresses this by returning prediction sets with a formal guarantee — the true label is included in the set with at least 90% probability. This connects to the broader field of trustworthy ML and uncertainty quantification.
