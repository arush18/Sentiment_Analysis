# 🧠 Sentiment Analysis on Twitter Tweets

[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat-square&logo=jupyter)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-blue?style=flat-square&logo=kaggle)](https://www.kaggle.com/datasets/kazanova/sentiment140)

This repository contains a machine learning project that performs **Sentiment Analysis** on a dataset of 1.6 million tweets. The dataset is publicly available on Kaggle (Sentiment140). The goal is to classify tweets as either **positive** or **negative** based on their textual content.

---

## 📁 Project Structure

Here's a breakdown of the current repository structure:

```
Sentiment_Analysis/
│
├── dataset/ # not pushed on github
│ └── training.1600000.processed.noemoticon.csv
│
├── notebooks
│ └── main.ipynb
│
├── output/models/ # (Optional)
│ └── sentiment_model.pkl
│
├── .gitignore
│
├── LICENSE.md
│
├── README.md
│
└── requirements.txt
```

---

## ⚙️ How It Works

### 1. **Data Preprocessing**
- Removes URLs, special characters, and mentions
- Applies **stemming** using `PorterStemmer`
- Removes **stopwords** from NLTK

### 2. **Feature Engineering**
- Converts text data to numerical features using `TfidfVectorizer`

### 3. **Model Training**
- Splits dataset into training and test sets
- Trains a **Logistic Regression** classifier

### 4. **Evaluation**
- Reports model accuracy
- You can replace the classifier with SVM, Random Forest, etc. for experimentation

### 5. **Model Persistence**
- Trained model can be saved using `pickle` for later use

---

## 📊 Results

- **Baseline model** (Logistic Regression with TF-IDF): ~Accuracy in the ballpark of 75-80% depending on preprocessing and vectorizer tuning.

---

## 🚀 How to Run

### Clone the Repo

```bash
git clone https://github.com/arush18/Sentiment_Analysis.git
cd Sentiment_Analysis