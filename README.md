# 📩 SMS Spam Detection — NLP Text Classification

A Natural Language Processing (NLP) project that classifies SMS messages as **Ham (legitimate)** or **Spam** using TF-IDF vectorization and Logistic Regression. Built and evaluated in Google Colab.

---

## 📊 Results at a Glance

| Metric | Ham | Spam |
|---|---|---|
| Precision | 0.96 | 0.97 |
| Recall | 1.00 | 0.72 |
| F1-Score | 0.98 | 0.83 |
| **Overall Accuracy** | **96%** | |
| **ROC AUC** | **0.99** | |

---

## 📸 Output Visualizations

### Distribution of Ham vs Spam
![Ham vs Spam Distribution](https://github.com/29Rajeswari/NLP-FOR-TEXT-CLASSIFICATION/blob/main/ham_vs_spam.png))

### Confusion Matrix & ROC Curve
![Confusion Matrix and ROC Curve](https://github.com/29Rajeswari/NLP-FOR-TEXT-CLASSIFICATION/blob/main/confusion_roc.png))

### Spam & Ham WordClouds
![WordClouds](https://github.com/29Rajeswari/NLP-FOR-TEXT-CLASSIFICATION/blob/main/wordclouds.png))

---

## 🗂️ Project Structure

```
SMS-Spam-Detection/
│
├── sms_spam_detection.ipynb     # Main Colab notebook
├── ham_vs_spam.png              # Class distribution chart
├── confusion_roc.png            # Confusion matrix + ROC curve
├── wordclouds.png               # Spam & Ham word clouds
└── README.md
```

---

## 🎯 Objective

Detect whether an SMS message is **spam** or **ham** by:
- Cleaning and preprocessing raw text
- Extracting features using **TF-IDF**
- Training a **Logistic Regression** classifier
- Evaluating with confusion matrix, ROC curve, and classification report

---

## 🔄 Project Workflow

```
Raw SMS Data
     │
     ▼
Text Preprocessing
(lowercase → remove punctuation → remove stopwords)
     │
     ▼
TF-IDF Vectorization
     │
     ▼
Logistic Regression Model
     │
     ▼
Evaluation (Accuracy, F1, ROC-AUC)
     │
     ▼
Predict on New Messages
```

---

## 🗃️ Dataset

| Property | Details |
|---|---|
| Source | [SMS Spam Collection — UCI / Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset) |
| Total Messages | 5,572 |
| Ham Messages | ~4,825 (86%) |
| Spam Messages | ~747 (14%) |
| Features | Raw SMS text |
| Target | `ham` / `spam` |

---

## 🧹 Text Preprocessing Steps

1. Convert to **lowercase**
2. Remove all **punctuation**
3. **Tokenize** the text
4. Remove **English stopwords** (via NLTK)
5. Join tokens back into a clean string

```python
def clean_text(text):
    text = text.lower()
    text = ''.join(ch for ch in text if ch not in string.punctuation)
    tokens = text.split()
    tokens = [word for word in tokens if word not in stopwords.words('english')]
    return ' '.join(tokens)
```

---

## 🤖 Model Details

| Component | Details |
|---|---|
| Vectorizer | TF-IDF (Term Frequency–Inverse Document Frequency) |
| Classifier | Logistic Regression |
| Train/Test Split | 80% / 20% |
| Random State | 42 |

---

## 🔍 Sample Predictions

| Message | Prediction |
|---|---|
| "Congratulations! You've won a $1000 gift card. Claim now!" | ➡ Ham ⚠️ |
| "Are you coming to the meeting today?" | ➡ Ham ✅ |
| "Urgent: Your account is suspended. Click to reactivate." | ➡ Ham ⚠️ |

> Note: The model predicted all 3 as Ham — spam-like phishing messages can sometimes bypass simple TF-IDF models. Adding more training data or using deep learning (LSTM/BERT) would improve detection of borderline cases.

---

## 📦 Dependencies

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Plotting charts |
| `seaborn` | Heatmap (confusion matrix) |
| `wordcloud` | Spam & Ham word cloud visualization |
| `nltk` | Stopword removal |
| `sklearn` | TF-IDF, Logistic Regression, metrics |
| `kagglehub` | Dataset download from Kaggle |

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)

1. Open the notebook in [Google Colab](https://colab.research.google.com/)
2. Click **Runtime → Run All**
3. Dataset loads automatically via URL — no manual download needed

### Option 2 — Local Setup

```bash
# Clone the repo
git clone https://github.com/29Rajeswari/SMS-Spam-Detection.git
cd SMS-Spam-Detection

# Install dependencies
pip install pandas numpy matplotlib seaborn wordcloud nltk scikit-learn kagglehub

# Run notebook
jupyter notebook sms_spam_detection.ipynb
```

---

## 💡 Possible Improvements

- Use **Multinomial Naive Bayes** (classic baseline for text classification)
- Try **Random Forest** or **XGBoost** for better spam recall
- Apply **SMOTE** to handle class imbalance (86% ham vs 14% spam)
- Use **LSTM** or **BERT** for deep learning–based classification
- Add **n-grams** (bigrams/trigrams) to TF-IDF for richer features

---

## 👤 Author

**Rajeswari**
🔗 GitHub: [@29Rajeswari](https://github.com/29Rajeswari)

---

> **Dataset:** SMS Spam Collection — UCI Machine Learning Repository, available on [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
