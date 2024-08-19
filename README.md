# Problem Definition

The goal of this project is to predict electric power consumption for various countries using a regression-based approach. The dataset consists of columns representing country names and years from 1981 onwards, with each cell containing the energy consumption value for a specific country and year.

The main objectives of this project are:
1. Data Preprocessing:
   - Filter out countries with less than 6 rows of data.
   - Ensure the first row for each country is not before 2005.
   - Transform the dataset by converting year columns into rows.
   - Remove data points after 2014 as they are not relevant for the prediction task. 

2. Feature Engineering:
   - Extract relevant features from the preprocessed dataset, such as year and country-specific features.
   - Create a feature matrix by combining the extracted features.

3. Regression Modeling:
   - Train and select the best-performing regression algorithm using the feature matrix and target variable.
   - Evaluate the selected model's performance using appropriate metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared ($R^2$). 
   - Fine-tune the selected model's hyperparameters to optimize its performance.

4. Prediction:
   - Make predictions on the test set or future years using the trained regression model.

## Mathematical Notation

Let the raw dataset be represented as a matrix $D$, where each row corresponds to a country and each column represents a year. The element $d_{ij}$ denotes the energy consumption for country $i$ in year $j$.

After data preprocessing, let the transformed dataset be represented as $X$, where each row corresponds to a year and each column represents a country.

The feature matrix $F$ is created by combining the extracted features:
$F = [x_1, x_2, \ldots, x_n]$

The target variable (energy consumption) is denoted as $y$.

The trained regression model is denoted as $f(x)$, which takes the feature vector $x$ as input and predicts the energy consumption $\hat{y}$.

For a given country $c$ and year $t$, the energy consumption prediction can be obtained as:

$\hat{y}_{c,t} = f(x_{c,t})$

where $x_{c,t}$ represents the feature vector for country $c$ in year $t$. 

## Tools

The following tools and libraries will be used in this project:

1. Pandas: A powerful data manipulation library for data preprocessing and feature engineering.

2. PyCaret: An open-source, low-code machine learning library in Python that automates machine learning workflows, including model training, selection, and evaluation. 

3. Docker: A containerization platform that provides a consistent and reproducible environment for running the project.

4. Streamlit: An open-source app framework for building interactive web applications, which will be used to create a user-friendly interface for the energy consumption prediction project.
