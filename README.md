# 📧 Spam Classifier (Python + Scikit-learn)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A machine learning model to classify text messages as **SPAM** or **HAM** (non-spam), built with:  
- **TF-IDF Vectorization**  
- **Logistic Regression**  
- Interactive testing in **Google Colab/Jupyter**  

---

## ▶️ Quick Start
1. **Open in Google Colab**:  
   [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1BMyh7b1KQAcz94fKxc5vHf3XXdlFJgWA)

2. **Run the interactive classifier**:
   ```python
   # Load model and predict
   def predict_spam(message):
       model = joblib.load('spam_classifier.pkl')
       proba = model.predict_proba([message])[0]
       print(f"🔮 Prediction: {'🚨 SPAM' if model.predict([message])[0] == 1 else '📩 HAM'}")
       print(f"   Confidence: {max(proba):.2%}")

   # Test it!
   predict_spam("Win a free iPhone!")  # Example

   📦 Files
File	Description
spam_classifier.pkl	Trained model (Joblib)
spam_classifier.ipynb	Colab notebook (training + demo)

🛠️ Customization
Train with Your Data
Replace the dummy dataset with real data (e.g., SMS Spam Collection):

import pandas as pd
df = pd.read_csv("spam.csv")  # Your dataset
X, y = df["text"], df["label"]

from sklearn.ensemble import RandomForestClassifier
pipeline = Pipeline([
    ("tfidf", TfidfVectorizer()),
    ("clf", RandomForestClassifier())  # Swapped model
])


📜 License
MIT License - Free for personal/commercial use.
