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

These preprocessing steps were essential to improve model performance and ensure accurate application of differential privacy mechanisms.

---

## Individual Contributions

- **Galib Abdun Noor**: Leading the implementation of Laplace and Gaussian noise mechanisms, handling dataset preprocessing, and analyzing the effects of privacy noise.
- **Jayashree Janani Purushothaman**: Conducting data exploration and developing visualizations to assess privacy noise impact.
- **Hunain Munir Surahio**: Researching differential privacy techniques and helping debug and optimize the noise mechanisms.
- **Farhana Ahmed**: Conducting a literature review on privacy-preserving techniques and contributing to documentation and report writing.

---

## Challenges Encountered

- **Handling Missing Data**: Required imputation techniques to ensure the dataset remained complete after applying noise.
- **Balancing Privacy and Utility**: Choosing the optimal privacy budget (ε, δ) was challenging, as too much noise degrades data utility.
- **Computational Efficiency**: Large-scale data transformations required optimization techniques to improve runtime performance.
- **Effect on Fraud Detection**: Differential privacy mechanisms sometimes altered the classification boundaries, requiring careful tuning.

---

## Plan for Completion

- **Finalizing Noise Parameters**: Experiment with different privacy budgets (ε, δ) and evaluate their impact on fraud detection accuracy.
- **Model Training and Evaluation**: Apply privacy-preserving data to machine learning models and compare performance.
- **Further Visualizations**: Develop scatter plots, box plots, and privacy-utility graphs to better understand privacy effects.
- **Report Completion**: Draft and format the final report using the ACM LaTeX template.
- **Presentation Preparation**: Develop slides for the group presentation, scheduled for March 26, 2025.

---

## Timeline of Activities

| Phase | Task Description | Timeline |
|-------|-------------------|----------|
| Phase 1 | Literature review on differential privacy & fraud detection | Jan 15 - Jan 25, 2025 |
| Phase 2 | Data collection and preprocessing | Jan 26 - Feb 5, 2025 |
| Phase 3 | Working on Laplace and Gaussian mechanisms | Feb 6 - Feb 18, 2025 |
| Phase 4 | Analyzing the impact of noise and generating visualizations | Feb 19 - Feb 28, 2025 |
| Phase 5 | Fine-tuning privacy parameters & evaluating model performance | Mar 1 - Mar 10, 2025 |
| Phase 6 | Writing the final report & formatting in ACM LaTeX | Mar 11 - Mar 20, 2025 |
| Phase 7 | Presentation preparation | Mar 21 - Mar 25, 2025 |
| Final Phase | Group presentation | Mar 26, 2025 |

---

## References

1. C. Dwork and A. Roth, "The Algorithmic Foundations of Differential Privacy," *Foundations and Trends in Theoretical Computer Science*, vol. 9, no. 3–4, pp. 211–407, 2014.
2. M. Abadi et al., "Deep Learning with Differential Privacy," in *Proceedings of the 2016 ACM SIGSAC Conference on Computer and Communications Security*, New York, NY, USA: ACM, 2016, pp. 308–318.
3. Y.-A. Le Borgne et al., "Reproducible Machine Learning for Credit Card Fraud Detection – Practical Handbook," *International Journal of Data Science and Analytics*, vol. 5, no. 4, pp. 285–300, 2018.
4. B. Lebichot et al., "Incremental Learning Strategies for Credit Card Fraud Detection," *IEEE Transactions on Neural Networks and Learning Systems*, vol. 29, no. 8, pp. 3784–3797, 2018.
5. I. Mironov, "Rényi Differential Privacy," in *Proceedings of the 30th IEEE Computer Security Foundations Symposium*, 2017, pp. 263–275.
6. F. McSherry and K. Talwar, "Mechanism Design via Differential Privacy," in *Proceedings of the 48th Annual IEEE Symposium on Foundations of Computer Science*, 2007, pp. 94–103.

---

This `README.md` file can now be used to describe your **Differential Privacy in Data Analytics** project on GitHub. Just create the `README.md` file in your repository and paste this content into it. Let me know if you need any further modifications!
