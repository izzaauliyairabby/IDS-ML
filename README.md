1. Introduction

- Objective: Evaluate Decision Tree and Random Forest classifiers for network intrusion detection using the CIC IDS 2018 dataset.
- Dataset: CIC IDS 2018, focusing on processed traffic data suitable for machine learning algorithms.

2. Dataset Overview

- Source: Downloaded from AWS S3 using aws s3 sync.
- Selection: Chose "Friday-02-03-2018" and "Friday-16-02-2018" due to balanced labels ("Benign" and combined 
  "Malicious").
- Preprocessing: Removed columns, handled missing values, duplicates, resulting in "processed_friday_dataset.csv".
- Labeling: Aggregated "Bot", "DoS attacks-SlowHTTPTest", and "DoS attacks-Hulk" into "Malicious" category.

Dataset
* CIC-IDS-2018 Processed Traffic Data for ML Algorithms on my Google Drive: [Drive](https://drive.google.com/file/d/1cJECqTj7ExPuwCddrCPB5RTnuk5NKvCF/view?usp=sharing)
* Processed Friday dataset "__processed_friday_dataset.csv__" that was used in the baseline experiments: [Drive](https://drive.google.com/file/d/1PaRrET5dDzJPFwGa7bUMmIwjQmE9otTb/view?usp=sharing)
* 
3. Experimental Setup

- Software: Ubuntu 18.04 for environment consistency.
- Packages: Managed via requirements.yml for reproducibility.
- Hardware: i9-9900KF CPU overclocked to 5 GHz, 32 GB DDR4 RAM at 3200 MHz.
4. Model Training

- Algorithms: Decision Tree Classifier and Random Forest Classifier.
- Techniques: Grid Search with 5-fold Cross Validation for hyperparameter tuning.
- Metrics: Accuracy, Macro Average Precision, Recall, and F1-Score.
5. Results and Analysis

- Decision Tree Classifier:

- Accuracy: 99.982%
- Macro Average Precision: 99.969%
- Macro Average Recall: 99.978%
- Macro Average F1-Score: 99.974%
- Random Forest Classifier:

- Accuracy: 99.904%
- Macro Average Precision: 99.787%
- Macro Average Recall: 99.926%
- Macro Average F1-Score: 99.856%
6. Conclusion

Findings: Both classifiers performed exceptionally well, with Decision Tree slightly outperforming Random Forest.
Next Steps: Explore ensemble methods, deep learning approaches, and real-time deployment feasibility.
7. References

Sharafaldin, Iman & Habibi Lashkari, Arash & Ghorbani, Ali. (2018). Toward Generating a New Intrusion Detection Dataset and Intrusion Traffic Characterization. 108-116. 10.5220/0006639801080116.
8. Appendix

Dataset Access: CIC-IDS-2018 Processed Traffic Data
Processed Dataset: processed_friday_dataset.csv
