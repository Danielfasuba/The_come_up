# Machine Learning Projects

End-to-end machine learning notebooks: data exploration, cleaning, preprocessing pipelines, model comparison, tuning and evaluation on held-out data. Each folder has its own README covering the problem, approach and results.

| Project | Type | Data | Approach | Result |
|---|---|---|---|---|
| [Bankruptcy](Bankruptcy) | Binary classification, imbalanced | 92,872 companies, 558 bankrupt (0.6%) | Median imputation, clipping, log transform, scaling; SMOTE + random undersampling; logistic regression vs random forest; GridSearchCV | 0.88 cross-validated ROC-AUC. Random forest scored 0.9999 on training data but 0.80 in cross-validation, so logistic regression was chosen |
| [Malware_analysis](Malware_analysis) | Binary classification | 58,596 memory dumps (CIC-MalMem-2022) | Removed all-null features; logistic regression vs linear SVM | Linear SVM: 99.9% precision, 99.9% recall, 0.9999 ROC-AUC on the test set |
| [California_housing](California_housing) | Regression | 20,640 census districts | Imputation, one-hot encoding, scaling; linear, decision tree, random forest and SVR; grid and randomized search | Random forest test RMSE $49,039 (95% CI $46.9k–$51.1k), vs $69.0k for linear regression |
| [Cifar10_img_classification](Cifar10_img_classification) | Multi-class image classification | CIFAR-10, 60,000 images, 10 classes | 3 fully connected Keras networks with dropout, tracked in TensorBoard | 48.8% test accuracy; per-class recall from 19% (cat) to 68% (ship) |
| [Titanic](Titanic) | Binary classification | Kaggle Titanic | SVM with a scikit-learn preprocessing pipeline | Being reworked: see the Titanic README |

**Tools:** Python, pandas, NumPy, scikit-learn, imbalanced-learn, Keras/TensorFlow, Matplotlib, Seaborn, SciPy

Some projects follow published exercises and are credited in their READMEs (e.g. California Housing, from *Hands-On Machine Learning* by Aurélien Géron).
