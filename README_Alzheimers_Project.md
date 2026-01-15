# 🧠 Early Alzheimer’s Detection Using Machine Learning
**MSc Business Analytics — University of Galway (2025)**
**Team: Brain Guardians**

This repository contains the implementation, analysis, and supporting materials for our final MSc project:
**“Enhancing Early Detection of Alzheimer’s Disease Using Predictive Analytics.”**

The project focuses on developing a scalable, non-invasive machine learning solution for early-stage Alzheimer’s prediction using simple clinical features such as **MOCA scores** and **Age**.
The full academic report is included in the `docs/` folder for reference.

---

## 📁 Repository Structure

```
├── data/
│   ├── sample_cleaned_dataset.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   ├── 03_model_training.ipynb
│   ├── 04_xgboost_final_model.ipynb
│
├── app/
│   ├── streamlit_app.py
│   ├── model.pkl
│
├── images/
│   ├── moca_distribution.png
│   ├── diagnosis_histogram.png
│   ├── confusion_matrix_xgb.png
│   ├── roc_curve_xgb.png
│
├── docs/
│   ├── Final_Project_Report.pdf
│
└── README.md
```

---

## 🎯 Project Objective

To build an accurate ML screening tool capable of identifying three cognitive states:

- **Cognitively Normal (CN)**
- **Mild Cognitive Impairment (MCI)**
- **Dementia**

The project uses non-invasive, easily collectible assessment data to support early detection.

---

## 📊 Dataset Overview

Data originates from **ADNI – Alzheimer’s Disease Neuroimaging Initiative**, integrating multiple data sources such as:

- MOCA, MMSE, CDR, FAQ
- Demographics
- Diagnosis metadata

After preprocessing:

- **700,000+** total records merged
- **131,061** usable rows for modeling

---

## 🔧 Methodology

### 1. Data Understanding
- Identified structure of ADNI tables
- Explored missingness
- Analyzed MOCA correlations

### 2. Data Preparation
- Cleaning invalid values
- Feature selection
- Encoding categorical data

### 3. Modeling
| Model | Accuracy | Notes |
|-------|----------|--------|
| Logistic Regression | ~52% | Baseline |
| Random Forest | 94% | Strong recall |
| XGBoost | **95%** | Best performer |

---

## 📈 Key Results

- **95% accuracy** using XGBoost
- Strong generalization across classes
- Improved MCI recall (critical for early diagnosis)

---

## 🖥 Demo Application

A Streamlit-based prototype allows input of **MOCA & Age** and returns diagnosis predictions.

Run:
```
streamlit run app/streamlit_app.py
```

---

## 🛠 Technologies Used

- Python, Pandas, NumPy
- Scikit-learn, XGBoost
- Streamlit
- Matplotlib, Seaborn

---

## 📄 Documentation

Full academic report available in:

```
docs/Final_Project_Report.pdf
```

---

## 👥 Contributors

**Arshaque Muhammed**
MSc Business Analytics — University of Galway (2024–2025)

---

## 🔗 License

For academic and educational use only.
