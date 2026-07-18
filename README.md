# 🚍 UrbanTech Feedback Classification with Naive Bayes

An end-to-end Natural Language Processing (NLP) project that automatically classifies customer feedback submitted through an urban transit mobile application into the appropriate support department using **Multinomial Naive Bayes**.

## 📌 Project Overview

UrbanTech receives hundreds of customer feedback messages every day through its public transportation navigation app. Manually sorting these messages is time-consuming and can delay issue resolution.

This project builds an automated text classification model capable of routing feedback into the correct department, improving operational efficiency and customer response times.

---

## 🎯 Business Problem

Automatically classify incoming customer feedback into one of three departments:

- 🗺️ **Navigation Issues**
  - Problems with routes, maps, or trip directions.

- 🚉 **Service Updates**
  - Incorrect transit schedules, delays, or service information.

- 📱 **App Experience**
  - Bugs, crashes, performance issues, and user interface feedback.

---

## 📂 Dataset

The dataset contains customer feedback collected from UrbanTech's mobile application.

**Features**

| Column | Description |
|----------|-------------|
| feedback_id | Unique feedback identifier |
| feedback_text | Customer feedback message |
| department | Target category |

Number of records: **197**

---

# 🛠️ Project Workflow

## 1. Data Exploration

- Dataset inspection
- Missing value analysis
- Category distribution
- Text length analysis

---

## 2. Text Preprocessing

The text preprocessing pipeline includes:

- Convert text to lowercase
- Remove punctuation
- Remove numbers
- Tokenization
- Stopword removal
- Lemmatization
- Text reconstruction

Libraries used:

- NLTK
- Regular Expressions (Regex)

---

## 3. Feature Engineering

Two text vectorization techniques were implemented:

### Bag of Words

Using:

- CountVectorizer

### TF-IDF

Using:

- TfidfVectorizer

---

## 4. Model Building

Model used:

- Multinomial Naive Bayes

Separate models were trained using:

- Bag of Words
- TF-IDF

---

## 5. Model Evaluation

Performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Classification Report
- Confusion Matrix

---

## 6. Hyperparameter Tuning

Model optimization was performed using:

- Pipeline
- GridSearchCV

Parameters tuned include:

- Alpha
- Maximum Features
- Minimum Document Frequency
- Maximum Document Frequency
- N-Grams
- Vectorizer Type

---

## 7. Prediction System

A reusable prediction function was created that:

- Accepts new customer feedback
- Applies preprocessing
- Performs vectorization
- Predicts the correct department
- Returns prediction confidence

Example:

```python
feedback = "The app keeps giving me the wrong bus route."

result = classify_feedback(feedback)

print(result)
```

---

# 📊 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Scikit-learn
- Jupyter Notebook

---



# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/urban-feedback-text-classification.git
```

Navigate into the project

```bash
cd urban-feedback-text-classification
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

---

# 📈 Skills Demonstrated

- Natural Language Processing (NLP)
- Text Cleaning
- Tokenization
- Lemmatization
- Feature Engineering
- Bag of Words
- TF-IDF
- Machine Learning
- Naive Bayes Classification
- Hyperparameter Tuning
- Model Evaluation
- Pipeline Construction
- GridSearchCV

---

# 📚 Future Improvements

- Deep Learning models (LSTM, GRU)
- Transformer-based models (BERT)
- Model deployment using FastAPI
- Interactive Streamlit dashboard
- Real-time feedback classification API

---

# 👨‍💻 Author

**Trevor**

Data Science | Machine Learning | NLP

If you found this project helpful, consider giving it a ⭐ on GitHub.
