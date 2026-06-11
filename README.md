# 🧬 QSAR-Based Bioactivity Prediction

> Predicting the bioactivity of DHFR–TS inhibitors using molecular fingerprints and classical ML.

![Banner](screenshots/banner.png)

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![RDKit](https://img.shields.io/badge/RDKit-Cheminformatics-blue?style=flat)](https://www.rdkit.org)

---

## 📌 Overview

|                 |                                                       |
| --------------- | ----------------------------------------------------- |
| **Target**      | DHFR–TS                                               |
| **Data Source** | ChEMBL                                                |
| **Task**        | Regression (pIC50) + Classification (active/inactive) |
| **Approach**    | Molecular Fingerprints → ML Models → Benchmarking     |

---

## 📸 Screenshots

| EDA & Distribution          | Model Performance                   |
| --------------------------- | ----------------------------------- |
| ![EDA](screenshots/eda.png) | ![Results](screenshots/results.png) |

| Fingerprint Comparison                        | App Workflow                         |
| --------------------------------------------- | ------------------------------------ |
| ![Fingerprints](screenshots/fingerprints.png) | ![App](screenshots/app_workflow.png) |

---

## ✨ Features

- Molecular descriptor generation: **[e.g. Morgan/ECFP4, MACCS Keys, RDKit Topological]**
- Models benchmarked: **[e.g. Random Forest, XGBoost, SVM, KNN]**
- Scaffold-aware train/test splitting to prevent data leakage
- Regression + classification metrics (R², RMSE, AUC, MCC)
- Interactive prediction app (Streamlit / Gradio)

---

## 📁 Project Structure

```
├── dataset/
│   ├── raw/                    # Raw data from ChEMBL / BindingDB
│   └── processed/              # Cleaned & featurized datasets
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_modeling.ipynb
│   └── 04_benchmarking.ipynb
│
├── src/
│   ├── descriptors.py          # Fingerprint generation
│   ├── preprocessing.py
│   ├── train.py
│   └── evaluate.py
│
├── models/                     # Saved .pkl / .joblib artifacts
├── screenshots/                # Graphs and app workflow images
├── app.py                      # Prediction app entry point
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/Sakhiur2022/QSAR-modeling-for-DHFR-TS
cd QSAR-modeling-for-DHFR-TS

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

---

## 📊 Results Summary

| Fingerprint  | Model         | R²  | RMSE | AUC |
| ------------ | ------------- | --- | ---- | --- |
| Morgan/ECFP4 | Random Forest | —   | —    | —   |
| MACCS Keys   | XGBoost       | —   | —    | —   |
| RDKit Topo   | SVM           | —   | —    | —   |

> Fill in after experiments are complete.

---

## 🗂️ Dataset

- **Source:** [ChEMBL](https://www.ebi.ac.uk/chembl/)
- **Target:** DHFR–TS
- **Size:** ~[N] compounds after filtering
- **Activity Metric:** IC50 → converted to pIC50

---

## 🤝 Connect

**Sakhiur** · [LinkedIn](https://www.linkedin.com/in/sakhiur/) · [Portfolio](https://sakhiur.vercel.app)

---

## 📄 License

[MIT](LICENSE)
