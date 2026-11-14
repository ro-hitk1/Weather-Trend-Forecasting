# Weather Trend Forecasting

A data science and machine learning project focused on exploring global weather patterns, identifying trends and anomalies, and forecasting weather conditions using historical weather data.

## Project Overview

Weather patterns are influenced by multiple atmospheric and environmental factors. This project uses historical weather data to perform exploratory data analysis, detect unusual weather patterns, study climate trends, and build machine learning models for weather forecasting.

The project combines data preprocessing, statistical analysis, visualization, and predictive modelling in Python.

## Objectives

- Explore and understand global weather data.
- Identify weather trends and seasonal patterns.
- Detect anomalies in weather observations.
- Compare different forecasting and machine learning models.
- Analyse weather variations across countries and continents.
- Investigate relationships between weather variables and environmental factors.
- Evaluate model performance using appropriate regression metrics.
=======
This project focuses on analyzing global weather data, identifying temperature patterns, and developing machine learning models to predict temperature based on geographical and time-related features.

It covers an end-to-end machine learning workflow, including data cleaning, exploratory data analysis, anomaly detection, geographical analysis, feature importance, model comparison, hyperparameter tuning, and model validation.

## Dataset

**Dataset:** `GlobalWeatherRepository.csv`

The dataset contains global weather observations with 128,638 records and 41 columns.

It includes weather-related information such as:
- Temperature
- Humidity
- Wind speed and direction
- Atmospheric pressure
- Precipitation
- Cloud cover
- Visibility
- Geographic information
- Date and time information

The dataset covers the period from **16 May 2024 to 10 March 2026**.
=======
The dataset contains geographical information, timestamps, temperature readings, and other weather-related variables.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation |
| NumPy | Numerical computations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine learning and evaluation |
| XGBoost | Gradient boosting |
| Statsmodels | Time-series analysis |
| Jupyter Notebook | Project development |

## Project Workflow

### 1. Data Collection and Preprocessing
- Load the weather dataset.
- Inspect the dataset structure and data types.
- Handle missing values and duplicate records where applicable.
- Convert date columns into appropriate datetime formats.
- Prepare relevant features for analysis and modelling.

### 2. Exploratory Data Analysis (EDA)
- Analyse temperature and other weather variables.
- Explore distributions and correlations.
- Compare weather patterns across locations.
- Visualize temporal and geographical variations.

### 3. Weather Trend Analysis
- Examine changes in weather variables over time.
- Investigate seasonal and temporal patterns.
- Compare weather conditions across countries and continents.

### 4. Anomaly Detection
- Identify unusual weather observations.
- Examine extreme values and deviations from typical patterns.

### 5. Weather Forecasting
The project explores multiple forecasting approaches:

=======
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
- Random Forest
- XGBoost
- ARIMA
- Exponential Smoothing
- Ridge Regression–XGBoost Ensemble

Models are evaluated using a common test period to make their performance more comparable.

### 6. Model Evaluation

The following metrics are used:

- **MAE (Mean Absolute Error):** Measures average absolute prediction error.
- **RMSE (Root Mean Squared Error):** Penalizes larger prediction errors.
- **R² Score:** Measures the proportion of variance explained by the model.
=======
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

### 7. Feature and Spatial Analysis
- Examine the importance of weather-related features.
- Investigate geographical differences in weather patterns.
- Compare weather conditions across regions.

## Model Results

The Ridge Regression–XGBoost ensemble achieved the following reported results on the common test period:

| Metric | Improved XGBoost |
|---|---:|
| MAE | 2.476 |
| RMSE | 3.225 |
| R² Score | 0.152 |

These results indicate that the ensemble performed better than the previously evaluated Random Forest model. However, the R² score indicates that the model explains only a limited proportion of the variation in the target variable. Therefore, its forecasting performance should be interpreted cautiously.

*Note: The reported error units depend on the target variable and its measurement scale.*
=======
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

├── GlobalWeatherRepository(1).csv
│   └── Weather dataset
=======
├── notebooks/
│   └── implementation_final.ipynb
>>>>>>> 3c2a5752b4d65a2a6772d146590bedb29b667277
│
├── models/
│   └── Saved forecasting models
│
├── README.md
│
└── requirements.txt
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Weather-Trend-Forecasting.git
```

### 2. Navigate to the project directory

```bash
cd Weather-Trend-Forecasting
```

<<<<<<< HEAD
### 3. Create a virtual environment (optional)

```bash
python -m venv venv
```

Activate it:

**Windows**
```bash
venv\Scripts\activate
```

**macOS / Linux**
```bash
source venv/bin/activate
```

### 4. Install dependencies
=======
### 3. Install the required dependencies
>>>>>>> 3c2a5752b4d65a2a6772d146590bedb29b667277

```bash
pip install -r requirements.txt
```

<<<<<<< HEAD
### 5. Run the notebook
=======
### 4. Launch Jupyter Notebook
>>>>>>> 3c2a5752b4d65a2a6772d146590bedb29b667277

```bash
jupyter notebook implementation.ipynb
```

<<<<<<< HEAD
You can also open the notebook directly in Visual Studio Code with the Jupyter extension installed.
=======
### 5. Run the notebook

Execute the notebook cells in sequence to reproduce the data preprocessing, analysis, model training, evaluation, and model improvement workflow.
>>>>>>> 3c2a5752b4d65a2a6772d146590bedb29b667277

## Requirements

<<<<<<< HEAD
Create a `requirements.txt` file containing the libraries used by the notebook:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
statsmodels
jupyter
joblib
```

## Limitations

- The dataset covers a relatively limited historical period for long-term climate analysis.
- Weather observations may contain noise and location-specific variations.
- Forecasting accuracy depends on data quality, feature selection, and the prediction horizon.
- A positive but relatively low R² score suggests that further model improvements are needed.
- Short-term weather forecasting results should not be interpreted as long-term climate predictions.

## Future Improvements

- Incorporate longer historical weather records.
- Include additional atmospheric and environmental variables.
- Explore advanced time-series and deep learning models such as LSTM.
- Improve feature engineering and hyperparameter tuning.
- Evaluate performance across multiple locations.
- Develop an interactive weather forecasting dashboard.
=======
## Future Improvements

- Include additional weather variables such as humidity, rainfall, and wind speed.
- Explore advanced time-series forecasting techniques.
- Improve geographical data standardization.
- Deploy the trained model through a web application.
- Evaluate model performance on newer and independent weather observations.
>>>>>>> 3c2a5752b4d65a2a6772d146590bedb29b667277

## Author

**Rohit Kumar**

## License

This project is intended for educational and research purposes. Add a license such as MIT if you want others to reuse and modify the project under its terms.
=======
This project demonstrates an end-to-end machine learning workflow for global temperature analysis, covering data preprocessing, exploratory analysis, anomaly detection, geographical comparisons, model development, and performance improvement.

Among the evaluated models, the improved XGBoost model achieved an **MAE of 2.4062°C, RMSE of 3.2484°C, and R² score of 0.8038** on the chronological test set, compared with an original XGBoost R² score of 0.7505.

The results demonstrate that feature engineering, hyperparameter tuning, and regularization improved the model's predictive performance on the evaluated test data.
