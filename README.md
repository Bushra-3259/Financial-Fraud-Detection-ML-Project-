# 🛡️ Secure-Gate: Multi-Modal Risk Assessment & Fraud Detection Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Bushra-3259/Financial-Fraud-Detection-ML-Project-/blob/main/Financial_Fraud_Detection_(ML_Project).ipynb)

An end-to-end Machine Learning and AI pipeline engineered to identify financial fraud in highly imbalanced datasets. This architecture couples traditional tabular fraud forecasting with natural language understanding to catch sophisticated, social-engineered threat vectors.

## 🚀 Key Architectural Highlights
- **Multi-Modal Decision Coupling:** Interlocks a tabular Random Forest model with a zero-shot NLP Transformer (`BART-large-mnli`). If text analysis flags an underlying threat, a system override triggers security steps even if numerical data appears safe.
- **Explainable AI (XAI):** Uses structurally constrained decision paths to map precise risk boundaries across transaction histories, peeling back the "black box" of risk scores.
- **Dynamic Security Tiering:** Employs an automated step-up Multi-Factor Authentication (MFA) buffer zone for uncertain risk scores (35% to 70%) to dramatically minimize user friction while keeping the system secure.

---

## 📊 Performance Diagnostics & Analytics

### 1. Risk Score Distribution & Security Tiering
Instead of making rigid, absolute binary assumptions, the system isolates high-density fraud zones and creates a frictionless "MFA Required" middle tier.
![Risk Score Distribution](img5.png)

### 2. Finding the Optimal Security Threshold
Evaluates model precision and recall trade-offs across different probability thresholds to identify where the operational security cutoffs should live.
![Operational Threshold Optimization](img9.png)

### 3. Precision-Recall & ROC Performance
The pipeline achieves high structural stability in heavily skewed data distributions, establishing a robust reliability score.
![Reliability Curve](img7.png) 

![ROC-AUC Curve](img8.png)

### 4. Machine Learning Feature Importances
A clean evaluation tracking which transactional markers (such as combined risk vectors, transaction amounts, and IP risk metrics) drive the underlying security logic.
![Feature Importances](img4.png)

### 5. Model Generalization (Learning Curves)
Tracks model training vs. validation F1-scores across shifting sample sizes to verify steady optimization without overfitting.
![Learning Curves](img3.png)

---

## 🎨 Interactive Control Panel & Multi-Modal Simulation
Because this project utilizes live UI elements (`ipywidgets`), use the **Open in Colab** badge at the top of this page to interact with the live control panel!

Below is a live validation snapshot where a transaction memo displaying manipulative intent triggers a **Multi-Modal Step-Up Override** even though the numerical engine initially outputted a low hazard score:

![Interactive UI Dashboard](img11.png)

---

## 🛠️ Tech Stack & Dependencies
- **Language:** Python
- **Tabular Core:** Scikit-Learn (Random Forest Ensemble & Pipelines), Pandas, NumPy
- **Linguistic Engine:** Hugging Face Transformers (`BART-large-mnli`)
- **UI Framework:** IPyWidgets & IPython Display
- **Visualization:** Seaborn & Matplotlib
