# CodeClauseInternshipProject2

### Project Description

1. **Objective**:
   - Predict the genres of movies based on their plot summaries and additional features (e.g., budget, runtime, vote average).

2. **Dataset**:
   - Combines `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`.
   - Key features used: `overview` (plot summary), `genres`, `budget`, `runtime`, `vote_average`.

3. **Technologies Used**:
   - Python for implementation.
   - NLTK for text preprocessing (lemmatization, stopword removal).
   - Scikit-Learn for feature extraction (TF-IDF), multi-label classification, and evaluation.
   - Pandas and NumPy for data handling.
   - Pickle for model persistence.

4. **Preprocessing**:
   - Text data (`overview`) cleaned using tokenization, lemmatization, and stopword removal.
   - JSON-formatted `genres` column converted to binary multi-label format.
   - Additional numerical features filled or normalized.

5. **Feature Engineering**:
   - Plot summaries converted to numerical features using TF-IDF vectorization.
   - Combined TF-IDF features with numerical features (budget, runtime, vote average).

6. **Model Training**:
   - Multi-label classification handled using `OneVsRestClassifier` with Logistic Regression.
   - Model trained to predict one or more genres for each movie.

7. **Evaluation**:
   - Metrics: Accuracy, precision, recall, and F1-score.
   - Evaluation done on a separate test set.

8. **Model Persistence**:
   - Trained model, TF-IDF vectorizer, and genre label binarizer saved for future predictions.

9. **Prediction**:
   - New movie summaries can be preprocessed and passed through the saved model to predict genres.

10. **Outcome**:
    - Demonstrates the use of NLP and machine learning techniques for multi-label text classification.
