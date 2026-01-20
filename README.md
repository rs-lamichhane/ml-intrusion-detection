# Machine Learning for Cyber Security: Intrusion Detection Pipeline

This repository contains a two-stage machine learning pipeline designed to detect and classify network intrusions efficiently. It was developed as part of the CMM541 module.

> **Note on Academic Integrity:** The source code for this project is kept private to comply with university policies regarding coursework and plagiarism. This repository serves as a high-level architectural and methodological overview.

## Architecture

The system uses a hybrid approach to balance computational efficiency with detection accuracy:

1. **Stage 1 (Binary Detection):** Uses network flow features (e.g., Failed Logins, IP Reputation) to quickly filter out benign traffic. Built using a **Random Forest Classifier**.
2. **Stage 2 (Multi-class Classification):** Applies Natural Language Processing (TF-IDF vectorizer + Random Forest) on unstructured attack descriptions *only* for traffic flagged by Stage 1, significantly reducing processing overhead.

## Performance Metrics

* **Stage 1 Precision:** 98.3%
* **Stage 1 F1-Score:** 84.9%
* **Stage 1 Recall:** 74.7%
* **Processing Overhead Reduction:** ~99%

## Technologies Used
* Python
* Scikit-learn
* XGBoost
* Imbalanced-learn (SMOTE)
* Pandas / NumPy

## Structure
* `notebooks/Lab_Coursework.ipynb`: Contains the full data preprocessing, exploratory data analysis, model training (Random Forest, XGBoost, DNN, Logistic Regression), and evaluation code.
