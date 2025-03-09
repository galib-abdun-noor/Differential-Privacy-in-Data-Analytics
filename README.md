# Differential Privacy in Data Analytics: Midterm Progress Report

## Overview of Achievements to Date

This project focuses on implementing differential privacy techniques in data analytics, specifically on the Credit Card Fraud Detection Dataset. The goal is to apply Laplace and Gaussian mechanisms to protect sensitive transaction data while maintaining utility. Our progress so far includes:

- **Data Preprocessing**: Cleaned and standardized the dataset, handling missing values and feature scaling.
- **Ongoing Implementation of Differential Privacy Mechanisms**: Currently working on applying Laplace and Gaussian noise to transaction amounts and analyzing their impact.
- **Visualization and Initial Analysis**: Generated histograms and distribution plots to assess how noise affects data patterns.
- **Research on Privacy-Utility Trade-offs**: Conducted a literature review on differential privacy in financial transactions.

Moving forward, we aim to fine-tune privacy parameters (ε and δ) and evaluate their effect on fraud detection accuracy.

---

## Dataset Description

We use the **Credit Card Fraud Detection Dataset**, which contains 284,807 anonymized transactions, with 0.27% labeled as fraudulent. The dataset presents challenges due to its highly imbalanced nature and the fact that most features have undergone Principal Component Analysis (PCA) transformation.

### Key Features:
- **V1 - V28** (Principal Components): Encoded representations of transaction details, extracted using PCA.
- **Amount**: Represents the transaction value; useful for anomaly detection.
- **Time**: Indicates the time elapsed since the first recorded transaction.
- **Class** (Target Variable): Binary label where 0 = Legitimate transaction, 1 = Fraudulent transaction.

### Challenges with This Dataset:
- **Data Imbalance**: Fraud cases are rare, requiring special handling techniques such as oversampling, undersampling, or synthetic data generation.
- **Noise Sensitivity**: Adding differential privacy noise could obscure patterns in fraudulent transactions, affecting fraud detection accuracy.
- **PCA-Transformed Features**: Lack of direct interpretability makes it harder to predict the impact of noise addition.

### Preprocessing Summary:
- **Class Distribution Analysis**: Identified a significant imbalance between fraudulent and non-fraudulent transactions.
- **Handling Missing Values**: Verified and removed any NaN entries to maintain dataset integrity.
- **Feature Normalization**: Normalized numerical features such as Amount and Time using **RobustScaler**, which helps mitigate the impact of outliers.
- **Dataset Reordering**: Scaled values were reordered to maintain consistency in the dataset structure.

![Untitled](https://github.com/user-attachments/assets/279e503e-1c5c-4ced-9641-ee5cee368b4a)

Figure 1 & 2: Class Distribution Before and After Preprocessing

These preprocessing steps were essential to improve model performance and ensure accurate application of differential privacy mechanisms.

---

