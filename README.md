# House Prices Prediction
Solution to kaggle competition: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques). The objective is to predict the final price of residential homes based on various features.

## Project Structure

- **`train.csv`**: Training dataset provided by Kaggle.
- **`test.csv`**: Test dataset provided by Kaggle.
- **`data_description.txt`**: Detailed description of all features in the dataset.
- **`house_solution.ipynb`**: Jupyter Notebook with data preprocessing, feature engineering, model training, and evaluation.
- **`best_params.json`**: JSON file storing the optimal hyperparameters for models used in the Stacking Regressor.
- **`submission.csv`**: Final submission file containing predictions for the test dataset.

## Methodology

### Data Preprocessing
1. **Handling Missing Values**:
   - Imputation by replacement or removal depending on the feature.
   
2. **Outlier Removal**:
   - Identified and removed significant outliers to improve model robustness.

3. **Skewness Correction**:
   - Applied transformations to reduce skewness in target and numerical features.

4. **Categorical Encoding**:
   - **Frequency Encoding** for features with high cardinality.
   - **One-Hot Encoding** for features with low cardinality.

5. **Feature Scaling**:
   - Standardized numerical features to improve model performance.

### Model Training
1. Multiple regression models were trained:
   - ElasticNet
   - Lasso
   - Ridge
   - Random Forest Regressor
   - Gradient Boosting Regressor
   - XGBRegressor

2. **Stacking Regressor**:
   - Combined the predictions from the above models to enhance accuracy.

### Hyperparameter Optimization
- Used **K-fold Cross-Validation** and **GridSearchCV** to find the best hyperparameters.
- The optimal parameters are saved in `best_params.json`.

### Submission
- Predictions were made using the final Stacking Regressor and saved in `submission.csv`.
