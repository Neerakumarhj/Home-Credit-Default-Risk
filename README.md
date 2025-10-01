# Home-Credit-Default-Risk
Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders.

# 🏦 Home Credit Default Risk – Kaggle Project  

## 📌 Overview  
This project tackles the **Home Credit Default Risk** challenge from Kaggle.  
The goal is to predict whether a client will **repay (0)** or **default (1)** on a loan using demographic, financial, and historical credit data.  

By improving risk prediction, financial institutions like **Home Credit Group** can broaden financial inclusion—approving more safe borrowers while reducing losses from defaults.  

---

## 🔹 Steps in the Project  
1. **Data Loading** – Imported training & test datasets (`application_train.csv`, `application_test.csv`).  
2. **Preprocessing** –  
   - Removed ID columns  
   - One-hot encoded categorical variables  
   - Handled missing values with imputation  
   - Aligned train and test features  
3. **Baseline Model** – Logistic Regression achieved **AUC ~0.62**.  
4. **Optimized Model** – LightGBM achieved **AUC ~0.75** (stronger predictive power).  
5. **Feature Importance** – Identified top predictors of default risk (e.g., external credit scores, age, employment history).  
6. **Predictions** – Generated probability of default for each client and created a **Kaggle submission file**.  

---

## 📊 Results  
- **Logistic Regression AUC**: ~0.62 (baseline)  
- **LightGBM AUC**: ~0.75 (optimized)  
- **Insights**:  
  - Higher credit risk linked to weaker external credit scores and shorter employment histories  
  - Default rate in training data: ~8% (imbalanced dataset)  

---

## 🚀 Business Impact  
- Enables better loan approval strategies:  
  - **Low risk (<5%)** → Approve normally ✅  
  - **Medium risk (5–15%)** → Approve with caution ⚠️  
  - **High risk (>15%)** → Reject or stricter terms ❌  
- Helps Home Credit support **financial inclusion** while managing default risk.  

---

## 📂 Files in Repository  
- `HomeCredit_Notebook.ipynb` → Jupyter Notebook with full analysis & modeling  
- `submission.csv` → Kaggle-ready predictions file  
- `README.md` → Project documentation  

---

## 🛠️ Tech Stack  
- **Python**  
- **Pandas, NumPy, Matplotlib, Seaborn**  
- **Scikit-learn** (Logistic Regression, preprocessing)  
- **LightGBM** (optimized model)  

---

## 📌 Next Steps  
- Feature engineering with additional datasets (`bureau.csv`, `previous_application.csv`, `installments_payments.csv`)  
- Hyperparameter tuning with **Optuna/RandomSearch**  
- Handling class imbalance with **SMOTE / class weights**  
