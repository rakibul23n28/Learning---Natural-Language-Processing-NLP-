# IMDB Sentiment Analysis using Naive Bayes

## Overview

This project builds a sentiment analysis model to classify movie reviews as positive or negative using the IMDB dataset. It uses Natural Language Processing (NLP) techniques and a Multinomial Naive Bayes classifier.

## Dataset

- File: IMDB Dataset.csv
- Columns:
  - review (text)
  - sentiment (positive/negative)

## Data Preprocessing

### 1. Label Encoding

- Sentiment labels are converted into numeric values:
  - positive → 1
  - negative → 0

### 2. Text Cleaning

Each review is processed using:

- Lowercasing
- Tokenization (RegexpTokenizer)
- Stopword removal
- Stemming (Porter Stemmer)

Function used:
getCleanedData()

## Feature Extraction

### CountVectorizer

- Converts text into numerical features
- Uses n-grams: (1, 2) → unigram + bigram
- Transforms cleaned text into a sparse matrix

## Model

### Multinomial Naive Bayes

- Used for text classification
- Learns probability of words in positive and negative reviews
- Trained using:
  mn.fit(X_cv, y_train)

## Prediction

Steps:

1. Clean test reviews using same preprocessing
2. Convert text into vector form using trained CountVectorizer
3. Predict sentiment using trained model

## Output

- Model predicts sentiment as:
  - 1 → Positive
  - 0 → Negative

## Libraries Used

- numpy
- pandas
- nltk
- scikit-learn

## Purpose

- Perform sentiment analysis on movie reviews
- Understand full NLP pipeline:
  preprocessing → vectorization → classification
