# 🎓 JEE Closing Rank Prediction

A data-driven machine learning project to predict JEE (Joint Entrance Examination) closing ranks using historical admission data. The system leverages machine learning and deep learning techniques to support students in making informed decisions about college and branch preferences.

---

## 🧠 Problem Statement

Due to dynamic admission cutoffs and reservation policies, students often struggle with admission planning. This project provides a predictive framework to forecast closing ranks using historical trends, thereby assisting in strategic decision-making for college admissions.

---

## 📊 Dataset

**Source:** RankMatrix (IIT Roorkee initiative) via web scraping  
**Years Covered:** 2019–2024  
**Size:** ~15,000 records  
**Key Features:**
- Category (GEN, OBC, SC, etc.)
- Quota (AI/HS)
- Seat Pool (Gender-Neutral/Female-only)
- Opening Rank & Closing Rank
- Institute Name
- Branch Name
- Admission Year

---

## 🧹 Data Preprocessing

- Removed unnecessary columns (`id`, `latest_year`, etc.)
- Converted nested fields using `ast.literal_eval` (for institute & branch details)
- Handled missing values (none found)
- Applied **Label Encoding** for categorical variables
- Split data into training and testing sets (80:20)

---

## 📈 Models Implemented

### ✅ Machine Learning Models
| Model | R² Score | MAE |
|-------|----------|-----|
| Linear Regression | ~0.85 | Moderate |
| Random Forest | ↑ | Improved |
| **XGBoost** | ↑↑ | Very Good |
| **LightGBM** | **0.9878** | **240.88** |

### 🤖 Deep Learning Model
- **Model:** Multi-Layer Perceptron (MLP)
- Architecture: Dense Layers + ReLU + Dropout
- Optimizer: Adam | Loss: MSE  
- **R² Score:** 0.9755  
- **MAE:** 372.97  
- Result: Performed well, but slightly under LightGBM

---

## 📊 Visualizations

Key insights from EDA (refer notebook/ppt):
- 📈 **Year-wise Closing Rank Trend:** Shows general rise over time.
- 🏫 **Top Institutes:** IIT Delhi & IIT Bombay most competitive.
- 🧑‍🎓 **Category-wise Analysis:** Reserved categories have lower ranks.
- 🧪 **Top Branches:** Dual-degree and niche programs less competitive.
- 🪑 **Seat Pool Analysis:** Gender-neutral seats are more competitive.

---

## ✅ Conclusion

- LightGBM outperformed all other models in prediction accuracy.
- The predictive system offers students a smarter way to navigate admission choices.
- Easily scalable for new data, additional features, or other entrance exams.

---

## 🛠️ Tools & Tech

- Python, Pandas, scikit-learn, XGBoost, LightGBM
- TensorFlow/Keras (for MLP)
- Matplotlib / Seaborn (for plots)
- Jupyter Notebook

---
