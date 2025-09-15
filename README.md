# DA5401 — Assignment 4: GMM-based Synthetic Sampling for Class Imbalance  

**Student Name:** Praveen  
**Roll Number:** MM22B014  
**Course Code:** DA5401  
**Assignment:** A4 — Gaussian Mixture Model (GMM) for Oversampling & Comparative Analysis  

---

## ▶️ How to Run

1. Open `DA5401_Assigment4_MM22B014.ipynb` in **Google Colab** or Jupyter.  
2. Place the dataset file **`creditcard.csv`** in the same folder.  
3. Run all cells sequentially to reproduce the results.  

---

## 📌 Summary of Work

- Preprocessed the **credit card fraud dataset**, isolating the minority (fraud) class for targeted resampling.  
- Built a **Baseline Logistic Regression model** to understand class imbalance effects.  
- Implemented **GMM-based synthetic sampling**:  
  - Fit Gaussian Mixture Models (GMM) on the minority class.  
  - Selected the best number of components using **BIC (Bayesian Information Criterion)**.  
  - Generated synthetic fraud samples from the fitted probability distribution.  
- Compared models across:  
  - **Baseline** (no resampling)  
  - **GMM Oversampling**  
  - **Clustering-Based Undersampling + GMM (CBU+GMM)**  
- Evaluated performance using **Precision, Recall, and F1-score**, focusing on fraud detection.  
- Plotted **comparison bar charts** for visual analysis.  

---

## 🔎 Key Findings

- **Baseline:** Good balance with high precision (~0.83) and moderate recall (~0.64).  
- **GMM Oversampling:** Boosted recall (~0.91) but collapsed precision (~0.08), leading to very poor F1.  
- **CBU+GMM:** Similar to GMM oversampling — very high recall but impractically low precision.  
- **Final Recommendation:**  
  - GMM oversampling, while theoretically powerful for multimodal distributions, was **not effective here**.  
  - It improved recall but caused excessive false alarms, making the model unreliable.  
  - The baseline model gave the best practical trade-off.  
  - Alternative resampling methods like **SMOTE+ENN, ADASYN, or refined GMM strategies** may yield better balance.  

---
