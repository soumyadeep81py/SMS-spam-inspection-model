📌 Overview
This project implements a spam detection system using a Logistic Regression classifier with TF-IDF text vectorization. It can predict whether a given message is spam (e.g., promotional, scam) or ham (legitimate).

✅ Interactive testing – Input messages and get real-time predictions
✅ Confidence scores – See how confident the model is
✅ Google Colab-ready – Works natively in Colab

🚀 Quick Start
1. Open in Google Colab
▶️ Run the Notebook

2. Run the Interactive Classifier
python
# Load the model and start predicting
predict_spam_interactive()
Example Input/Output:

text
🔮 Spam Classifier - Type 'quit' to exit  

Enter a message: "You won a free iPhone!"  
🚨 SPAM (Confidence: 98.5%)  

Enter a message: "Let's meet tomorrow"  
📩 HAM (Confidence: 99.1%)  
🛠️ How It Works
Model Pipeline
Text Vectorization: TfidfVectorizer() converts messages into numerical features.

Classification: LogisticRegression() predicts spam (1) or ham (0).

Training Data (Dummy Example)
python
X_train = ["Win cash now", "Meeting at 3 PM", "Free gift!", "Hello"]  
y_train = [1, 0, 1, 0]  # 1=Spam, 0=Ham  
📂 Files
File	Description
spam_classifier.pkl	Saved trained model (Joblib format)
spam_classifier.ipynb	Colab notebook with training & prediction code
🔧 Customization
Improve the Model
Replace dummy data with a real dataset (e.g., SMS Spam Collection).

Try better models (e.g., RandomForestClassifier, SVM).

Add preprocessing (lowercase, stopwords removal, etc.).

Deploy
Web App: Use Flask/FastAPI to host the classifier.

API: Wrap predictions in a REST endpoint.

📜 License
MIT License – Free for personal and commercial use.

🎯 Made for learning purposes – Adapt and expand as needed!
🔗 Questions? Open an issue or contribute!
