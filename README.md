# sms-spam-detector

## 📌 Project Overview
This project builds a **machine learning–based SMS spam classifier** that automatically labels text messages as **Spam** or **Ham (legitimate)**.  
The model was trained on the **SMSSpamCollection dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection).  

The goal is to filter out unwanted promotional or fraudulent texts while maintaining a strong balance between **precision** (avoiding false alarms) and **recall** (catching as much spam as possible).

---

## 📂 Table of Contents
- Overview  
- Dataset  
- Preprocessing  
- Exploratory Data Analysis  
- Models  
- Results & Insights  
- Challenges & Solutions  
- Conclusion  
- How to Run  
- Requirements  

---

## 🗃 Dataset
- **Name:** SMSSpamCollection  
- **Size:** 5,574 English SMS messages  
- **Classes:**  
  - **Spam** → Promotional or fraudulent messages  
  - **Ham** → Genuine, user-to-user messages  
- **Source:** UCI Machine Learning Repository  

---

## 🧹 Preprocessing
- Converted text to lowercase  
- Removed punctuation, numbers, and special characters  
- Stripped extra whitespace  
- Tokenization + **TF-IDF vectorization** (max features: 5000)  
- Split: 80% training, 20% testing  

---

## 📊 Exploratory Analysis
- **Class Imbalance:** ~13% spam vs 87% ham  
- **Message Length:** Spam tends to be longer than ham  
- **Frequent Spam Words:** “free”, “win”, “text”, “claim”, etc.  
- **Visuals:** Count plots, histograms, word clouds  

---

## 🤖 Models Implemented
1. **Naïve Bayes (MultinomialNB)**  
   - Simple, efficient, well-suited for text data  
2. **Logistic Regression**  
   - Regularized model, tuned with GridSearchCV  
   - Adjusted with `class_weight='balanced'`  

---

## ✅ Results

### Naïve Bayes
- Accuracy: **96.86%**  
- Precision: **100%**  
- Recall: **76.51%**  
- F1 Score: **86.69%**  
➡ Zero false positives but lower recall  

### Logistic Regression
- Accuracy: **96.77%**  
- Precision: **99.13%**  
- Recall: **76.51%**  
- F1 Score: **86.36%**  
➡ Better balance, slight precision trade-off  

---

## ⚖️ Model Insights
| Model              | Pros                         | Cons                  |
|--------------------|------------------------------|-----------------------|
| Naïve Bayes        | Perfect precision (0 FP)     | Lower recall          |
| Logistic Regression| Balanced accuracy & recall   | Slightly lower precision |

- Use **Naïve Bayes** when avoiding false positives is critical  
- Use **Logistic Regression** for a more balanced approach  
- Future: Try **ensembles** or **deep learning (RNNs, Transformers)**  

---

## 🚧 Challenges & Solutions
- **Precision vs Recall Trade-off** → Tested multiple models and tuned hyperparameters  
- **Vectorization Choice** → Switched from CountVectorizer to TF-IDF for richer feature representation  
- **Convergence Issues in Logistic Regression** → Increased `max_iter` to 500  

---

## 🎯 Conclusion
- Both models detect spam effectively (>96% accuracy)  
- **Naïve Bayes**: Safer, no false positives, but misses more spam  
- **Logistic Regression**: More balanced and reliable in real-world use  

---

