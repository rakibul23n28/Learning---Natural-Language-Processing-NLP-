# NLP Text Preprocessing Pipeline

## Overview

This project demonstrates a simple NLP preprocessing pipeline using the 20 Newsgroups dataset. The goal is to clean and normalize raw text data for machine learning tasks.

## Dataset

- Source: sklearn.datasets.fetch_20newsgroups
- Used first 4 documents for demonstration

## Steps

1. Lowercasing  
   Convert all text to lowercase for consistency.

2. Tokenization

- Sentence tokenization using sent_tokenize
- Word tokenization using word_tokenize

3. Cleaning (Regex)  
   Remove non-alphabetic characters (numbers, punctuation).

4. Stopword Removal  
   Remove common words like "the", "is", "and".

5. Stemming  
   Reduce words to root form using PorterStemmer.  
   Example: playing → play

6. Lemmatization  
   Convert words to dictionary base form using WordNetLemmatizer.  
   Example: running → run

## Output

- clean_text_5 → stemmed text
- lem → lemmatized text

## Libraries Used

- sklearn
- nltk
- numpy
- re

## Purpose

Prepare text data for tasks like:

- Text classification
- Sentiment analysis
- Machine learning models
