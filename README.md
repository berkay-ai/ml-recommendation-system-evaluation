# ML Recommendation System Evaluation

![Python](https://img.shields.io/badge/Python-3.9-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-yellow)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-lightgrey)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red)

This project presents the development and evaluation of a recommendation system using matrix factorization (TruncatedSVD). The focus is not only on generating recommendations, but also on understanding model behavior under realistic conditions, including temporal validation, error analysis, and model reliability, with an emphasis on drift-aware evaluation and cost-efficient retraining strategies.

---

## Problem

Recommendation systems often degrade over time due to changing user behavior. Traditional evaluation approaches may fail to capture this issue, leading to models that perform well offline but struggle in real-world environments.

This project investigates how recommendation performance changes across time and highlights the importance of building adaptive, drift-aware systems.

---

## Approach

- Built a recommendation model using **TruncatedSVD** on implicit user-product interactions  
- Applied **temporal train-test split** to simulate real-world prediction scenarios  
- Evaluated performance using **Precision@10** and **Recall@10**  
- Conducted **error analysis**, including zero-hit rate evaluation  
- Used **Logistic Regression + LIME** for model interpretability  

---

## Key Findings

- The model achieved baseline performance but struggled with generalization across time  
- Temporal validation revealed significant performance degradation (including cases with near-zero accuracy)  
- A high **zero-hit rate** indicated limitations in capturing user preferences  
- The model showed sensitivity to changes in user behavior  

---

## Why It Matters

These findings demonstrate that model accuracy alone is not sufficient for production systems. 

Instead, machine learning systems must:
- Detect performance degradation over time  
- Adapt to evolving user behavior  
- Trigger retraining when necessary  

This project emphasizes the importance of **drift-aware evaluation** and **cost-efficient retraining strategies** in real-world machine learning systems.

---

## Project Structure
```bash
├── notebooks/
│ └── recommendation_system_final.ipynb
├── report/
│ └── final_report.pdf
└── README.md
```

---

## Dataset

This project uses the Instacart Online Grocery Shopping Dataset.

- Source: https://www.kaggle.com/c/instacart-market-basket-analysis

The dataset contains anonymized user-product interaction data and is used to simulate real-world recommendation scenarios.

---

## Notebook

The main implementation and evaluation pipeline can be found here:

👉 [Final Notebook](notebooks/recommendation_system_final.ipynb)

---

## Report

The full technical report is available here:

👉 [Final Report](report/final_report.pdf)

---

## Future Work

Next steps to productionize this system include:

- Implementing drift detection to monitor performance degradation  
- Defining retraining triggers based on performance thresholds  
- Introducing cost-aware retraining to balance performance and computation  
- Deploying the model via an API for real-time inference  



