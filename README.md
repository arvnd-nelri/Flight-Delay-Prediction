# Flight Departure Delay Prediction

This project aims to predict flight departure delays using machine learning models. The dataset used for this project is available on Kaggle: [Flight Delays Dataset](https://www.kaggle.com/datasets/usdot/flight-delays/data). We use multiple machine learning algorithms to predict the departure delay and evaluate their performance.

## Data Preprocessing

The data preprocessing steps include:

- **Selecting Relevant Columns**: 
  We retain only the columns that are useful for predicting the departure delay (`DEPARTURE_DELAY`), including features like `MONTH`, `DAY`, `DAY_OF_WEEK`, `AIRLINE`, etc.

- **Merging Airport Data**: 
  We ensure that the `ORIGIN_AIRPORT` and `DESTINATION_AIRPORT` are valid airport codes, replacing unknown codes with `"OTHER"`.

- **Handling Missing Values**: 
  Rows with missing values are dropped from the dataset to avoid issues during model training.

- **Encoding Categorical Variables**: 
  Categorical variables such as `AIRLINE`, `ORIGIN_AIRPORT`, `DESTINATION_AIRPORT`, and `DAY_OF_WEEK` are one-hot encoded. One-hot encoding creates binary columns for each category in the categorical variables.

- **Feature Engineering**: 
  The dataset is prepared by combining the encoded categorical columns with the numeric features. Then, a random sample of 60,000 rows is selected for model training.

## Modeling

The following machine learning models are used for prediction:

- **Random Forest Regressor**
- **Decision Tree Regressor**
- **Gradient Boosting Regressor**

Each model is trained on 70% of the data, with the remaining 30% used for testing.

## Model Evaluation

The models are evaluated using the following metrics:

- **RMSE (Root Mean Squared Error)**: 
  Measures the difference between the predicted and actual values. Lower values indicate better performance.

- **R-squared**: 
  Represents how well the model explains the variance in the target variable. Higher values indicate better model performance.
