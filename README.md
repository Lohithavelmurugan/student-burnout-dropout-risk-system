# Student-Burnout-Dropout-Risk-System
# Overview

This project focuses on early detection of student burnout, academic disengagement, and dropout probability using behavioural analytics. Modern LMS platforms generate behavioural signals such as login patterns, assignment submission delays, irregular study routines, attendance trends, and student sentiment. These indicators can reveal early signs of academic risk long before grades begin to decline.

The system applies machine learning models to classify burnout levels, estimate dropout probability, and generate behavioural insights that help institutions take proactive action.

# Objectives

Predict burnout level: Low, Medium, High

Estimate dropout probability (0–1)

Identify academic disengagement indicators

Extract key behavioural triggers influencing risk

Suggest intervention strategies for high-risk students

Provide analytics and insights to support academic decision-making

# Project Structure
project/
│
├── data/
│   └── synthetic_student_behaviour.csv
│
├── src/
│   ├── student_burnout_pipeline.py
│   
│
├── docs/
│   └── Model_Explanation_Document.pdf
│
├── visuals/
│   ├── correlation_heatmap.png
│   ├── burnout_distribution.png
│   ├── cluster_plot.png
│
├── presentation/
│   └── Burnout_Dropout_Prediction_PPT.pptx
│
└── README.md

# Dataset Description

The project uses synthetic data (10,000 records) created to mimic realistic student behavioural patterns observed in LMS environments.

# Behavioural Features :

 1.LMS logins per week

 2.Average submission delay (days)

 3.Attendance percentage

 4.Inactivity gap days

 5.Night activity ratio

 6.Study-time variance

 7.Psychological Features

 8.Sentiment score (−1 to +1)

 9.Feedback negativity flag

# Academic Features :

 1.Past semester GPA

 2.GPA drop rate

 3.Labels

 4.Burnout level

 5.Dropout probability

 6.Disengagement flag

 7.Feature Engineering

# Key derived features include:

Engagement Index:

A combined score representing learning involvement based on LMS logins and assignment punctuality.

Stress Score:

Captures lifestyle irregularity using night activity ratio and study-time variance.

Risk Behaviour Index:

A composite weighted index representing behavioural, emotional, and academic risk contributors.

# Models Used
1. Burnout Prediction (Classification)

Model: Random Forest Classifier
Output: Burnout Level (Low / Medium / High)

2. Dropout Prediction (Regression)

Model: XGBoost Regressor
Output: Dropout probability (0–1)

3. Behavioural Pattern Clustering

Model: K-Means
Purpose: Identify behavioural clusters such as Engaged, Moderately Engaged, and At-Risk.

# Evaluation Metrics
1.For Burnout Classification

Accuracy

Precision

Recall

F1 Score

Confusion Matrix

2.For Dropout Regression

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² Score

3.For Clustering

Silhouette Score

Davies–Bouldin Index

# Key Insights

Submission delays are strongly associated with burnout risk.

Low attendance significantly increases dropout probability.

Negative sentiment indicates emotional fatigue or academic stress.

Behaviour clusters reveal distinct engagement differences across students.

Higher stress scores and irregular study patterns correspond to elevated academic risk.

# How to Run
1. Install required libraries
pip install -r requirements.txt
2. Run the machine learning pipeline
python student_burnout_pipeline.py
3. (Optional) Launch the analytics dashboard
streamlit run app.py
Use Cases

Early detection of at-risk students

Counselling and academic intervention planning

Student performance monitoring

Behaviour-driven academic analytics

Institutional academic risk management

Author

Lohitha V
M.Tech (Integrated) – CSE (Business Analytics)
