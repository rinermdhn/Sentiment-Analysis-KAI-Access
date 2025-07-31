# Sentiment-Analysis-KAI-Access

🚅 This project performs sentiment analysis on user reviews of the *Access by KAI* application, scraped from *Google Play Store*. It involves processing unstructured textual data and compares the performance of **Random Forest** and **Naive Bayes** classifiers in sentiment classification. The pipeline includes data scraping, manual sentiment labeling, data preprocessing, sentiment analysis, and model evaluation to determine the most effective classification approach.

## Features
- `userName`: The username of the individual who submitted the review.
- `content`: The actual review text, which may include expressions of dissatisfaction, complaints, appreciation, gratitude, suggestions, criticism, and more.
- `score`: A numerical rating (1–5) given by the user to the application.
- `sentiment`: A sentiment label assigned to the review, categorized as positive or negative.

## Methodology
### Data Scraping
The dataset comprises **2,000 reviews** scraped from Google Play Store using `google_play_scraper`. Sentiment labels (positive or negative) were manually assigned based on the corresponding rating scores.

### Data Preprocessing
1. **Case-folding**: Converting all characters in the reviews to lowercase.
2. **Data Cleaning**: Removing emojis, hashtags, numbers, punctuation, repeated words, and excessive whitespace.
3. **Tokenizing**: Splitting the review into tokens.
4. **Filtering**: Removing stopwords to retain only meaningful terms.
5. **Stemming**: Reducing inflected or derived words to their root form.

### Sentiment Analysis
- **Modelling**: Random Forest and Naive Bayes.
- **Model Development**: 5-fold cross-validation.
- **Hyperparameter Tuning**: Grid Search.
- **Model Evaluation**: Confusion Matrix.

## Results
### Random Forest
- **Accuracy**: 0.89 — 89% of the data were correctly classified. This reflects a generally strong performance.
- **Confusion Matrix**
  - **True Negative**: 889.
  - **False Positive**: 78.
  - **True Positive**: 537.
  - **False Negative**: 96.

### Naive Bayes
- **Accuracy**: 0.87 — 87% of the data were correctly classified. This reflects a generally strong performance.
- **Confusion Matrix**
  - **True Negative**: 214.
  - **False Positive**: 16.
  - **True Positive**: 135.
  - **False Negative**: 35.

## Conclusion
Based on the **Accuracy** scores, the Random Forest model **outperformed** Naive Bayes in classifying user review sentiments for the Access by KAI application. Random Forest achieved an accuracy of **89%**, while Naive Bayes showed a slightly lower accuracy of **87%**.
