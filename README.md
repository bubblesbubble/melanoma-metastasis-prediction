# Melanoma Metastasis Prediction using Hybrid Machine Learning

A machine learning project for classifying melanoma tumor samples as **Primary** or **Metastatic** using TCGA RNA-seq gene expression data.  
The project benchmarks multiple models and develops a **Hybrid ANN + LightGBM ensemble** for improved predictive performance, with explainability using SHAP.

---

## Project Overview

Melanoma is an aggressive skin cancer where early detection of metastasis is clinically important.  
This project uses gene expression profiles to predict tumor type and identify influential genes associated with progression.

### Objectives
- Classify melanoma samples into Primary (0) and Metastatic (1)
- Compare multiple ML/DL models
- Build a hybrid ensemble model
- Interpret predictions using explainable AI
- Extract top genes for biological analysis

---

## Dataset

- Source: **TCGA (The Cancer Genome Atlas)**
- Data Type: RNA-seq Gene Expression
- Task: Binary Classification

### Labels
- `0` = Primary Tumor
- `1` = Metastatic Tumor

---

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- LightGBM
- XGBoost
- Matplotlib
- SHAP

---

## Workflow

1. Data preprocessing  
2. Feature selection / dimensionality reduction  
3. Train-test split with stratification  
4. Model training:
   - Artificial Neural Network (ANN)
   - Random Forest
   - XGBoost
   - LightGBM
5. Hybrid ANN + LightGBM Ensemble
6. Evaluation using Accuracy, ROC-AUC, Confusion Matrix
7. SHAP explainability
8. Top gene extraction

---

## Results

| Model | Accuracy | ROC-AUC |
|------|----------|---------|
| Random Forest | 90.5% | 0.953 |
| XGBoost | 95.8% | 0.952 |
| LightGBM | 95.8% | 0.970 |
| Hybrid ANN + LightGBM | **96.8%** | 0.955 |

### Final Model
**Hybrid ANN + LightGBM** selected for highest classification accuracy and strong metastatic detection.

---

## Explainability

Used **SHAP (SHapley Additive Explanations)** on LightGBM to interpret predictions and identify biologically relevant genes.

### Example Insights
- Certain genes strongly push predictions toward metastatic melanoma
- Model learns combined gene-expression patterns rather than relying on one feature

---

## Top Gene Analysis

Exported the **Top 200 important genes** using LightGBM feature importance for downstream pathway / biomarker analysis.
