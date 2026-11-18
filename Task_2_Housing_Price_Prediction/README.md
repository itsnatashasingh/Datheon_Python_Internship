# California Housing Price Prediction

## Project Overview

This project focuses on predicting median house values in California using supervised machine learning regression techniques.

Completed as **Task 2 – Real Estate Housing Price Prediction (Ridge & Lasso Regression)** under the Datheon Machine Learning & Data Science Internship, the project explores housing data, performs feature engineering and preprocessing, develops regression models, and evaluates their predictive performance.

The primary objective is to build and compare Ordinary Least Squares (OLS), Ridge Regression, and Lasso Regression models to understand their effectiveness in predicting median house values.

## Objectives

- Perform exploratory data analysis to understand housing characteristics and relationships between variables.
- Identify and handle missing values and examine data quality.
- Perform feature engineering to create meaningful numerical features.
- Analyze multicollinearity using Variance Inflation Factor (VIF).
- Apply feature scaling and categorical encoding.
- Develop and optimize multiple regression models.
- Evaluate model performance using appropriate regression metrics.
- Perform residual analysis to understand prediction errors.

## Dataset Description

The project uses the California Housing dataset, containing **20,640 observations and 10 original columns**.

The dataset includes geographical information, housing characteristics, demographic information, median income, and ocean proximity.

### Features

| Feature | Description |
|---|---|
| longitude | Longitude of the geographical location |
| latitude | Latitude of the geographical location |
| housing_median_age | Median age of houses in the block |
| total_rooms | Total number of rooms |
| total_bedrooms | Total number of bedrooms |
| population | Population of the block |
| households | Number of households |
| median_income | Median household income |
| ocean_proximity | Proximity to the ocean |

**Target Variable:** `median_house_value`

The target represents the median house value for each geographical block.

## Technologies and Libraries

- **Programming Language:** Python
- **Environment:** Jupyter Notebook
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Statistical Analysis:** Statsmodels

## Project Workflow

The project is organized into eight major parts.

### Part 1 – Dataset Loading and Initial Inspection

- Loaded the California Housing dataset.
- Examined dataset dimensions, columns, and data types.
- Inspected initial records and statistical summaries.

### Part 2 – Exploratory Data Analysis

- Analyzed numerical and categorical variables.
- Examined distributions and relationships between features.
- Used visualizations to understand housing characteristics and geographical patterns.

### Part 3 – Data Cleaning and Preprocessing

- Identified and handled missing values.
- Examined duplicate records.
- Prepared the dataset for further analysis.

### Part 4 – Exploratory Analysis and Feature Relationships

- Investigated relationships between independent variables and the target variable.
- Examined correlations and patterns in housing data.
- Identified potential relationships relevant to house value prediction.

### Part 5 – Feature Engineering and Multicollinearity Analysis

Created the following engineered features:

- `rooms_per_household`
- `bedrooms_per_room`
- `population_per_household`
- `income_x_house_age`

Performed Variance Inflation Factor (VIF) analysis to examine multicollinearity among numerical features.

### Part 6 – Feature Scaling and Encoding

- Applied StandardScaler to numerical features.
- Applied OneHotEncoder to the categorical `ocean_proximity` feature.
- Used ColumnTransformer to combine preprocessing operations.
- Prepared 17 transformed features for regression modeling.

### Part 7 – Regression Model Development

Developed and compared three regression algorithms:

1. **Ordinary Least Squares (OLS):** Used as the baseline linear regression model.
2. **Ridge Regression:** Applied L2 regularization to control coefficient magnitudes.
3. **Lasso Regression:** Applied L1 regularization to encourage sparse coefficients.

Used GridSearchCV with 5-fold cross-validation to optimize the regularization parameter (`alpha`) for Ridge and Lasso regression.

The models were implemented using Scikit-learn Pipelines to ensure that preprocessing was performed within each cross-validation fold and to prevent data leakage.

### Part 8 – Residual Error Analysis

Performed residual analysis to examine model prediction errors.

The analysis included:

- Generating predictions for the test dataset.
- Calculating residual errors.
- Actual vs Predicted visualizations.
- Residual distribution analysis.
- Residuals vs Predicted visualizations.
- Calculation of residual statistics.
- Comparison of prediction bias and error variability.

## Model Evaluation

The dataset was divided into training and testing sets using an 80:20 split.

| Dataset | Observations |
|---|---:|
| Training | 16,512 |
| Testing | 4,128 |

The models were evaluated using the following metrics:

- **RMSE (Root Mean Squared Error):** Measures the magnitude of prediction errors, penalizing larger errors more heavily.
- **MAE (Mean Absolute Error):** Measures the average absolute prediction error.
- **R² Score:** Measures the proportion of variance in the target variable explained by the model.

### Test Set Performance

| Model | RMSE | MAE | R² Score |
|---|---:|---:|---:|
| OLS | 72,838.3183 | 50,613.0149 | 0.5951 |
| Ridge | 72,847.9561 | 50,621.6349 | 0.5950 |
| Lasso | 72,839.9701 | 50,616.2072 | 0.5951 |

### Hyperparameter Tuning Results

| Model | Best Alpha | Cross-Validation RMSE |
|---|---:|---:|
| Ridge | 1.0 | 67,720.72 |
| Lasso | 3.1623 | 67,721.32 |

## Key Findings

- All three regression models achieved similar predictive performance.
- OLS obtained the lowest test RMSE and MAE among the evaluated models.
- Ridge and Lasso regularization did not provide a substantial improvement over the baseline OLS model.
- All models achieved an R² score of approximately 0.595, explaining around 59.5% of the variation in median house values.
- Residual analysis indicated slightly negative mean residuals across all three models, suggesting a small average tendency toward overprediction.
- The models also produced some large individual prediction errors, highlighting opportunities for further improvement.

## Conclusion

This project provided practical experience in developing a complete regression workflow, including exploratory data analysis, data cleaning, feature engineering, multicollinearity analysis, feature preprocessing, model development, hyperparameter tuning, and residual analysis.

Among the three evaluated models, OLS achieved marginally better performance on the test dataset. However, the differences between OLS, Ridge, and Lasso were negligible.

The results demonstrate that regularization did not substantially improve the predictive performance of the selected linear regression models on this dataset.

Further improvements could explore non-linear regression techniques, additional feature engineering, and more advanced modeling approaches.

## Limitations

- Linear regression models may not fully capture complex non-linear relationships in housing data.
- The dataset contains substantial variation in housing values, resulting in some large prediction errors.
- The `median_house_value` target variable is capped at $500,001, which limits the representation of higher-value properties.
- The evaluated models explain approximately 59.5% of the variation in the target variable.

## Repository Contents

The project folder contains the Jupyter Notebook used for data exploration, preprocessing, model development, evaluation, and residual analysis.

## How to Run the Project

1. Clone or download the repository.
2. Navigate to the Task 2 project folder.
3. Install the required Python libraries.
4. Open the Jupyter Notebook.
5. Execute the notebook cells sequentially.

### Installation

```bash
pip install numpy pandas matplotlib seaborn scikit-learn statsmodels jupyter
```

## Internship Information

**Program:** Datheon Machine Learning & Data Science Internship

**Project:** Task 2 – Real Estate Housing Price Prediction (Ridge & Lasso Regression)

**Focus Area:** Machine Learning and Regression Analysis

---

*This project was developed as part of the Datheon Machine Learning & Data Science Internship to gain practical experience in regression modeling, feature engineering, model evaluation, and error analysis.*