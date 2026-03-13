# loan-approval-prediction
ML model to predict bank loan approvals using Logistic Regression with automated business risk analysis
# 🏦 Bank Loan Approval Prediction System

## 📌 Project Overview
An end-to-end Machine Learning project that predicts 
whether a bank loan application will be 
Approved ✅ or Denied ❌ based on applicant's 
financial & personal information.

Built during Data Science Internship at 
iStudio

---

## 🎯 Problem Statement
Banks receive thousands of loan applications daily.
Manual review is:
- ⏰ Time consuming
- ❌ Prone to human bias
- 💰 Expensive

This ML model automates the decision process and
provides business risk analysis to reduce:
- Financial losses from bad loans
- Revenue loss from rejected good customers

---

## 📊 Dataset
- File: loan_data_set.csv
- Source: Internship Project Dataset
- Target Column: Loan_Status (Y = Approved, 
                              N = Denied)

Features Used:
┌─────────────────────┬────────────────────┐
│ Feature             │ Type               │
├─────────────────────┼────────────────────┤
│ Gender              │ Categorical        │
│ Married             │ Categorical        │
│ Education           │ Categorical        │
│ Self_Employed       │ Categorical        │
│ ApplicantIncome     │ Numerical          │
│ CoapplicantIncome   │ Numerical          │
│ LoanAmount          │ Numerical          │
│ Loan_Amount_Term    │ Numerical          │
│ Credit_History      │ Numerical          │
│ Property_Area       │ Categorical        │
│ Loan_Status         │ Target Variable    │
└─────────────────────┴────────────────────┘

---

## 🔄 Project Workflow

Data Loading → EDA → Data Cleaning → 
Preprocessing → Model Training → 
Evaluation → Business Report

---

## 🛠️ Tech Stack
- Language  : Python 3
- ML Library: Scikit-learn
- Analysis  : Pandas, NumPy
- Visualize : Matplotlib, Seaborn
- Platform  : Google Colab

---

## ⚙️ ML Pipeline

### 1️⃣ Data Cleaning
- Filled missing numerical values 
  with Median
- Filled missing categorical values 
  with Mode (most frequent)
- Dropped irrelevant column (Loan_ID)

### 2️⃣ Preprocessing
- One-Hot Encoding for categorical 
  features (Gender, Education, 
  Property Area etc.)
- StandardScaler for numerical 
  features to handle income-scale 
  disparities

### 3️⃣ Model Training
- Algorithm : Logistic Regression
- Train/Test Split: 80% / 20%
- Random State: 42

### 4️⃣ Model Evaluation
- Overall Accuracy: 78.86%
- Metrics Used:
  ✓ Precision
  ✓ Recall  
  ✓ F1-Score
  ✓ Confusion Matrix

---

## 📈 Results

### Model Performance
|
 Metric    
|
 Denied (0) 
|
 Approved (1) 
|
|
-----------
|
------------
|
--------------
|
|
 Precision 
|
 0.95       
|
 0.76        
|
|
 Recall    
|
 0.42       
|
 0.99         
|
|
 F1-Score  
|
 0.58       
|
 0.86         


### Confusion Matrix


---

## 💡 Business Insights Generated

### ✅ What Model Does Well
- Correctly identifies safe loans to approve
- Correctly flags risky loans to deny

### ⚠️ Risk Analysis
- False Positives = Bad loans approved
  → Direct financial risk to bank
  
- False Negatives = Good loans rejected
  → Lost revenue opportunity

### 📌 Business Recommendation
[Model automatically generates this based 
on FP vs FN comparison]
- If FP > FN → Model is too optimistic
  → Need stricter thresholds
- If FN > FP → Model is too strict  
  → Need relaxed thresholds

---

## 🗂️ Project Structure

📂 loan-approval-prediction/
├── 📓 loan_prediction.ipynb  ← Main notebook
├── 📊 loan_data_set.csv      ← Dataset
├── 📄 README.md              ← You are here
└── 📈 results/
    └── confusion_matrix.png  ← Output image

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Click "Open in Colab" button above
2. Upload loan_data_set.csv to Colab
3. Run all cells (Runtime → Run All)

### Option 2: Local Machine
```bash
# Clone repository
git clone https://github.com/yourusername/loan-approval-prediction.git

# Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn

# Open notebook
jupyter notebook loan_prediction.ipynb
