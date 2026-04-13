# 🏦 Loan Approval Prediction

> End-to-End Data Science project predicting loan approval using Python (EDA, Cleaning, ML) and Power BI interactive dashboard — SVM model achieving 80% accuracy.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) ![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-orange?logo=powerbi) ![ML](https://img.shields.io/badge/ML-SVM%2080%25%20Accuracy-green) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Project Overview

This project builds a complete end-to-end data science pipeline to predict loan approval outcomes for banking applications. Starting from raw CSV data, the project covers exploratory analysis, data cleaning, feature engineering, machine learning modeling, and an interactive Power BI dashboard — making the insights accessible to both technical and non-technical stakeholders.

| Metric | Value |
|--------|-------|
| 📋 Total Applications | 614 |
| 🔢 Features | 13 |
| ✅ Approval Rate | 68.7% |
| 🤖 Model Accuracy | 80% |
| 📊 ML Models Tested | 6 |

<img src="https://github.com/Mohamed-Nofal-DataAnalysis/loan-approval-prediction/blob/main/Project%20Overview.png">

---

## 📊 Dataset

- **614** loan applications from a financial institution
- **13** features including applicant demographics, income, loan amount, and credit history
- **Target variable:** `Loan_Status` → Y (Approved) = 68.7% | N (Rejected) = 31.3%

### Features
| Feature | Description |
|---------|-------------|
| `Gender` | Applicant gender |
| `Married` | Marital status |
| `Dependents` | Number of dependents |
| `Education` | Graduate / Not Graduate |
| `Self_Employed` | Self-employment status |
| `ApplicantIncome` | Applicant monthly income |
| `CoapplicantIncome` | Co-applicant monthly income |
| `LoanAmount` | Loan amount requested (K) |
| `Loan_Amount_Term` | Term of loan in months |
| `Credit_History` | Credit history (1 = Good, 0 = Bad) |
| `Property_Area` | Urban / Semiurban / Rural |
| `Loan_Status` | Target — Y (Approved) / N (Rejected) |

---

## 📂 Project Structure

```
loan-approval-prediction/
├── data/
│   ├── Loan data.csv                       # Raw dataset
│   └── loan_cleaned.csv                    # Cleaned dataset
├── notebook/
│   └── Loan_Status_Prediction.ipynb        # Full Python analysis
├── dashboard/
│   └── Loan_Approval_Dashboard.pbix        # Power BI dashboard
├── presentation/
│   └── Loan_Approval_Presentation.pptx
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| Pandas & NumPy | Data manipulation |
| Seaborn & Matplotlib | Data visualization |
| Scikit-learn | Machine learning |
| Jupyter Notebook | Development environment |
| Microsoft Power BI | Interactive dashboard |

---

## 🔄 Project Pipeline

### 1. Exploratory Data Analysis (EDA)
- Loaded dataset — 614 rows × 13 columns
- Analyzed distributions of income, loan amount, and term
- Visualized approval patterns across education, marital status, gender, and property area
- Identified missing values across 6 columns

### 2. Data Cleaning & Preprocessing
- **Categorical columns** → filled with Mode (Gender, Married, Dependents, Self_Employed, Credit_History, Loan_Amount_Term)
- **LoanAmount** → filled with Median to avoid skew sensitivity
- Confirmed **0 duplicate records**
- Replaced `'3+'` dependents with `4` for numerical encoding
- Saved cleaned dataset as `loan_cleaned.csv`

### 3. Feature Engineering
- Label Encoding applied to all categorical variables:
  - `Gender`: Male=1, Female=0
  - `Married`: Yes=1, No=0
  - `Self_Employed`: Yes=1, No=0
  - `Property_Area`: Rural=0, Semiurban=1, Urban=2
  - `Education`: Graduate=1, Not Graduate=0
  - `Loan_Status`: Y=1, N=0

### 4. Model Training & Evaluation

- **Train/Test Split:** 90% / 10% with stratification (552 train | 62 test)
- **Primary Model:** Support Vector Machine — Linear Kernel

| Model | Test Accuracy |
|-------|:-------------:|
| **Logistic Regression** | **80.6%** |
| **SVM — Linear ✅** | **80.6%** |
| Naive Bayes | 80.6% |
| Random Forest | 77.4% |
| Gradient Boosting | 75.8% |
| KNN | 72.6% |

### 5. Power BI Dashboard
- **KPI Cards:** Total Requests, Approval Rate, Avg Loan Amount, Median Income, Good Credit Ratio
- **Charts:** Approval by Education & Marital Status, Dependents Impact, Property Area Analysis, Gender Distribution, Loan Status Breakdown
- **6 Interactive Slicers** for full data exploration

<img src="https://github.com/Mohamed-Nofal-DataAnalysis/loan-approval-prediction/blob/main/Exploratory%20Data%20Analysis%20%26%20Cleaning.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/loan-approval-prediction/blob/main/Machine%20Learning%20Model.png">

---

## 💡 Key Insights

- 💳 **Credit History is the #1 driver** — 85.5% of good-credit applicants were approved
- 🎓 **Education matters** — Graduates had 70.8% approval vs significantly lower for non-graduates
- 🏘️ **Semiurban leads** — highest demand (233 applications) AND best approval rates
- 👨‍👩‍👧 **Dependents impact** — approval peaks at 1–2 dependents, drops at 3+
- ⚖️ **No gender bias detected** — Female 50.79% vs Male 49.21%, nearly equal distribution
- 💍 **Married applicants** show 71.8% approval rate

<img src="https://github.com/Mohamed-Nofal-DataAnalysis/loan-approval-prediction/blob/main/Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/loan-approval-prediction/blob/main/Key%20Insights%20from%20the%20Dashboard.png">

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/loan-approval-prediction.git
cd loan-approval-prediction
```

### 2. Install Dependencies
```bash
pip install pandas numpy seaborn scikit-learn matplotlib jupyter
```

### 3. Run the Notebook
```bash
jupyter notebook notebook/Loan_Status_Prediction.ipynb
```

### 4. Open Power BI Dashboard
Open `dashboard/Loan_Approval_Dashboard.pbix` in Microsoft Power BI Desktop

---

## 📬 Connect

If you found this project useful, feel free to ⭐ star the repository and connect!
---

## 👨‍💼 Author
Mohamed Nofal
Data & Business Analyst  
> Transforming raw data into actionable business insights.

