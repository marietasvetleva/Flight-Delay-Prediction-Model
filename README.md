# Flight Delay Prediction

## Overview

Flight delays affect passengers, airlines, airports and the wider aviation network. Delays can be caused by multiple factors, including weather conditions, airport congestion, air traffic control restrictions, airline operations and delays carried over from previous flights.

This project explores these factors and applies Machine Learning to predict flight delays using historical flight and operational data.

The project combines domain research, data analysis, data preprocessing, feature engineering, model development and evaluation to investigate how accurately flight delays can be predicted.



## Project Goal

The main goal of this project is to develop a Machine Learning model capable of predicting whether a flight is likely to experience a delay.

The project focuses on:

- Understanding the main causes of flight delays
- Exploring patterns within historical flight data
- Identifying variables that influence delays
- Preparing and transforming data for Machine Learning
- Training and comparing prediction models
- Evaluating model performance
- Understanding which factors contribute most to flight delays



## Research Questions

Before developing the prediction model, domain research is conducted to better understand flight delays and determine which variables may be relevant.

The research focuses on questions such as:

1. What is considered a flight delay?
2. What are the main causes of flight delays?
3. How do time-related factors such as time of day, day of week, and season influence delays?
4. What are the impacts of flight delays, and how can delay prediction be beneficial?


## Machine Learning Workflow

The project follows a structured Machine Learning workflow:

**1. Domain Understanding**  
Research the aviation domain and understand how flight delays occur.

**2. Data Understanding**  
Explore the dataset, variables, distributions, missing values and potential relationships.

**3. Data Preparation**  
Clean the data, handle missing values, encode categorical variables and prepare features for modelling.

**4. Exploratory Data Analysis (EDA)**  
Visualize patterns and investigate relationships between potential predictors and flight delays.

**5. Feature Engineering & Selection**  
Create and select relevant variables that may improve prediction performance.

**6. Model Development**  
Train Machine Learning models using the prepared dataset.

**7. Model Evaluation**  
Evaluate and compare models using appropriate classification metrics.

**8. Improvement**  
Analyse model weaknesses and experiment with preprocessing, features and model parameters.



## Model Evaluation

Depending on the final modelling approach, performance will be evaluated using metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Additional metrics may be introduced as the project develops.



## Technologies

The project is primarily developed using:

- **Python**
- **Jupyter Notebook**
- **Pandas** – data manipulation and analysis
- **NumPy** – numerical operations
- **Matplotlib** – data visualization
- **Scikit-learn** – preprocessing, Machine Learning and model evaluation

Additional libraries may be added during development.


## Repository Structure

```text
flight-delay-prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── data_understanding.ipynb
│   ├── data_preprocessing.ipynb
│   ├── exploratory_data_analysis.ipynb
│   └── model_development.ipynb
│
├── research/
│   └── domain_research.md
│
├── models/
│
├── src/
│
├── requirements.txt
├── .gitignore
└── README.md
```

The repository structure may change as the project develops.



## Current Status

**Project Status: In Development**

Current work focuses on:

- Flight delay domain research
- Understanding potential delay factors
- Dataset exploration
- Preparing the Machine Learning approach

The README and repository will be updated as new experiments, models and results are completed.



## Future Development

Planned next steps include:

- Complete exploratory data analysis
- Finalise data preprocessing
- Identify the most relevant predictive features
- Train baseline Machine Learning models
- Compare multiple algorithms
- Perform hyperparameter tuning
- Analyse feature importance
- Evaluate the final model
- Document findings and limitations


## Author

**Marieta Svetleva**  
ICT Student – AI & Machine Learning  
Fontys University of Applied Sciences


## Academic Context

This project is developed as part of the **AI & Machine Learning semester** within the ICT Bachelor programme at **Fontys University of Applied Sciences**.

The project is intended to demonstrate the application of Machine Learning techniques to a real-world prediction problem while combining technical development with domain understanding and research.