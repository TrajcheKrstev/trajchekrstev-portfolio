+++
title = 'News Article Comment Prediction'
draft = false
summary = "This project, completed as part of the **Intro to Data Mining** course, involved developing a predictive model to estimate the number of comments on news articles. The model uses a combination of text processing techniques and machine learning algorithms, leveraging various features extracted from article content and metadata to make accurate predictions."
featured_image = "images/newsArticle.jpg"
+++

### Description

This project, completed as part of the **Intro to Data Mining** course, involved developing a predictive model to estimate the number of comments on news articles. The model uses a combination of text processing techniques and machine learning algorithms, leveraging various features extracted from article content and metadata to make accurate predictions.

### Code Overview

The project utilizes several Python libraries, including `scikit-learn`, `pandas`, and `nltk`for text processing, feature extraction, and model training. Below is a high-level overview of the key components of the code:

1. **Data Reading and Preprocessing:**

   - `read_json(data_path: str) -> list`: Reads compressed JSON data files.
   - `preprocess_text(text)`: Processes text by tokenizing, removing punctuation, stopwords, and lemmatizing words.
   - `combine_figure_captions(figures)`: Combines captions from figure data into a single text string.
   - `get_one_hot_encoded(data, data_type, column)`: Encodes categorical data as one-hot vectors.

2. **Model Training:**

   - `fit(train_data: list)`: Trains the model using the training data. The process includes text preprocessing, feature extraction, TF-IDF vectorization, and model fitting using Ridge regression.

3. **Prediction:**

   - `predict(test_data: list) -> np.array`: Predicts the number of comments for the test data based on the trained model.

### Summary

#### Data Preprocessing

1. **Data Aggregation:**

   - Combined all paragraphs, keywords, and figure captions into single strings.
   - Extracted `hour` and `day_of_week` from the `date` column.
   - Counted the number of paragraphs and figures in each article.

2. **Text Cleaning:**

   - Converted text to lowercase.
   - Tokenized text into words.
   - Removed punctuation and stopwords.
   - Lemmatized words.
   - Processed URLs to extract subtopics.

3. **Feature Engineering:**
   - Created a combined text field from the cleaned title, lead, and paragraphs.
   - Used TF-IDF vectorization for text features.
   - One-hot encoded categorical features such as subtopics, authors, topics, and day of the week.
   - Normalized continuous features like article length and publication hour.

#### Model Building

- **Model Choice:** Used Ridge regression due to its balance of simplicity and performance.
- **Features:** Combined text and numerical features including:
  - TF-IDF vectorized text.
  - One-hot encoded subtopics, authors, topics, and day of the week.
  - Article length, number of figures, and number of paragraphs.
  - Publication hour.
- **Normalization:** Applied standard scaling to continuous features.

#### Model Evaluation

- Trained the model to predict the square root of the number of comments to improve the Mean Absolute Error (MAE).
- Experimented with various models and feature combinations, ultimately finding Ridge regression to be the best performing model in terms of speed and accuracy.

[Github Repository](https://github.com/TrajcheKrstev/comment_prediction/tree/main)
