# Weather Trend Forecasting

## Project Overview

This project focuses on analyzing global weather data, identifying temperature patterns, and developing machine learning models to predict temperature based on geographical and time-related features.

It covers an end-to-end machine learning workflow, including data cleaning, exploratory data analysis, anomaly detection, geographical analysis, feature importance, model comparison, hyperparameter tuning, and model validation.

## Dataset

- **Dataset:** Global Weather Repository
- **Records:** 170,927
- **Country-name entries:** 211
- **Date range:** May 2024 – October 2026
- **Target variable:** Temperature (°C)

The dataset contains geographical information, timestamps, temperature readings, and other weather-related variables.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- XGBoost
- Joblib
- Jupyter Notebook

## Project Workflow

### 1. Data Cleaning and Preprocessing

- Checked and handled missing values and duplicate records.
- Converted date columns into datetime format.
- Identified and corrected suspicious temperature readings.
- Verified Celsius and Fahrenheit consistency.
- Compared StandardScaler and MinMaxScaler on selected numerical features.

### 2. Exploratory Data Analysis (EDA)

- Analyzed temperature distributions.
- Studied daily temperature trends.
- Visualized weather condition frequencies.
- Examined correlations between numerical features.

### 3. Anomaly Detection

- Applied Isolation Forest to identify unusual temperature observations.
- Visualized normal and anomalous records.
- Examined extreme temperature readings.

### 4. Machine Learning Models

Developed and compared the following regression models:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- XGBoost Regressor

Also evaluated a weighted ensemble combining XGBoost and Random Forest.

### 5. Additional Analyses

- Monthly and yearly temperature analysis.
- Feature importance using XGBoost.
- Permutation importance analysis.
- Geographical temperature visualization.
- Comparison of temperature patterns across countries.

### 6. Model Improvement

Improved the XGBoost model through:

- Cyclical time features to represent recurring seasonal patterns.
- Hyperparameter tuning to identify better model configurations.
- Regularization to help control model complexity.

### 7. Model Validation

Used chronological train-test evaluation and TimeSeriesSplit cross-validation to assess model performance across different time periods.

This approach helps evaluate how well the model performs on later observations rather than relying only on random data splitting.

## Model Performance

The improved XGBoost model achieved the following results on the chronological test set:

| Metric | Improved XGBoost |
|---|---:|
| MAE | 2.4062°C |
| RMSE | 3.2484°C |
| R² Score | 0.8038 |

The original XGBoost model achieved an R² score of **0.7505**, while the improved model achieved **0.8038**.

This represents an improvement in the model's ability to explain temperature variation on the test set.

## Saved Models

The trained models and their corresponding feature lists are saved in the `models/` directory:

- `xgboost_weather_model.pkl` – Original trained XGBoost model.
- `weather_features.pkl` – Feature list used by the original model.
- `improved_xgboost_weather_model.pkl` – Improved and tuned XGBoost model.
- `improved_weather_features.pkl` – Feature list used by the improved model.

The models are saved using Joblib for future loading and prediction without retraining.

## Project Structure

```text
Weather-Trend-Forecasting/
│
├── data/
│   └── GlobalWeatherRepository.csv
│
├── notebooks/
│   └── implementation_final.ipynb
│
├── models/
│   ├── xgboost_weather_model.pkl
│   ├── weather_features.pkl
│   ├── improved_xgboost_weather_model.pkl
│   └── improved_weather_features.pkl
│
├── outputs/
├── reports/
│
├── requirements.txt
├── README.md
└── .gitignore
```

## Installation and Usage

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

### 2. Navigate to the project directory

```bash
cd Weather-Trend-Forecasting
```

### 3. Install the required dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook notebooks/notebook.ipynb
```

### 5. Run the notebook

Execute the notebook cells in sequence to reproduce the data preprocessing, analysis, model training, evaluation, and model improvement workflow.

**Note:** Ensure the dataset is placed inside the `data/` directory before running the notebook.

## Future Improvements

- Include additional weather variables such as humidity, rainfall, and wind speed.
- Explore advanced time-series forecasting techniques.
- Improve geographical data standardization.
- Deploy the trained model through a web application.
- Evaluate model performance on newer and independent weather observations.

## Conclusion

This project demonstrates an end-to-end machine learning workflow for global temperature analysis, covering data preprocessing, exploratory analysis, anomaly detection, geographical comparisons, model development, and performance improvement.

Among the evaluated models, the improved XGBoost model achieved an **MAE of 2.4062°C, RMSE of 3.2484°C, and R² score of 0.8038** on the chronological test set, compared with an original XGBoost R² score of 0.7505.

The results demonstrate that feature engineering, hyperparameter tuning, and regularization improved the model's predictive performance on the evaluated test data.
