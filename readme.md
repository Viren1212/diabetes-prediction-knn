Diabetes Prediction using KNN

Binary classification on the Pima Indians dataset to predict diabetes.

Dataset
768 patients, 8 features, slightly imbalanced (500 vs 268)

 What I did
- Replaced invalid 0s with NaN, imputed using training median only
- Feature selection using Mutual Information on training data
- Scaled with StandardScaler, handled imbalance with SMOTE
- Tuned `k` using 5-fold cross-validation (no test set peeking)
- Used recall as primary metric — missing a diabetic is more costly than a false alarm 

 Results
| | Recall (Diabetic Class) | Accuracy |
|---|---|---|
| Without SMOTE | 0.60 | 0.80 |
| With SMOTE | 0.80 | 0.80 |

 Tech Stack
Python, Pandas, Scikit-learn, Imbalanced-learn, Seaborn
