# Customer Churn Prediction using AI/Machine Learning

Internship project for the **IBM SkillsBuild Data Analytics with AI Academic
Internship Program**, conducted by **BharatCares** in association with **AICTE**.

**Author:** Isha Sharma

## Project Description

Customer churn (customers discontinuing a service) directly impacts the revenue of
subscription-based businesses. This project analyzes a telecom company's customer
data to understand **why customers churn** and builds several **Machine Learning
classification models** to **predict which customers are likely to churn**, so the
business can act proactively through targeted retention efforts.

The project covers a complete data analytics + AI workflow:

1. Data cleaning and preprocessing
2. Exploratory Data Analysis (EDA) with visualizations
3. Feature engineering (encoding, scaling, class-imbalance handling with SMOTE)
4. Training and comparing four AI models: Logistic Regression, Decision Tree,
   Random Forest, and Gradient Boosting
5. Model evaluation (accuracy, precision, recall, F1-score, ROC-AUC, confusion
   matrix, ROC curves)
6. Feature-importance analysis
7. Business insights and actionable recommendations

## Dataset

- **Name:** Telco Customer Churn
- **Source:** [Kaggle — Telco Customer Churn (blastchar/telco-customer-churn)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
  — originally an IBM sample dataset for customer retention analytics. The identical
  data is included in this repository at [`data/Telco-Customer-Churn.csv`](data/Telco-Customer-Churn.csv)
  so the notebook runs without any manual download.
- **Size:** 7,043 customer records × 21 columns
- **Target:** `Churn` (Yes / No)

## Technologies Used

- Python 3
- pandas, NumPy — data manipulation
- Matplotlib, Seaborn — data visualization
- scikit-learn — machine learning models and evaluation
- imbalanced-learn (SMOTE) — class-imbalance handling
- Jupyter Notebook

## Project Structure

```
IBM-SkillsBuild-Customer-Churn-Prediction/
├── data/
│   └── Telco-Customer-Churn.csv
├── notebook/
│   └── IshaSharma_CustomerChurnPrediction.ipynb
├── requirements.txt
└── README.md
```

## Setup / Run Instructions

1. Clone or download this project folder.
2. Create and activate a virtual environment (recommended):
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate      # Windows: .venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook notebook/IshaSharma_CustomerChurnPrediction.ipynb
   ```
5. Run all cells (Kernel → Restart & Run All). The notebook reads the dataset from
   `../data/Telco-Customer-Churn.csv`, so keep the folder structure intact.

## Key Results

- Best model: **Gradient Boosting** (ROC-AUC ≈ 0.84, accuracy ≈ 78%)
- Strongest churn drivers: contract type (month-to-month), low tenure, high
  monthly charges, fiber-optic internet service, and electronic-check payment.
- Full details, charts, and the classification report are in the notebook and in
  the project report (`IshaSharma_ProjectReport.docx`).

## Key Business Recommendations

- Incentivize month-to-month customers to move to longer-term contracts.
- Build a dedicated retention journey for customers in their first 12 months.
- Review Fiber-optic pricing and bundle security/support add-ons into plans.
- Encourage automatic payment methods to reduce payment-related churn.
- Score the active customer base monthly with the trained model to proactively
  flag and reach out to high-risk customers.
