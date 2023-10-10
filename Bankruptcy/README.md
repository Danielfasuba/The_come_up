## Bankruptcy Prediction

### Overview

Financial institutions, fund managers, lenders, and players in the financial markets often need reliable models to assess the risk of bankruptcy. This project's goal is to develop a bankruptcy prediction model. The dataset includes features like Earnings per share, liquidity, operational margin, and more.

### Exploratory Data Analysis

Here, I found that the dataset consists entirely of numerical feature attributes. Since there are no categorical or textual features, encoding transformations are unnecessary. However, missing values exist in all attributes, and many have high standard deviations, suggesting outliers or long-tailed distributions. Proper handling of missing data and outlier detection is crucial for accurate analysis and modeling. A significant class imbalance is also observed, posing a challenge for linear models.

### Data Processing

During data processing, I applied several steps to prepare the dataset:

- Missing values in features were filled using median values due to low ranges observed along quartiles of feature atrributes.
- A clipping process was performed to truncate extremely negative values.
- Log transforms were applied to mitigate outlier influence.
- All attributes were scaled to ensure consistency and comparability.

### Model Development

Two baseline algorithms, Logistic Regression and Random Forest Classifier, were trained to address the classification problem on a resampled dataset. Upon evaluating the models, it was found that the Random Forest Classifier achieved a better roc_auc score compared to the Logistic Regression model. Fine-tuning with GridSearchCV was conducted on the Training + Validation set. Interestingly, Logistic Regression outperformed Random Forest Classifier, suggesting overfitting in the latter during initial training.

### Model Evaluation and Testing

The ROC_AUC metric, measuring both Recall and False Positive Rate, was chosen for model evaluation. The reason for selecting this performance metric was to consider both the Recall and the FPR. Recall measures the proportion of correctly predicted positive instances (in this case, cases of bankruptcy) out of the total actual positive instances. Since the focus of the analysis is on identifying cases of bankruptcy (positive predictions), it is crucial to evaluate the model's ability to correctly classify such instances. Additionally, the False Positive Rate computes the ratio of non-bankrupt instances that are incorrectly classified as bankrupt. This metric is important to assess the model's specificity or its ability to correctly identify non-bankrupt instances

This project aims to create a robust bankruptcy prediction model, considering the complexities of financial data and class imbalance.