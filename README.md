# Weather Trend Forecasting

## Project Overview

This project focuses on analyzing global weather data, identifying temperature patterns, and building machine learning models to estimate temperature based on geographical and time-related features.

The project includes data cleaning, exploratory data analysis, anomaly detection, geographical analysis, feature importance, model comparison, and model improvement.

## Dataset

- **Dataset:** Global Weather Repository
- **Records:** 170,927
- **Country-name entries:** 211
- **Date range:** May 2024 – October 2026
- **Target variable:** Temperature (°C)

The dataset contains geographical information, timestamps, and temperature readings.

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

### 2. Exploratory Data Analysis
- Analyzed temperature distributions.
- Studied daily temperature trends.
- Visualized weather condition frequencies.
- Examined correlations between numerical features.

### 3. Anomaly Detection
- Used Isolation Forest to identify unusual temperature observations.
- Visualized normal and anomalous records.
- Examined extreme temperature readings.

### 4. Machine Learning Models
Built and compared the following models:
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- XGBoost Regressor

Also evaluated a weighted ensemble of XGBoost and Random Forest.

### 5. Unique Analyses
- Monthly and yearly temperature analysis.
- Feature importance using XGBoost.
- Permutation importance analysis.
- Geographical temperature visualization.
- Comparison of temperature patterns across countries.

### 6. Model Improvement
Improved the XGBoost model using cyclical time features, hyperparameter tuning, and regularization.

### 7. Model Validation
Used TimeSeriesSplit cross-validation to evaluate model performance across different time periods.

## Model Performance

The improved XGBoost model achieved the following results on the chronological test set:

| Metric | Result |
|---|---:|
| MAE | 2.4062°C |
| RMSE | 3.2484°C |
| R² Score | 0.8038 |

The improved model performed better than the original XGBoost model, which achieved an R² score of 0.7505.

## Saved Models

The trained models and their feature lists are saved in the `models/` directory:

- `xgboost_weather_model.pkl`
- `weather_features.pkl`
- `improved_xgboost_weather_model.pkl`
- `improved_weather_features.pkl`

## Project Structure

```text
Weather-Trend-Forecasting/
│
├── data/
│   └── GlobalWeatherRepository.csv
│
├── notebooks/
│   └── notebook.ipynb
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

1. Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

2. Navigate to the project directory:

```bash
cd Weather-Trend-Forecasting
```

3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook:

```bash
jupyter notebook notebooks/notebook.ipynb
```

5. Run the notebook cells in sequence to reproduce the analysis and model development.

**Note:** Ensure the dataset is placed inside the `data/` directory before running the notebook.



## Future Improvements

- Include additional weather variables such as humidity, rainfall, and wind speed.
- Apply advanced time-series forecasting techniques.
- Improve geographical data standardization.
- Deploy the model through a web application.

## Conclusion

This project demonstrates an end-to-end machine learning workflow for global temperature analysis, from data preprocessing and exploratory analysis to model development, evaluation, and improvement. The improved XGBoost model achieved an R² score of 0.8038 on the test set.
