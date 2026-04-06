# NLP Preprocessing and Text Classification Assignment

## Overview
This notebook demonstrates a complete workflow for text classification, from data loading and preprocessing to model training and evaluation. The primary goal is to classify newsgroup documents into predefined categories using various Natural Language Processing (NLP) techniques and a Multinomial Naive Bayes classifier.

## Objective
The main objectives of this assignment were:
1.  **Load and explore** a text dataset.
2.  Implement comprehensive **NLP preprocessing** steps.
3.  Perform **text vectorization** using different techniques.
4.  **Train and evaluate** a text classification model.

## Dataset
We utilized a subset of the **20 Newsgroups dataset**, a classic dataset for text classification. The specific categories chosen for this assignment were:
*   `alt.atheism`
*   `soc.religion.christian`
*   `comp.graphics`
*   `sci.med`

The dataset was split into training and testing sets, with approximately 2257 training samples and 1502 test samples across these four categories.

## NLP Preprocessing
The following steps were applied to clean and prepare the text data:
1.  **Text Cleaning**: Removal of special characters and numbers, followed by conversion to lowercase.
2.  **Tokenization**: Breaking down text into individual words or tokens.
3.  **Stopword Removal**: Eliminating common words (e.g., 'the', 'is') that generally do not contribute much to the meaning of a text.
4.  **Lemmatization**: Reducing words to their base or dictionary form (e.g., 'running' becomes 'run', 'better' becomes 'good').

## Text Vectorization
After preprocessing, the text data was converted into numerical features using two popular vectorization techniques:
1.  **CountVectorizer**: Transforms text into a matrix where each entry represents the frequency of a word in a document.
2.  **TF-IDF Vectorizer**: Converts text into a matrix where values reflect the Term Frequency-Inverse Document Frequency (TF-IDF) score, indicating the importance of a word in a document relative to the entire corpus.

## Classification Model
A **Multinomial Naive Bayes (MNB)** classifier was chosen for this task. MNB is a probabilistic algorithm well-suited for text classification due to its effectiveness with discrete features like word counts.

## Model Evaluation
The models were evaluated using the following metrics:
*   **Accuracy**: Proportion of correctly classified instances.
*   **Precision**: Proportion of true positive predictions among all positive predictions.
*   **Recall**: Proportion of true positive predictions among all actual positives.
*   **F1-Score**: Harmonic mean of precision and recall.
*   **Confusion Matrix**: A visual representation of the model's performance, showing true vs. predicted labels.

## Key Results
*   **CountVectorizer + MNB Model**:
    *   Accuracy: ~0.9414
    *   Precision: ~0.9415
    *   Recall: ~0.9414
    *   F1-Score: ~0.9413

*   **TF-IDF Vectorizer + MNB Model**:
    *   Accuracy: ~0.8901
    *   Precision: ~0.9042
    *   Recall: ~0.8901
    *   F1-Score: ~0.8901

The model trained with **CountVectorizer features generally performed slightly better** on this dataset compared to the TF-IDF vectorizer, achieving higher accuracy and other metrics.
