# Challenge — CatBoost Regression 🐆

A project for predicting real-estate prices in Melbourne using **CatBoostRegressor**.  
Completed as part of a Data Science educational competition on the Stepik platform.

Result: MAPE improved from 14.32 → 14.07

Kaggle Notebook:  [Challenge — CatBoost Regression](https://www.kaggle.com/code/ivan4956/challenge-catboost-regression) *(Viewing on Kaggle is recommended — the notebook is easier to read there.)*

---

## Dataset

- Real-estate prices in Melbourne
- Size: 23,000+ objects, 19 features
- Many missing values (up to 47% in some features)

---

## Main Stages

#### 1. EDA (Exploratory Data Analysis)

- Analysis of target variable (Price)
- Geospatial visualization by coordinates and districts
- Correlation analysis (numeric + categorical)
- Multicollinearity inspection


#### 2. DATA PROCESSING

**Handling Missing Values**
- Group-level imputation (Type + Rooms, Suburb + Street)
- Using group medians instead of global
- Contextual handling of coordinates and construction year

**Feature Engineering**
- `Street` - street name extracted from full address
- `Building_Age` - age of building at time of sale
- Categorical grouping: `Distance_Group`, `Bathroom_Group`, `Car_Group`,  `Landsize_Group`, `BuildingArea_Group`

**Preprocessing**
- Data type optimization (float32, int32, category)
- Native CatBoost categorical processing


#### 3. MODELING

**Baseline**
- Simple median imputation
- Default CatBoost parameters
- MAPE: 14.32

**Final Model**
- Grid Search over: `learning_rate`, `depth`, `l2_leaf_reg`
- Optimal params: `depth=6`, `learning_rate=0.068`, `l2_leaf_reg=3`
- Validation + early stopping
- MAPE: 14.07


#### 4. RESULTS ANALYSIS

- Key features: `Lattitude`, `Longtitude`, `Distance`
- SHAP interpretation
- Visualization: learning curves, feature importance

---

## Conclusion

CatBoost demonstrated strong performance for housing-price prediction.  
With minimal tuning and proper handling of missing data, it showed great results.

Sometimes simple solutions work best - a default CatBoost model landed in the **top 20%** of all participants.  
Further tuning improved performance even more.


## Tech Stack

`Python` • `Pandas` • `NumPy` • `CatBoost` • `Scikit-learn` • `Matplotlib` • `Seaborn` • `Phik`
