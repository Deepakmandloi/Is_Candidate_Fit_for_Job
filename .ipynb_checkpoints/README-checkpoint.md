# 📘 Is Candidate Fit for Job

This project builds a machine learning pipeline to assess whether a candidate is suitable for a job, using various features like skills, experience, salary expectations, certifications, and location.

---

## 🚀 Project Overview

The notebook:
- Preprocesses and engineers features from raw job application data.
- Handles imbalanced classification using SMOTE and class weighting.
- Trains and evaluates models including **Random Forest** and **XGBoost**.
- Outputs performance metrics to help recruiters or automated systems make better hiring decisions.

---

## 🧠 Key Assumptions & Feature Engineering

1. **Job Description** is constant and was dropped.
2. Missing values in `certifications` were filled with empty strings.
3. Created:
   - `No. of matching skills`  
   - `Skills overlap ratio`  
   - `No. of certifications`  
   - `No. of past jobs`
4. **Experience gap** calculated:  
   `+ve` = over-qualified, `-ve` = under-qualified
5. **Salary metrics**:
   - `Expected salary under budget` (Boolean)
   - `Deviation from budget mean`
6. **Location match** encoded as a binary variable.
7. **One-hot encoding** applied to location and education level.
8. Data was **highly imbalanced**:
   - Used **stratified train-test split**
   - Applied **SMOTE** for Random Forest
   - Used **class weighting** for XGBoost

---

## 📊 Models Used

- **Random Forest Classifier**
- **XGBoost Classifier**

Each model was evaluated on precision, recall, and F1-score, with adjustments for class imbalance.

---

## 🧰 Requirements

To run the notebook:

```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn matplotlib
```

---

## 📁 Files

- `IsCandidateFit.ipynb` — Main notebook with full analysis
- `README.md` — You're reading it!

---