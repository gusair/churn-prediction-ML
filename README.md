# 📉 Churn Prediction Using Machine Learning

Welcome! This project uses machine learning to predict customer churn in a subscription-based telecom service. It walks through data cleaning, exploration, feature engineering, model training, and evaluation — all with a hands-on, beginner-friendly approach.

---

## 📌 What is Churn?

In the business world, **churn** refers to when customers stop using a service — whether they cancel a subscription, stop engaging, or leave silently. Understanding and predicting churn is critical, especially in industries where retaining customers is much more cost-effective than acquiring new ones.

---

## 🧠 Objective

The main goal of this project is to **predict which customers are at risk of churning**, using a real-world telecom dataset (provided by IBM Developer). With these insights, businesses can act early and reduce customer loss.

---

## 📂 Dataset

- Source: [IBM Sample Dataset](https://raw.githubusercontent.com/carlosfab/dsnp2/master/datasets/WA_Fn-UseC_-Telco-Customer-Churn.csv)
- Total records: `7,043`
- Total features: `21`
- Target variable: `Churn` (Yes / No)

The dataset includes customer demographics, account info, and service usage.

---

## 🔍 Project Steps

### 1. Data Cleaning & Exploration
- Checked for null values and fixed `TotalCharges` formatting issues.
- Converted data types as needed.
- Handled 11 missing values by imputing with the median.

### 2. Feature Engineering
- Created a new column to group customer `tenure` into short-term, mid-term, and long-term categories.
- Investigated churn rate by tenure groups:
  - Short-term: 47.43%
  - Mid-term: 25.53%
  - Long-term: 11.92%

### 3. Data Preprocessing
- Label encoded binary variables.
- Applied one-hot encoding to categorical variables.
- Converted all boolean columns to integer format.

### 4. Modeling
- Split data into train/test sets.
- Balanced the dataset using `RandomUnderSampler`.
- Standardized features using `StandardScaler`.
- Compared multiple classifiers using cross-validation focused on **recall**.

### 5. Final Model: Logistic Regression
- Selected Logistic Regression based on performance and interpretability.
- **Final Results on Test Set:**
  - Recall: `0.83`
  - Precision: `0.53`
  - F1 Score: `0.64`
  - Accuracy: `0.75`

---

## 📈 Key Insight

Customers who churn tend to do so early. Once a subscriber stays beyond one year, their likelihood to churn drops significantly. This highlights the importance of **early engagement strategies**.

---

## 🚀 How to Use

1. Clone the repository  
2. Install dependencies  
3. Run the Jupyter Notebook or Google Colab

---

## 💡 Tools & Libraries

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Imbalanced-learn
- XGBoost & LightGBM

---

## ✍️ Author

Project by Augusto de Jesus — built as part of a hands-on journey into Machine Learning.  
Feel free to connect or ask questions!

---

## 📎 License

This project is for educational purposes only.
