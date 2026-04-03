# Mushroom Classification using Naive Bayes (From Scratch)

## Overview

This project implements a Naive Bayes classifier from scratch to classify mushrooms as edible or poisonous using a dataset of categorical features.

## Dataset

- File: mushrooms.csv
- Each row represents a mushroom sample
- Features are categorical attributes (converted into numeric form using Label Encoding)

## Preprocessing

- Label Encoding is applied to convert all categorical values into integers
- Dataset is split into features (X) and target (y)
- Train-test split: 80% training, 20% testing

## Model: Naive Bayes (Manual Implementation)

The model is built from scratch using probability concepts:

### 1. Prior Probability

Probability of each class:
P(Class) = count(class) / total samples

### 2. Likelihood (Conditional Probability)

Probability of feature given class:
P(X|Class)

Computed by counting occurrences of feature values within each class.

### 3. Posterior Probability

P(Class|X) ∝ P(X|Class) \* P(Class)

Prediction is made by selecting the class with the highest posterior probability.

## Prediction Function

- Calculates posterior probability for each class
- Multiplies likelihoods across all features
- Chooses class with maximum probability

## Evaluation

- Accuracy is calculated on the test set
- Compares predicted labels with actual labels

## Output Example

Accuracy: 99.6308%

## Libraries Used

- pandas
- numpy
- scikit-learn

## Purpose

- Understand Naive Bayes mathematically
- Implement probabilistic classification without using built-in models
