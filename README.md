# Amazon-Review-Classification

This repository contains the code and resources used for classification of Amazon reviews based on their review text. 

## Key Takeaways

- **Natural Language Processing**: Bi-grams and monograms were used to process review text, yielding a feature space which spanned every single word and 2-word phrase that was used in any of the reviews. Term frequency was calculated from this feature space and sentiment was determined from the original text, creating additional variables each model could consider.
- **Model Prediction Aggregation**: A Support Vector Machine, Ridge Classifier and Naive Bayes model were all used for multiclass classification to determine which class of scores a review belonged to, from one to five stars. The average prediction score of each model was aggregated to determine the most likely class. Models were chosen primarily because of their computational efficiency, as the data spanned thousands of reviews and tens of thousands of features. 
- **Model Assessment**: Five Receiver Operating Characteristic (ROC) curves were generated for each model to evaluate their predictive performances. Each curve represents the ability of the model to classify one categorical outcome, specifically a review's rating ranging from 1 to 5 stars. The Area Under the Curve (AUC) was used to summarize the performance of each ROC curve. F1 score and accuracy were calculated to summarize the performance of each model across all 5 classes.

## Notable Dependencies
- `CountVectorizer` from `sklearn.feature_extraction.text`
- `SentimentIntensityAnalyzer` from `vaderSentiment.vaderSentiment`
- `MultinomialNB`, `LinearSVC` and `RidgeClassifier` from `sklearn`
