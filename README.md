MajorFit: Predicting Students’ Academic Major Suitability Based on Personality Traits

Project Overview

MajorFit is a machine learning project that predicts whether an academic major is suitable for a student based on personality traits, learning preferences, problem-solving style, academic performance, major interest, and career alignment.

The project aims to support students in making more informed academic major decisions by analyzing the relationship between students’ characteristics and their selected major.

Problem Statement

Students may choose academic majors without considering whether the major aligns with their personality, interests, learning preferences, and career goals. This may lead to low academic satisfaction, reduced performance, and uncertainty about future career paths.

This project addresses this problem by developing machine learning classification models to predict academic major suitability.

Dataset

The dataset was collected through an online questionnaire. The data is numerically encoded and contains information related to students’ academic and personality characteristics.

The dataset includes the following features:

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
* Target

The target variable represents the suitability classification.

Data Preprocessing

The following preprocessing steps were applied:

* Loaded the dataset using Pandas.
* Checked for missing values.
* Filled missing values using the mode when necessary.
* Removed duplicate records.
* Checked the data types.
* Separated the input features from the target variable.

The dataset was already numerically encoded before model training.

Methodology

The machine learning workflow includes:

1. Data Preprocessing
2. Train-Test Split
3. Model Training
4. Model Evaluation
5. Hyperparameter Tuning
6. Model Comparison

The dataset was divided into training and testing sets using an 80/20 split with stratification.

Machine Learning Models

Three classification algorithms were implemented:

Logistic Regression

Used as a baseline classification model.

Decision Tree

Used to model decision rules and capture non-linear relationships between the input features and the target.

Random Forest

Used as an ensemble classification model based on multiple decision trees.

Model Evaluation

The models were evaluated using classification performance metrics, including:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Hyperparameter Tuning

GridSearchCV with 5-fold cross-validation was used to search for suitable hyperparameter combinations for each model.

The best parameters identified by the notebook were:

Model	Best Parameters
Logistic Regression	C = 10
Random Forest	n_estimators = 200, max_depth = 5, criterion = gini
Decision Tree	max_depth = 3, criterion = gini

Results

The accuracy results recorded in the notebook are:

Model	Accuracy Before Tuning	Accuracy After Tuning
Logistic Regression	0.653	0.653
Random Forest	0.597	0.597
Decision Tree	0.444	0.653

Based on the recorded test accuracy after tuning, Logistic Regression and Decision Tree achieved the highest accuracy at approximately 65.3%.

The Decision Tree showed the largest improvement after hyperparameter tuning.

Deployment

The project was developed as a machine learning application for predicting academic major suitability.

Application:

https://majorfit-app.streamlit.app/

Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Streamlit
* Jupyter Notebook

Project Files

* MajorFit (1).csv — Dataset used for the project
* MajorFit_ML.ipynb — Jupyter Notebook containing data preprocessing, model training, evaluation, and hyperparameter tuning
* projectML_converted.html — HTML export of the Jupyter Notebook
* requirements.txt — Python dependencies required for the project

Future Improvements

Future improvements could include:

* Collecting a larger dataset.
* Adding more personality and behavioral features.
* Testing additional machine learning algorithms.
* Improving feature engineering and model optimization.
* Further improving the deployed application.
