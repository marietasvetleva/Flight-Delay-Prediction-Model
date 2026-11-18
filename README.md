
# Flight Delay Prediction — Machine Learning

A machine learning project focused on predicting flight delays using historical flight data from the Bureau of Transportation Statistics (BTS).

The project explores flight delay patterns, develops classification models and evaluates how different preprocessing and class-balancing techniques influence prediction performance.

## Project Overview

Flight delays affect passengers, airlines and airport operations. Factors such as weather, congestion, airline operations and departure schedules can influence whether a flight experiences a delay.

The goal of this project was to develop and evaluate machine learning models capable of classifying flights as delayed or on time, while investigating the challenges of working with imbalanced datasets.

The project followed the AMD methodology, covering domain understanding, data preparation, model development, evaluation and recommendations.

## Project Objectives

- Investigate factors associated with flight delays.
- Explore and prepare historical flight data for machine learning.
- Develop and evaluate classification models.
- Investigate the impact of class imbalance on prediction performance.
- Experiment with feature selection and data-balancing techniques.
- Compare model performance using multiple evaluation metrics.
- Identify limitations and recommend future improvements.

## Dataset

**Source:** Bureau of Transportation Statistics (BTS)

The project uses historical flight and operational data to investigate flight delay prediction.

Data preparation included:

- Exploring missing values, data types and feature distributions.
- Selecting relevant numerical and categorical features.
- Converting scheduled departure and arrival times into separate hour and minute features.
- Applying one-hot encoding to categorical variables.
- Separating the target variable from the input features.
- Preparing training and testing datasets.
- Experimenting with an 80/20 stratified train-test split.

The dataset contained substantially more on-time flights than delayed flights, creating a class imbalance that influenced model performance.

## Machine Learning Models

### 1. k-Nearest Neighbors (k-NN)

The first model was developed using the k-Nearest Neighbors algorithm as an initial baseline.

The model was evaluated using classification metrics and a confusion matrix.

**Results:**
- Accuracy: 83.66%
- Recall for delayed flights: 10.39%

Although the model achieved relatively high accuracy, it identified only a small proportion of delayed flights.

This demonstrated that accuracy alone was not a sufficient measure of performance for this classification problem.

### 2. Random Forest — Baseline

Random Forest was selected as an alternative classification algorithm to investigate whether a tree-based approach could better identify delayed flights.

The baseline model achieved:

- Accuracy: approximately 81%
- Recall for delayed flights: approximately 15%

Despite its reasonable overall accuracy, the model still struggled to identify the minority class.

### 3. Random Forest — Class Balancing

A second Random Forest model was trained to investigate whether class balancing could improve delayed-flight predictions.

The balanced model did not improve recall compared with the baseline.

This experiment demonstrated that class balancing does not automatically improve model performance.

### 4. Random Forest — Random Undersampling

To address class imbalance, Random Undersampling was applied to the training dataset by reducing the number of on-time flight observations.

The original class distribution was preserved in the test dataset to evaluate performance under more realistic conditions.

This approach increased recall for delayed flights from approximately 15% to 64%.

However, the improvement came with lower precision and overall accuracy, as the model incorrectly classified more on-time flights as delayed.

### 5. Random Forest — Feature Selection & Undersampling

Feature importance was investigated to identify the most relevant predictors.

The number of features was reduced from 699 to 200, and the models were evaluated with and without undersampling.

The combination of **200 selected features and Random Undersampling** achieved the strongest delayed-flight recall and F1-score among the Random Forest experiments.

**Results:**
- Recall for delayed flights: 65.16%
- Precision for delayed flights: 29.08%
- F1-score for delayed flights: 40.22%

These results demonstrate the trade-off between identifying more delayed flights and producing more false-positive predictions.

## Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices
- Classification reports

Particular attention was given to **recall for delayed flights**, as identifying actual delays was an important objective of the project.

### Key Findings

1. **High accuracy does not guarantee effective delay prediction.** Models could achieve over 80% accuracy while missing most delayed flights.

2. **Class imbalance strongly influenced performance.** Models tended to favour the majority class of on-time flights.

3. **Random Undersampling improved recall.** However, reducing the majority class also removed training data and increased false-positive predictions.

4. **Feature selection influenced model performance.** Reducing the number of features provided another approach to investigate model improvement.

5. **Model comparisons require consistent evaluation conditions.** The k-NN and Random Forest experiments used different test samples, so their results are not directly comparable under identical conditions.

## Technologies Used

- **Python** — Machine learning development
- **Jupyter Notebook** — Data exploration and experimentation
- **Pandas** — Data manipulation and preprocessing
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualisation
- **Scikit-learn** — Classification models, preprocessing and evaluation

## Development Process

The project followed an iterative machine learning workflow:

1. **Domain Understanding:** Researched flight delays, their causes and their operational impact.
2. **Data Understanding:** Explored the BTS dataset, investigated variables and assessed data quality.
3. **Data Preparation:** Cleaned and transformed the dataset, encoded categorical variables and prepared training and testing data.
4. **Initial Modelling:** Developed and evaluated a k-NN classification model.
5. **Algorithm Selection:** Investigated Random Forest as an alternative approach.
6. **Model Improvement:** Experimented with class balancing, Random Undersampling and feature selection.
7. **Evaluation:** Compared classification metrics and analysed the strengths and limitations of each approach.
8. **Recommendations:** Identified possible improvements and assessed whether the model was suitable for practical use.

## Limitations

The project identified several limitations:

- The dataset was imbalanced, with substantially fewer delayed flights.
- Improving recall through undersampling reduced precision.
- Undersampling removed potentially useful training observations.
- k-NN and Random Forest were evaluated using different test samples.
- Additional factors, such as detailed weather conditions, could improve the available predictive information.
- The current model performance is not sufficient to recommend deployment in a real operational environment.

## Recommendations & Future Improvements

Potential improvements include:

- Exploring alternative approaches to handling class imbalance.
- Experimenting with classification thresholds to improve the precision-recall trade-off.
- Including flight data from additional months and seasons.
- Incorporating relevant weather information.
- Comparing algorithms using identical training and testing conditions.
- Investigating additional feature engineering and hyperparameter tuning.

## Project Status

**Status: Completed — Academic Machine Learning Project**

The project includes data preparation, model development, experimentation, evaluation and final recommendations.

Further development would be required before considering real-world implementation.

## Author

**Marieta Svetleva**

Bachelor of ICT - AI & Machine Learning  
Fontys University of Applied Sciences

This project was developed as an individual academic challenge to apply machine learning techniques to a real-world classification problem.
