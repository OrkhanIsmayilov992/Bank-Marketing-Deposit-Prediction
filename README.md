# Bank Marketing Deposit Prediction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/OrkhanIsmayilov992/Bank-Marketing-Deposit-Prediction/blob/main/Bank_Marketing_Deposit_Prediction_Model%20(2).ipynb)


A machine learning model that predicts whether a bank customer will subscribe to a term deposit based on marketing campaign data.

## 🎯 Problem

Banks run phone-based marketing campaigns to sell term deposits, but calling every customer is expensive and inefficient — most calls don't convert. This project predicts **which customers are most likely to subscribe**, so the bank can focus its outreach on high-potential leads instead of cold-calling everyone.

## 📊 Dataset

- **Source:** UCI Bank Marketing Dataset
- **Samples:** 11,162
- **Target:** `deposit` (0 = No, 1 = Yes)
- **Features:** age, job type, marital status, education, balance, previous campaign outcomes, and more

## 🔍 Methodology

1. **Data cleaning & EDA** — missing values, outlier detection, correlation analysis
2. **Feature engineering** — encoding categorical variables, binning age/balance
3. **Model training** — comparison of Logistic Regression, Random Forest, XGBoost, and CatBoost
4. **Model interpretation** — SHAP values to explain feature contributions

## 🤖 Result: CatBoost performed best

| Metric | Score |
|---|---|
| Accuracy | 0.8119 |
| F1 Score | 0.8068 |
| ROC AUC | 0.8894 |

## 📈 Top predictive features

1. **Balance** — strongest numerical predictor
2. **Marital Status** — married vs. single customers behave differently
3. **Campaign** — number of contacts affects outcome
4. **Age Group** — behavioral patterns vary by age
5. **Previous Outcome** — the result of prior campaigns is a strong signal

## 🛠️ Tech stack

- Python 3.11
- Pandas, NumPy
- Scikit-learn
- XGBoost, CatBoost
- SHAP (model interpretability)
- Matplotlib, Seaborn (visualization)

## 📁 Project structure

```
Bank-Marketing-Deposit-Prediction/
├── Bank_Marketing_Deposit_Prediction_Model.ipynb   # main analysis and model
├── README.md
├── LICENSE
└── requirements.txt
```

## 🚀 Getting started

```bash
git clone https://github.com/OrkhanIsmayilov992/Bank-Marketing-Deposit-Prediction.git
cd Bank-Marketing-Deposit-Prediction
pip install -r requirements.txt
jupyter notebook Bank_Marketing_Deposit_Prediction_Model.ipynb
```

## 💡 Results & limitations

The model achieves ~89% ROC AUC and separates likely subscribers from unlikely ones well. However, the dataset is tied to a specific country and time period, so it would need retraining before use in a different market. A planned next step is wrapping the model in a lightweight FastAPI service for real-time scoring.

## 👤 Author

**Orkhan Ismayilov**
[GitHub](https://github.com/OrkhanIsmayilov992)

## 📄 License

MIT License
