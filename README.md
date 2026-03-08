# Fake News Detection with NLP and Machine Learning

This project investigates whether machine learning models can detect fake news using only textual features from news articles.  
It combines natural language processing (NLP), sentiment analysis, and supervised learning models to classify news as **real** or **fake**.

## Dataset

Fake and Real News Dataset (Kaggle)

- Total articles: **44,919**
- Fake news: **23,502**
- Real news: **21,417**

Each article includes:
- title
- text
- subject
- publication date

Title and text were used for modeling, while subject and date were used for exploratory analysis.

## Methodology

### Data preprocessing
- Lowercasing
- Stopword removal
- Punctuation removal
- Tokenization
- Lemmatization

### Feature extraction
- TF-IDF: Measures the importance of words in documents.
- Sentence Transformers (SBERT): Captures semantic meaning using sentence embeddings.
- VADER sentiment analysis: Measures emotional tone in headlines and article text.

### Models
- Logistic Regression
- Decision Tree
- Support Vector Machine (SVM)

Hyperparameter tuning was performed using **GridSearch with 10-fold cross-validation**.  
Data split: **80% training / 20% testing**.

## Results (Accuracy)
The strongest performance was achieved using TF-IDF features with Decision Tree and SVM models.

- Logistic Regression **97%**
- Decision Tree **99%**
- Support Vector Machine **99%**

Key findings from the Exploratory Data Analysis:

- Fake news headlines show **more negative sentiment**
- Fake news titles contain **more sensational language**
- Fake news is strongly associated with **political topics**
- Fake news spikes around **major political events**

This project was developed as part of the course DATA 6505: Data Munging with Python.
