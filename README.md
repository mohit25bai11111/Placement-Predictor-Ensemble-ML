# 🎓 Student Placement Intelligence System (SPIS)
**An Ensemble Machine Learning Approach to Career Readiness Prediction**

![Python](https://img.shields.io/badge/Python-3.13-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)
![Status](https://img.shields.io/badge/Project-VITyarthi--BYOP-green.svg)
![Accuracy](https://img.shields.io/badge/Model_Accuracy-100%25-brightgreen.svg)

---

## 👤 Project & Author Details

| Detail | Information |
| :--- | :--- |
| **Project Name** | Student Placement Intelligence System (SPIS) |
| **Lead Developer** | **Mohit Pillai** |
| **Registration Number** | **BAI11111** |
| **Course Code** | CSA2001 — Artificial Intelligence & Machine Learning |
| **Semester** | Winter Semester 2025–26 |
| **Institution** | VIT-VITyarthi Programme |
| **Project Category** | Ensemble Predictive Analytics |
| **Submission Type** | Build Your Own Project (BYOP) |

---

## 🚀 Project Overview
The **Student Placement Intelligence System (SPIS)** is a high-level predictive framework designed to quantify "Placement Readiness" as a probabilistic **Confidence Score**. By moving beyond binary classification, the system provides a granular percentage-based result (e.g., **94.23%**), helping students identify specific levers for career improvement.

### 🧠 The Ensemble Architecture
To ensure maximum stability and zero misclassifications, the architecture integrates a **Soft-Voting Ensemble**:
1. **Logistic Regression:** Establishes a linear probability baseline.
2. **Random Forest (100 Estimators):** Captures complex non-linear feature interactions via Bagging.
3. **SVM (RBF Kernel):** Optimizes the separating hyperplane for robust margin classification.

---

## 📊 Key Performance Metrics
Based on the final execution in `Placement_Predictor_Ensemble.ipynb`:
* **Test-Set Accuracy:** 100.00%
* **Confusion Matrix:** 71 True Negatives | 29 True Positives (0 Misclassifications)
* **Target Result:** 94.23% Confidence achieved for high-tier student profiles.

### 📋 Holistic Feature Analysis
| Feature | Range | Role in Prediction |
| :--- | :--- | :--- |
| **CGPA** | 0.0 - 10.0 | Primary academic filter |
| **Aptitude Score** | 50 - 100 | Cognitive ability signal |
| **Internships** | 0 - 3 | **Top Positive Predictor** (Weight: 0.365) |
| **Projects** | 1 - 5 | Practical skill demonstrator |
| **Backlogs** | 0 - 3 | **Strongest Penalty** (Negative weight) |
| **Communication** | 1 - 10 | Interview readiness indicator |

---

## 🛠️ Technical Implementation
### 🔹 Feature Scaling (Standardization)
I implemented **StandardScaler** to normalize the data, ensuring that features with large ranges (Aptitude) do not mathematically overpower smaller ranges (CGPA):
$$z = \frac{x - \mu}{\sigma}$$

### 🔹 Explainable AI (XAI)
SPIS utilizes **Gini Importance** to provide transparency. Analysis confirms that industry exposure (Internships) and technical depth (Projects) are the most significant drivers for recruitment success.

---

## 📁 Repository Structure
```text
Student-Placement-System/
├── data/
│   └── placement_data.csv        # Engineered synthetic dataset
├── notebooks/
│   └── Placement_Predictor_Ensemble.ipynb # Full ML Pipeline
├── src/
│   └── model_trainer.py          # Core Ensemble logic
├── requirements.txt              # Dependency list
└── README.md                     # Project documentation
