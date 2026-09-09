MajorFit – Academic Major Suitability Prediction

Project Overview

MajorFit is a machine learning project that predicts whether a student’s academic major is suitable for their personality traits, academic preferences, and career alignment.

The project aims to support students in making more informed decisions about their academic major by analyzing different personality and academic-related factors.

Problem Statement

Students may choose academic majors without considering whether the major matches their personality, interests, learning preferences, and career goals. This can lead to low academic satisfaction and uncertainty about their future career.

MajorFit addresses this problem by using machine learning classification models to predict major suitability.

Dataset

The dataset contains questionnaire responses related to students’ academic and personality characteristics.

The features include:

* Major Field
* Academic Year
* Personality Type
* Work Preference
* Problem-Solving Style
* Learning Method
* Major Interest
* Academic Performance
* Major Choice
* Career Alignment

The target variable represents major suitability:

* 0 – Suitable
* 1 – Neutral
* 2 – Not Suitable

Data Preprocessing

The dataset was prepared before model training by:

* Checking for missing values
* Filling missing values using the mode when necessary
* Removing duplicate records
* Checking data types
* Separating the input features from the target variable
* Splitting the data into 80% training and 20% testing sets using stratified sampling

Methodology

The project followed a machine learning workflow that included:

1. Data Understanding
2. Data Preparation
3. Exploratory Data Analysis
4. Model Training
5. Model Evaluation
6. Hyperparameter Tuning
7. Prediction and Deployment

Machine Learning Models

Three classification models were implemented:

Logistic Regression

Used as a baseline classification model.

Decision Tree

Used to capture non-linear relationships between the input features and the target variable.

Random Forest

Used as an ensemble model to improve prediction performance and reduce overfitting.

Model Evaluation

The models were evaluated using classification accuracy before and after hyperparameter tuning.

Model	Before Tuning	After Tuning
Logistic Regression	65.3%	65.3%
Random Forest	59.7%	59.7%
Decision Tree	44.4%	65.3%

Hyperparameter Tuning

GridSearchCV with 5-fold cross-validation was used to identify the best hyperparameters for each model.

Best Parameters:

* Logistic Regression: C = 10
* Random Forest: criterion = gini, max_depth = 5, n_estimators = 200
* Decision Tree: criterion = gini, max_depth = 3

The Decision Tree showed the largest improvement after tuning, increasing its accuracy from 44.4% to 65.3%.

Results

After hyperparameter tuning, Logistic Regression and Decision Tree achieved the highest test accuracy of 65.3%.

The results show that hyperparameter tuning improved the performance of the Decision Tree significantly.


Deployment

The trained model was integrated into a Streamlit web application that allows users to enter their characteristics and receive a predicted major suitability result.

Application: https://majorfit-app.streamlit.app/

Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Streamlit
* Jupyter Notebook
* GridSearchCV

Future Improvements

Future work could include:

* Collecting a larger and more diverse dataset
* Adding more personality and behavioral features
* Testing additional machine learning algorithms
* Improving model performance through further feature engineering and tuning
* Enhancing the deployed application
