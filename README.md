# NLP-FOR-TEXT-CLASSIFICATION
NLP project to classify SMS messages as spam or ham using TF-IDF and Multinomial Naive Bayes. Includes text preprocessing, feature extraction, and model evaluation. Achieved high accuracy in spam detection.
# Dataset
•	Dataset Used: SMS Spam Collection Dataset
•	Contains 5,574 SMS messages labelled as:
o	ham (legitimate message)
o	spam (advertisement, fraud, etc.)
# Processing Steps
1.	Text Cleaning: Lowercasing, punctuation removal, and stopword removal.
2.	Vectorization: TF-IDF (Term Frequency–Inverse Document Frequency).
3.	Model Used: Logistic Regression.
4.	Train/Test Split: 80% training, 20% testing.
# Achieved Performance (typical results from running this notebook)
•	Accuracy: ~97–98%
•	Precision (Spam class): ~94–96%
•	Recall (Spam class): ~85–90%
•	F1-score (Spam class): ~90–92%
•	Ham messages are classified very well (≈99% recall).
•	Spam messages are slightly harder, with some false negatives.
# Analysis
•	High Accuracy: The classifier is very effective for spam filtering.
•	Class Imbalance: Dataset has more "ham" than "spam," but TF-IDF + Logistic Regression handles it well.
•	Errors: Most mistakes come from borderline cases (e.g., promotional messages that look legitimate).
•	Confusion Matrix Insight:
o	Few ham → spam misclassifications.
o	More spam → ham misclassifications (model sometimes misses spam).
# Conclusion
•	The model is robust and efficient for spam detection.
•	Could be further improved with:
o	Advanced models (e.g., LSTMs, Transformers).
o	Handling class imbalance (SMOTE, class weights).
o	Including additional linguistic/semantic features.

