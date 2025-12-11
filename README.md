# 🌾 Crop Recommendation System (Machine Learning + Explainable AI)

This project recommends the most suitable crop based on soil nutrients and environmental conditions using a **Random Forest Classifier**, and provides **model explainability using SHAP (SHapley Additive exPlanations)**.

---

## 📌 Objective

To build a machine learning model that predicts the best crop for a given set of soil and climate parameters, and to **interpret model decisions** using feature importance and SHAP explainability.

---

## 📊 Dataset

* **Features:**

  * N (Nitrogen)
  * P (Phosphorus)
  * K (Potassium)
  * Temperature
  * Humidity
  * pH
  * Rainfall
* **Target:** Crop label (multi-class)
* **Rows:** ~2200
* **Source:** Kaggle – Crop Recommendation Dataset

---

## 🤖 Model Description

* **Algorithm:** Random Forest Classifier
* **Train/Test Split:** 80% / 20%
* **Accuracy:** ~99.3%
* **Saved model:** `crop_model.pkl`

The Random Forest model was chosen because it performs well on tabular data, handles nonlinear patterns, and provides built-in feature importance.

---

## 🧠 Explainable AI (XAI) — SHAP

To understand **why** the model predicts a particular crop:

* Used **TreeExplainer** from the SHAP library
* Aggregated multiclass SHAP values for global sensitivity
* Visualized:

  * **SHAP summary plot** (`shap_summary.png`)
  * **Feature importance plot** (`feature_importance.png`)

These visualizations show how each feature influences the model's predictions.

---

## 📈 Key Insights

* **Rainfall** and **Humidity** strongly influence crop suitability.
* **pH** is an important environmental factor.
* N, P, and K nutrients affect crops differently depending on their biology.

---

## 📁 Project Structure

```
crop_project/
│
├── Crop_recommendation.csv      # Dataset
├── notebook.ipynb               # Full ML + SHAP code
├── crop_model.pkl               # Saved Random Forest model
├── shap_summary.png             # SHAP global explanation
├── feature_importance.png       # Random Forest feature importance
└── README.md                    # Project documentation
```

---

## 🔧 How to Run the Project

### 1. Install dependencies

```bash
pip install numpy pandas scikit-learn shap matplotlib joblib
```

### 2. Open the Jupyter Notebook

```bash
jupyter notebook
```

### 3. Run all cells in `notebook.ipynb` to:

* Train the model
* Evaluate accuracy
* Generate SHAP plots
* Save the model

---

## 🚀 Future Improvements

* Build a **Streamlit web app** for user input
* Add **real-time weather API**
* Perform **GridSearchCV** hyperparameter tuning
* Deploy on **HuggingFace Spaces** or **Render**

---

## ✔ Status

**Completed** — Machine Learning + Explainability + Visualizations + Documentation.

---


