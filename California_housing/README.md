## California Housing Price Prediction

### Overview

The California Housing task involves building a predictive model for housing prices in California using census data. This dataset includes features such as population, median income, median housing price (target variable), median age, and more for various districts in California. The primary objective is to develop a model capable of accurately predicting the median housing price for each block group (district) in California.

### Data Exploration

I initiated the project by conducting a comprehensive exploration of the dataset using Pandas. This exploration included:

- **Descriptive Statistics:** I examined informative statistics to gain insights into the dataset's key characteristics.
- **Data Visualization:** Visualizing the dataset through histograms and other graphical representations helped me understand the distribution of various attributes.

This initial analysis revealed that the task is a supervised learning problem, specifically a regression task.

### Data Preprocessing

To prepare the data for machine learning algorithms, I employed several essential tools from Scikit-Learn:

- **Handling Missing Values:** I used the SimpleImputer to address missing data points, ensuring data completeness.
- **Encoding Categorical Attributes:** For converting categorical attributes from text to numerical format, I utilized both OrdinalEncoder and OneHotEncoder.
- **Feature Scaling:** StandardScaler was employed to scale the features appropriately.

### Model Training and Evaluation

I trained and evaluated four different regression algorithms:

1. **Linear Regression**
2. **Decision Tree Regression**
3. **Random Forest Regression**
4. **Support Vector Regression**

The performance metric used in evaluation was the Root Mean Square Error (RMSE). Out of these algorithms, the Random Forest Regressor emerged as the top-performing model, exhibiting superior predictive capabilities compared to the others.

### Hyperparameter Tuning

After identifying the Random Forest Regressor as the most promising model, I conducted fine-tuning to optimize its hyperparameters. This process involved selecting the combination of hyperparameters that produced the best results.

### Model Evaluation

The final model, based on the Random Forest Regressor with optimized hyperparameters, underwent evaluation on a separate test dataset. The evaluation demonstrated that the model's performance closely mirrored its performance on the training set, indicating its robustness and generalization ability.

### Conclusion

In conclusion, the Random Forest Regressor outperforms other regression algorithms, including linear regression, decision tree regression, and support vector regression, for predicting housing prices in California. This project showcases the power of machine learning in solving real-world regression tasks and can serve as a valuable resource for housing market analysis in California.

- **Project source:** https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/ (Book)