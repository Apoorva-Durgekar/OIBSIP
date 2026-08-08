# Sentiment Analysis on Product Reviews

**Track:** Data Analytics
**Level:** Level 1 — Task 4
**Internship:** Oasis Infobyte (OIBSIP)

## Objective
Build a machine learning model that classifies the sentiment of text data (positive, negative, or neutral), providing insights into public opinion or customer feedback.

## Dataset
Sample product review dataset (1,200 reviews across positive/negative/neutral classes), included as `sentiment_sample.csv`.
(If using a real Kaggle dataset instead — e.g. Twitter Sentiment Analysis, Amazon Product Reviews, or IMDB Movie Reviews — add the exact Kaggle link here.)

## Tech Stack
- Python
- pandas
- scikit-learn
- NLTK
- WordCloud
- matplotlib / seaborn
- Jupyter Notebook

## What This Project Covers
- Class distribution inspection
- Text preprocessing: lowercasing, punctuation removal, stopword removal, tokenization
- Feature extraction using TF-IDF
- Train/test split (80/20)
- Two trained classifiers: Naive Bayes and Logistic Regression
- Evaluation: accuracy, precision, recall, F1-score, confusion matrices
- Sentiment distribution chart and WordClouds per class
- Error analysis on misclassified examples
- Conclusion on best-performing model and real-world application

## How to Run
1. Clone this repository
2. Navigate to this folder: `OIBSIP/DataAnalytics-L1-SentimentAnalysis/`
3. Install requirements: `pip install pandas scikit-learn nltk wordcloud matplotlib seaborn jupyter`
4. Open the notebook: `jupyter notebook Sentiment_Analysis.ipynb`
5. Run all cells in order (the first NLTK cell downloads required language data automatically)

## Key Findings
- The dataset was moderately balanced across sentiment classes: positive (500), negative (400), and neutral (300) reviews.
- Text preprocessing (lowercasing, punctuation removal, stopword removal) successfully reduced reviews to their core sentiment-bearing keywords.
- Both Naive Bayes and Logistic Regression achieved 100% accuracy, precision, recall, and F1-score on the test set, correctly classifying all 240 test reviews.
- WordCloud analysis confirmed each sentiment class has clearly distinct vocabulary — positive reviews centered on words like "great" and "excellent", negative reviews on "terrible" and "disappointed", and neutral reviews on "okay" and "average".

## Best Model & Application
Both Naive Bayes and Logistic Regression performed equally well (100% accuracy) on this dataset. In practice, Logistic Regression is generally preferred for production deployment due to its better-calibrated probability outputs, while Naive Bayes offers faster training as a lightweight baseline.
This pipeline could be applied in a real-world setting to automatically classify incoming customer reviews or social media mentions, flagging negative feedback for priority customer support follow-up, or tracking brand sentiment trends over time.

## Author
Apoorva
