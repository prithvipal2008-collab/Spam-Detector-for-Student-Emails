📧 SMS Spam Classifier
A lightweight machine learning pipeline that classifies SMS messages as spam or ham (not spam) using TF-IDF vectorization and a Multinomial Naive Bayes model.

📁 Project Structure
├── spam.csv          # Dataset file (required)
├── spam_classifier.py  # Main script
└── README.md

📦 Requirements
Install dependencies via pip:
bashpip install pandas scikit-learn

📊 Dataset
The script expects a file named spam.csv with at least two columns:
ColumnDescriptionv1Label — ham or spamv2The raw SMS message text
A commonly used dataset is the UCI SMS Spam Collection.

⚙️ How It Works

Load & Preprocess — Reads the CSV, renames columns, and maps labels to binary (ham → 0, spam → 1)
Split — 80/20 train-test split with random_state=42 for reproducibility
Vectorize — Converts raw text to numerical features using TF-IDF
Train — Fits a Multinomial Naive Bayes classifier on the training set
Evaluate — Prints accuracy on the held-out test set
Predict — Classifies a sample message: "Congratulations! You won a lottery"


▶️ Usage
bashpython spam_classifier.py
```

**Sample Output:**
```
Accuracy: 0.9713
Prediction: [1]   # 1 = spam, 0 = ham

🔍 Predict Custom Messages
Modify the msg list in the script to test your own messages:
pythonmsg = ["Hey, are we still meeting tomorrow?"]
msg_vec = vectorizer.transform(msg)
print("Prediction:", model.predict(msg_vec))

🧠 Model Details
ComponentChoiceVectorizerTF-IDF (TfidfVectorizer)ClassifierMultinomial Naive BayesTest Split20%Random State42

📌 Notes

The CSV must be encoded in latin-1 (as specified in the loader)
Only columns v1 and v2 are used; extra columns are ignored
TF-IDF is fit only on training data to prevent data leakage

---

## 👤 Author

Prithvi Pal
25BCE11284
