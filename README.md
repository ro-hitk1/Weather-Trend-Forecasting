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

## Dataset

**Dataset:** `GlobalWeatherRepository(1).csv`

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

### 7. Feature and Spatial Analysis
- Examine the importance of weather-related features.
- Investigate geographical differences in weather patterns.
- Compare weather conditions across regions.

## Model Results

The Ridge Regression–XGBoost ensemble achieved the following reported results on the common test period:

| Metric | Result |
|---|---:|
| MAE | 2.476 |
| RMSE | 3.225 |
| R² Score | 0.152 |

These results indicate that the ensemble performed better than the previously evaluated Random Forest model. However, the R² score indicates that the model explains only a limited proportion of the variation in the target variable. Therefore, its forecasting performance should be interpreted cautiously.

*Note: The reported error units depend on the target variable and its measurement scale.*

## Project Structure

```text
Weather-Trend-Forecasting/
│
├── implementation.ipynb
│   └── Main project notebook
│
├── GlobalWeatherRepository(1).csv
│   └── Weather dataset
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

```bash
pip install -r requirements.txt
```

### 5. Run the notebook

```bash
jupyter notebook implementation.ipynb
```

You can also open the notebook directly in Visual Studio Code with the Jupyter extension installed.

## Requirements

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

## Author

**Your Name**

GitHub: [YOUR-GITHUB-PROFILE](https://github.com/YOUR-USERNAME)

## License

This project is intended for educational and research purposes. Add a license such as MIT if you want others to reuse and modify the project under its terms.
