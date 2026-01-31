# 🎓 Student Dropout Early Warning System

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.29-orange)](https://streamlit.io/)
[![License](https://img.shields.io/badge/License-MIT-green)](https://opensource.org/licenses/MIT)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/student-dropout-warning)](https://github.com/yourusername/student-dropout-warning/issues)

---

## 🚀 Project Overview
Universities often face student dropouts every semester, impacting performance and reputation.  
This project builds a **Student Dropout Early Warning System** using machine learning to **flag high-risk students early** so advisors can intervene in time.

**Key Features:**
- Predicts which students are at risk of dropping out.
- Provides a **risk score** and **risk label** (Low / Medium / High) for each student.
- Displays **top 20 high-risk students** for quick action.
- Explains **key reasons behind dropout predictions** using feature importance.
- Interactive **Streamlit dashboard** for easy use by non-technical staff.

---

## 📊 Dataset
Dataset used: [xAPI-Edu-Data](https://www.kaggle.com/datasets/aljarah/xAPI-Edu-Data)  
- 480 student records  
- 17 features including demographics, academic activity, and parent info  
- Target variable mapped to **Dropout (1) / Continue (0)**

---

## 🔧 Tech Stack
- Python 3.11  
- Pandas, NumPy for data manipulation  
- Matplotlib, Seaborn for visualization  
- Scikit-learn for ML (RandomForestClassifier, LogisticRegression, DecisionTree)  
- Streamlit for interactive dashboard  
- Joblib for saving/loading trained models  

---

## 🧩 Project Workflow

1. **Data Cleaning & Preprocessing**
   - Remove duplicates
   - Encode categorical variables
   - Handle class imbalance using **SMOTE**

2. **Feature Exploration**
   - Count plots for categorical variables
   - Correlation heatmaps for numerical variables
   - Pairplots and visualizations for insights

3. **Model Training**
   - Logistic Regression, Decision Tree, Random Forest
   - Random Forest chosen for best **accuracy (≈88%)** and interpretability
   - Model saved as `student_dropout_model.pkl` for deployment

4. **Prediction & Evaluation**
   - Risk score = predicted probability of dropout
   - Risk label = High / Medium / Low
   - Confusion matrix, precision, recall, F1-score plots for evaluation

5. **Streamlit Dashboard**
   - Upload CSV student file
   - View top high-risk students
   - Check individual student risk
   - Feature importance visualization
   - Optional: Evaluate performance if true labels provided

---

- `requirements.txt` → Python dependencies  
- `README.md` → This file  

---

git clone https://github.com/yourusername/student-dropout-warning.git
cd student-dropout-warning
