# House Price Prediction

A machine learning project for predicting house prices using the Kaggle House Prices dataset.

## Dataset

- Competition: House Prices - Advanced Regression Techniques
- Platform: Kaggle

## Pipeline 1

### Data Cleaning
- Removed features with more than 50% missing values
- Kept remaining missing values
- No duplicate rows found
- No outlier removal

### Data Preprocessing
- Separated `SalePrice` and `Id`
- Applied manual ordinal encoding
- Applied one-hot encoding for nominal features
- Applied log transformation to highly skewed numerical features (only 4 feature removed with threshold(50%>))
- No feature scaling for tree-based models
- Filled remaining missing values with `0` before training XGBoost (`fillna(0)`) (on 5th file)

### Model
- XGBoost Regressor

## Results

| Version | Model | Kaggle Public Score |
|---------|-------|--------------------:|
| Pipeline 1 v1 | Baseline XGBoost | **0.12477** |

## Next Steps

- Better missing value imputation
- Feature engineering
- Hyperparameter tuning
- Pipeline 2 experiments