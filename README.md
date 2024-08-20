# Hate Speech Detection in English

## Overview

This project explores the detection of hate speech in English text using machine learning and natural language processing (NLP) methods. The objective is to develop a model that accurately distinguishes between hate speech and non-hate speech in a collection of tweets. By leveraging feature extraction techniques and applying a logistic regression model, this project demonstrates an efficient approach to identifying harmful language in online communications.

## Project Motivation

The increasing use of social media platforms has amplified the spread of harmful and hateful content. Monitoring and mitigating hate speech has become a critical issue for maintaining a safe and respectful online environment. This project was initiated to build an automated system capable of detecting such content and reducing the human burden of content moderation.

## Methodology

### Data Collection

- **Dataset**: The dataset comprises over 31,000 tweets labeled as either "hate speech" or "non-hate speech." The labels were derived from manual annotations, enabling the supervised learning model to be trained with reliable data.

### Data Preprocessing

Several preprocessing steps were applied to the raw tweets to prepare them for modeling:

1. **Text Cleaning**: Removal of URLs, special characters, hashtags, and mentions.
2. **Tokenization**: Breaking down the tweets into individual words.
3. **Lowercasing**: Converting all text to lowercase for uniformity.
4. **Stopwords Removal**: Eliminating common stopwords (e.g., "and," "the") that do not contribute to meaning.
5. **Lemmatization**: Reducing words to their base forms to normalize variations (e.g., "running" becomes "run").

### Feature Engineering

- **TF-IDF Vectorization**: Text data was transformed into numerical features using Term Frequency-Inverse Document Frequency (TF-IDF) vectorization. This technique assigns weights to words based on their frequency in a document and their rarity across all documents, making it effective for identifying important terms.

### Model Development

- **Logistic Regression**: A logistic regression classifier was used to predict whether a tweet contains hate speech or not. The simplicity and interpretability of logistic regression make it a suitable choice for binary classification problems.
  
### Model Evaluation

- **Accuracy**: The model was evaluated using accuracy as a performance metric, providing insights into its correctness in classifying tweets.
- **Confusion Matrix & Classification Report**: These tools were used to assess the model's precision, recall, and F1-score, further revealing its strengths and areas for improvement in distinguishing hate speech from non-hate speech.

## Results

The hate speech detection model yielded the following results on the test set:

- **Accuracy**: 94.89%
- **Precision**: 
  - Class 0 (Non-hate speech): 0.95
  - Class 1 (Hate speech): 0.94
- **Recall**: 
  - Class 0 (Non-hate speech): 1.00
  - Class 1 (Hate speech): 0.29
- **F1-Score**: 
  - Class 0 (Non-hate speech): 0.97
  - Class 1 (Hate speech): 0.44

The model effectively identified non-hate speech but showed limitations in recalling hate speech. This suggests room for improvement in detecting hate speech more accurately.

## Insights & Conclusion

The project shows that machine learning models, combined with appropriate NLP techniques, can play a significant role in combating hate speech. While the logistic regression model performs well, further improvements can be made by experimenting with more advanced models such as support vector machines, random forests, or deep learning architectures.

This system can be further extended to other languages and integrated into real-time applications for better online content moderation.
