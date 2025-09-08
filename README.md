# NLP-FOR-TEXT-CLASSIFICATION
NLP project to classify SMS messages as spam or ham using TF-IDF and Multinomial Naive Bayes. Includes text preprocessing, feature extraction, and model evaluation. Achieved high accuracy in spam detection.

# Dataset
1.  Dataset Used: SMS Spam Collection Dataset
2. 	Contains 5,574 SMS messages labelled as:
o	ham (legitimate message)
o	spam (advertisement, fraud, etc.)

# Processing Steps
1.	Text Cleaning: Lowercasing, punctuation removal, and stopword removal.
2.	Vectorization: TF-IDF (Term Frequency–Inverse Document Frequency).
3.	Model Used: Logistic Regression.
4.	Train/Test Split: 80% training, 20% testing.

# Achieved Performance 
1. 	Accuracy: ~97–98%
2.  Precision (Spam class): ~94–96%
3.	Recall (Spam class): ~85–90%
4.	F1-score (Spam class): ~90–92%
5. 	Ham messages are classified very well (≈99% recall).
6.	Spam messages are slightly harder, with some false negatives.
   
# Analysis
1.	High Accuracy : The classifier is very effective for spam filtering.
2.	Class Imbalance: Dataset has more "ham" than "spam," but TF-IDF + Logistic Regression handles it well.
3.	Errors: Most mistakes come from borderline cases (e.g., promotional messages that look legitimate).
4.	Confusion Matrix Insight:
5 	Few ham → spam misclassifications.
6 	More spam → ham misclassifications (model sometimes misses spam).
  	
# Conclusion
1. 	The model is robust and efficient for spam detection.
2.	Could be further improved with:
3. 	Advanced models (e.g., LSTMs, Transformers).
4.	Handling class imbalance (SMOTE, class weights).
5. 	Including additional linguistic/semantic features.

