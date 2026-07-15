# House Price Prediction

A machine learning project for predicting house prices using the Kaggle House Prices dataset.

## Dataset

- **Competition:** House Prices - Advanced Regression Techniques
- **Platform:** Kaggle

## Pipeline

### Data Cleaning
- Removed features with more than 50% missing values
- Kept remaining missing values for later handling
- No duplicate rows found
- No outlier removal

### Data Preprocessing
- Separated `SalePrice` and `Id`
- Applied manual ordinal encoding
- Applied one-hot encoding for nominal features
- Applied log transformation to the target (`SalePrice`)
- No feature scaling for tree-based models
- Filled remaining missing values with `0` before model training


### Feature Engineering
Created new features such as:

- TotalSF
- TotalBathrooms
- TotalPorchSF
- TotalRooms
- TotalOutdoorArea
- LivingArea_to_LotArea
- HouseAge
- RemodelAge
- IsRemodeled
- HasSecondFloor
- HasBasement
- HasGarage
- HasFireplace
- HasPool
- Quality_x_Area
- Quality_x_TotalSF


## Models Evaluated

- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Random Forest
- LightGBM
- XGBoost

## Hyperparameter Tuning

Optimized the XGBoost model using **GridSearchCV** with 5-Fold Cross Validation.

## Results

| Version | Description | CV RMSE | Kaggle Public Score |
|---------|-------------|--------:|--------------------:|
| v1 | Baseline XGBoost | 0.12651 | **0.12477** |
| v2 | XGBoost + Feature Engineering | 0.12507 | **0.12169** |
| v3 | XGBoost + Feature Engineering + Hyperparameter Tuning | **0.12071** | **0.11840** |

📈 Improved from **0.12477 → 0.11840** after Feature Engineering and Hyperparameter Tuning.

🏆 **Best Kaggle Public Score:** **0.11840**

🏅 **Best Kaggle Ranking:** **198th Place**

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- LightGBM
- Matplotlib
- Seaborn

## Future Improvements

- Experiment with alternative preprocessing pipelines
- Compare different missing value imputation strategies
- Investigate outlier removal
- Model ensembling / stacking
