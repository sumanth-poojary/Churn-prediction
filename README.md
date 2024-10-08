# Customer Churn Prediction

This project aims to predict customer churn based on historical customer data. It uses various feature engineering techniques and a `RandomForestClassifier` to classify customers who are likely to churn. This project was guided work, which I completed through forage virtual intership.

## Project Overview

Customer churn is when a customer stops doing business with a company. Predicting customer churn helps businesses take preventive measures and retain customers, which can be more cost-effective than acquiring new ones. In this project, a machine learning model was built to predict whether a customer will churn or not based on their attributes.

## Project Steps:

1. **Data Loading**:
    - Data is loaded from `clean_data_after_eda.csv`, which contains various customer features and churn labels.

2. **Data Preprocessing**:
    - Date columns like `date_activ`, `date_end`, `date_modif_prod`, and `date_renewal` are converted to a datetime format.
    - Feature engineering is performed to derive additional useful features like price differences and total consumption.
    
3. **Feature Engineering**:
    - A feature to measure the difference between December and January off-peak prices.
    - Features like total consumption, contract duration, and gas usage (`has_gas`) were created.
    - Categorical variables were handled using encoding techniques (Label Encoding, One-Hot Encoding).
    
4. **Model Training**:
    - A `RandomForestClassifier` was trained on 70% of the data, and predictions were made on the remaining 30%.
    - Feature selection was performed by removing irrelevant date columns.

5. **Model Evaluation**:
    - Accuracy score and classification report were generated to evaluate the model performance.

## Key Features:

- **Random Forest Classifier**: A powerful ensemble learning algorithm used for classification.
- **Feature Engineering**: Various new features created from the existing data to improve the model's performance.
- **Data Preprocessing**: Handled missing values, date-time formatting, and categorical variables.

## Technologies Used:

- **Programming Language**: Python
- **Libraries**: 
    - `Pandas` for data manipulation
    - `Scikit-learn` for machine learning modeling
    - `Matplotlib` and `Seaborn` for data visualization
- **Machine Learning Algorithm**: `RandomForestClassifier`

## How to Use

1. Clone this repository:
    ```bash
    git clone https://github.com/sumanth-poojary/customer-churn-prediction.git
    ```
2. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the project code:
    ```bash
    python churn_prediction.py
    ```

## Results

- **Accuracy**: Achieved an accuracy of around 90% on the test data.
- **Classification Report**: The model outputs precision, recall, and F1-scores to assess the performance across various classes.

## Future Work

- Improve the model using hyperparameter tuning.
- Experiment with other machine learning algorithms like XGBoost or Logistic Regression.
