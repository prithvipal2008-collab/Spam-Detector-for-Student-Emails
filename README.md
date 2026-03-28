# 📧 Spam Detector for Student Emails

A Natural Language Processing (NLP) project that classifies email/SMS messages as **Spam** or **Ham (Not Spam)** using a Naive Bayes classifier trained on TF-IDF features.

Built as part of the **Fundamentals of AI and ML** course — Bring Your Own Project (BYOP).

---

## 🧠 What This Project Does

Students receive dozens of emails daily — from professors, classmates, and unfortunately, spammers. This project builds an ML model that:

- Reads and preprocesses text messages
- Converts text into numerical features using **TF-IDF**
- Trains a **Multinomial Naive Bayes** classifier
- Evaluates the model using accuracy, precision, recall, and a confusion matrix
- Lets you type any message and instantly predicts whether it is spam or not

---

## 📁 Project Structure

```
spam-detector/
│
├── spam_detector.py        # Main Python script
├── requirements.txt        # Python dependencies
├── README.md               # This file
├── SMSSpamCollection       # Dataset file (download separately — see below)
├── eda_analysis.png        # Generated: EDA chart (after running)
└── confusion_matrix.png    # Generated: Confusion matrix (after running)
```

---

## 🚀 How to Set It Up

### 1. Clone the Repository

```bash
git clone https://github.com/prithvipal2008-collab/spam-detector-student-emails.git
cd spam-detector-student-emails
```

### 2. Install Dependencies

Make sure you have Python 3.7+ installed. Then run:

```bash
pip install -r requirements.txt
```

### 3. Download the Dataset (Optional but Recommended)

The script works with a built-in sample dataset by default.

For full accuracy, download the **SMS Spam Collection Dataset**:

- Source: [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection)
- Place the file named `SMSSpamCollection` (no extension) in the project folder.

---

## ▶️ How to Run

```bash
python spam_detector.py
```

The script will:
1. Load the dataset
2. Show exploratory data analysis and save a chart
3. Preprocess text and extract TF-IDF features
4. Train the Naive Bayes model
5. Print evaluation metrics and save a confusion matrix
6. Let you test your own messages interactively

---

## 💬 Interactive Demo

After the model trains, you can type any message:

```
Enter message (or 'quit'): Congratulations! You've won a FREE iPhone!
Result  : 🚨 SPAM  (Confidence: 98.3%)

Enter message (or 'quit'): Hey, can we meet at 5 PM for the project?
Result  : ✅ HAM (Not Spam)  (Confidence: 96.7%)
```

---

## 📊 Sample Results

| Metric    | Score     |
|-----------|-----------|
| Accuracy  | ~97%      |
| Precision | ~97%      |
| Recall    | ~97%      |
| F1 Score  | ~97%      |

*(Results may vary based on whether the full dataset or sample data is used)*

---

## 🔧 Concepts Used

| Concept               | Tool / Technique               |
|-----------------------|-------------------------------|
| Text Preprocessing    | Python `re`, `string` modules |
| Feature Extraction    | TF-IDF (`TfidfVectorizer`)    |
| ML Model              | Multinomial Naive Bayes       |
| Model Evaluation      | Accuracy, F1, Confusion Matrix|
| Data Visualization    | Matplotlib, Seaborn           |
| Data Handling         | Pandas, NumPy                 |

---

## 📚 Course

**Fundamentals of AI and ML**
Bring Your Own Project (BYOP) Submission
VIT — VITyarthi Platform

---

## 👤 Author

Prithvi Pal
25BCE11284
