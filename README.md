# California-Housing-Price-Prediction
# California Housing Price Prediction (HistGradientBoostingRegressor)

**Project:** Regression model to predict median house value using the California Housing dataset.

**Language:** Python 3.9+  
**Libraries:** scikit-learn, pandas, numpy, joblib

## Project structure

california-housing-ml/
├── main_regression.py
├── requirements.txt
└── README.md

bash
Copy code

## Setup

1. (Optional) Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate    # macOS / Linux
venv\Scripts\activate       # Windows
Install dependencies:

bash
Copy code
pip install -r requirements.txt
requirements.txt:

shell
Copy code
scikit-learn>=1.2
pandas
numpy
joblib
Run
bash
Copy code
python main_regression.py
This script will:

Load the California Housing dataset

Split train/test (stratified by a binned target)

Use Pipeline (optional robust scaler + HistGradientBoostingRegressor)

Run RandomizedSearchCV over a compact search space

Evaluate with RMSE and R² on test set

Save the trained pipeline to regressor_artifact.joblib

Next steps / suggestions
Try LightGBM/XGBoost for speed on larger datasets.

Add feature engineering (interaction terms, polynomial features).

Add SHAP explainability and a small Flask API to serve predictions.