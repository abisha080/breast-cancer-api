# 🩺 Breast Cancer Risk Prediction API

This project implements an end-to-end **Machine Learning + Optimization + API** solution to predict breast cancer risk and support cost-effective screening decisions.

---

## 🚀 Project Overview

Early detection of breast cancer significantly improves survival rates, but advanced diagnostic tests are expensive and limited.  
This project uses **machine learning probability estimates** combined with **optimization logic** to identify high-risk patients for screening.

---

## 🧠 Machine Learning Pipeline

- Dataset: Breast Cancer Wisconsin Dataset
- Target Variable: `diagnosis`
  - 1 → Malignant
  - 0 → Benign
- Models Used:
  - Logistic Regression (final model)
  - Random Forest (comparison)

### Key Steps:
- Exploratory Data Analysis (EDA)
- Outlier detection & IQR-based capping
- Feature scaling using StandardScaler
- Model evaluation using:
  - Confusion Matrix
  - ROC Curve
  - AUC Score

---

## 🧮 Optimization (PuLP)

Predicted cancer probabilities are used in a **Linear Programming model** to:

- Maximize total cancer risk detected
- Subject to:
  - Budget constraints
  - Screening capacity constraints

This enables **risk-based resource allocation** in healthcare screening.

---

## 🌐 FastAPI Deployment

A RESTful API was built using **FastAPI** to serve real-time predictions.

### API Endpoint

**POST /predict**

**Request Body:**
```json
{
  "features": [30 numeric feature values]
}
Response:

json
Copy code
{
  "cancer_risk_probability": 0.92,
  "screening_decision": "MANDATORY_SCREENING"
}
Screening Decisions:
MANDATORY_SCREENING → Very high risk

RECOMMENDED_SCREENING → High risk

NO_ADVANCED_SCREENING → Low risk

🛠️ Tech Stack
Python

Pandas, NumPy

Scikit-learn

PuLP

FastAPI

Uvicorn

▶️ Run Locally
bash
Copy code
pip install -r requirements.txt
python -m uvicorn main:app --reload
Open in browser:

arduino
Copy code
http://127.0.0.1:8000/docs
📌 Project Status
✅ Completed
✅ API Tested
✅ GitHub Ready
✅ Deployment Ready

👤 Author
Abisha

yaml
Copy code

---

## ✅ STEP 3: SAVE THE FILE

- Press **Ctrl + S**
- Close the file

---

## ✅ STEP 4: PUSH README TO GITHUB

In your project folder terminal, run:

```bash
git add README.md
git commit -m "Add project README"
git push
✅ STEP 5: VERIFY ON GITHUB
Open:
👉 https://github.com/abisha080/breast-cancer-api