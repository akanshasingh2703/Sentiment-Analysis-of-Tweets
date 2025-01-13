# Sentiment Analysis of Tweets

## Overview
This project focuses on sentiment analysis of tweets, classifying them as either positive or negative. Sentiment analysis, also known as opinion mining, is a sub-field of natural language processing (NLP) aimed at detecting and analyzing the emotional tone behind a series of words. It is widely used to understand customer feedback, social media reactions, and public sentiment.

## Dataset
The dataset used in this project is a preprocessed version of the Sentiment140 dataset, which contains 1.6 million labeled tweets. Each tweet is labeled with a target sentiment:

- **0**: Negative sentiment
- **4**: Positive sentiment

The dataset includes the following columns:
- `target`: Sentiment label (0 for negative, 4 for positive)
- `id`: Unique ID for each tweet
- `date`: Date and time the tweet was posted
- `flag`: Query information (not used in analysis)
- `user`: Username of the person posting the tweet
- `text`: The content of the tweet

## Models Used
The following machine learning models were applied to perform sentiment classification:
1. **Logistic Regression**: A baseline model used for text classification tasks.
2. **Random Forest**: An ensemble model using multiple decision trees for classification.
3. **Support Vector Machine (SVM)**: A linear classifier aimed at finding the hyperplane that best separates positive and negative sentiments.
4. **XGBoost**: A gradient boosting model known for its performance and speed, used for classification.

## Model Evaluation
Each model was evaluated based on its accuracy, precision, recall, and F1-score. The models were compared to identify which one performs best in predicting the sentiment of tweets.

### Hyperparameter Tuning
To improve the performance of the models, hyperparameter tuning was done using:
- **RandomizedSearchCV** for tuning Random Forest hyperparameters.
- **GridSearchCV** for tuning SVM parameters.

### Cross-Validation
Cross-validation was used to ensure that the models perform well across different subsets of the dataset, and to avoid overfitting.

### Ensemble Method
An ensemble model using **Voting Classifier** was implemented by combining the predictions of Logistic Regression, Random Forest, SVM, and XGBoost. The ensemble approach aimed to improve model performance by leveraging the strengths of each individual model.

## Results
- **Logistic Regression**: Baseline model, achieving an accuracy of ~80%.
- **Random Forest**: Achieved ~79% accuracy, similar to Logistic Regression.
- **SVM**: Performed similarly to Logistic Regression, with an accuracy of around 80%.
- **XGBoost**: Achieved the highest accuracy at approximately 81%.
- **Ensemble Model**: The Voting Classifier combining all models achieved an accuracy of ~82%.

## Conclusion
This project demonstrates the effectiveness of using various machine learning models for sentiment analysis of tweets. The final ensemble model provided the best performance. Hyperparameter tuning and cross-validation further improved the model's robustness and accuracy.


