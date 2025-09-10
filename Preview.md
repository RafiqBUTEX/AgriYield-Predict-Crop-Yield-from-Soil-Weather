# AgriYield-Predict-Crop-Yield-from-Soil-Weather.
Kaggle Competetion Limk: www.kaggle.com/competitions/agriyield-2025/overview
Predict crop yield from soil and weather data in the Kaggle AgriYield competition. Explored ~20 ML models, performed feature engineering, and submitted the best-performing model to the leaderboard. 
This project focuses on predicting maize yield (kg/ha) for agricultural fields using soil, weather, and vegetation data. The goal is to generate accurate predictions for submission in a Kaggle competition.

The dataset contains features such as soil pH, organic matter, sand percentage, temperature, humidity, rainfall, and NDVI, with yield as the target variable.

Dataset
Column	Description
field_id	Unique identifier for each field
soil_ph	Soil acidity (pH scale)
organic_matter	Percentage of organic matter in the soil
sand_pct	Percentage of sand in soil composition
temperature	Average temperature (°C) during growing season
humidity	Average relative humidity (%) during growing season
rainfall	Total rainfall (mm) during growing season
ndvi	Normalized Difference Vegetation Index (remote sensing)
yield	Target variable – maize yield in kg/ha

Train dataset: Includes all features + yield.

Test dataset: Includes all features except yield; predictions are submitted to Kaggle.

Approach

Data Preparation:

Cleaned and split the train dataset into training and validation sets.

Standardized and encoded features where necessary.

Model Exploration:

Tested over 20 different machine learning models, including:

Linear models (Linear Regression, Ridge, Lasso)

Tree-based models (Decision Tree, Random Forest, Gradient Boosting, XGBoost, LightGBM, CatBoost)

Support Vector Regressors (SVR, NuSVR)

Robust regressors (Huber, Poisson, Orthogonal Matching Pursuit)

k-Nearest Neighbors, KNN Regressor

Neural network based approaches (MLP)

Evaluated all models using MSE, RMSE, MAE, and R² on the validation set.

Model Selection:

Selected the model with the highest R² and lowest error metrics for final predictions.

For this competition, LightGBM provided the best performance among the tested models.

Prediction & Submission:

Generated predictions for the test dataset.

Created a CSV submission file with field_id and predicted yield.


Dependencies

Python ≥ 3.8

Pandas

NumPy

scikit-learn

LightGBM, XGBoost, CatBoost

Matplotlib / Seaborn (optional)

Submission

Output CSV (submission.csv) contains the following columns:

field_id

yield

Notes

Explored multiple models to find the optimal approach for prediction.

Feature engineering and hyperparameter tuning were performed to improve model accuracy.

Validation metrics were calculated on an internal split before submission to Kaggle.
