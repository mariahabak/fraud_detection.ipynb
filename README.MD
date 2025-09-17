💳 Credit Card Fraud Detection (Unsupervised Learning)

📌 Project Overview
This project was developed as part of the AI Engineer Accelerator Program with Lara Wehbe.
The goal is to use unsupervised learning techniques to detect fraudulent credit card transactions — a real-world challenge due to the extreme class imbalance (frauds are <1% of transactions).

📂 Dataset
 [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  
-284,807 transactions
-Features: 28 anonymized PCA components + Amount + Time
-Target: Class (0 = Normal, 1 = Fraud) → hidden during training, used only for evaluation

# Methods
The following models were applied:
1-One-Class SVM – anomaly detection
2-Isolation Forest – tree-based anomaly detection
3-Autoencoder – deep learning for reconstruction errors
4-Logistic Regression – baseline supervised model (for comparison only)

Data preprocessing included:
-Feature scaling with StandardScaler
-Train/test split (80/20)
-Dimensionality reduction for visualization

# Results 

| Model                 | Accuracy | Precision | Recallm | F1-Score|
|-----------------------|----------|-----------|--------|-------|
| One-Class SVM         | 94.96%   | 0.029     | 0.878  | 0.057 |
| Isolation Forest      | 99.80%   | 0.391     | 0.255  | 0.309 |
| Autoencoder           | 95.13%   | 0.030     |  0.878 | 0.058 |
| Logistic Regression   | 97.55%   | 0.061     | 0.918m | 0.114 |

# How to Run
Clone the repository
bash
git clone https://github.com/mariahabak/fraud_detection.ipynb.git
cd fraud_detection




# Key Insights
-Unsupervised models (SVM, Autoencoder): Very high recall (caught most frauds) but too many false positives.
-Isolation Forest: More balanced, but missed some frauds.
-Logistic Regression (baseline): Best compromise (~92% recall), though precision remained low.


Fraud detection is always a trade-off between recall (catching all fraud) and precision (avoiding false alarms).

# Learning Outcomes
-Learned how unsupervised learning can be applied to rare-event detection.
-Practiced anomaly detection on highly imbalanced datasets.
-Understood the importance of evaluating models using precision, recall, and F1-score, not just accuracy.

# Next Steps
-Try ensemble methods combining Isolation Forest + Autoencoder.
-Experiment with SMOTE or oversampling for supervised baselines.
-Tune decision thresholds to optimize the precision-recall trade-off.



