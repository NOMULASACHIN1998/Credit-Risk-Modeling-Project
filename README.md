📊 Credit Risk Modeling — Lauki Finance

A Complete End-to-End Machine Learning Pipeline for Predicting Loan Defaults

📌 Overview

Credit risk modeling helps lenders understand which customers are likely to default on their loans.
In this project, we built a complete ML pipeline using customer data, loan attributes, and bureau information to predict loan default probability.

The final model assists the Risk Unit in making data-driven loan approval decisions.

🎯 Project Objective

Develop a machine learning model that:

Learns from past loan repayment behavior

Identifies patterns that indicate high risk

Predicts the probability of loan default

Helps reduce financial losses for the lender

🏆 Success Criteria
Metric	Target	Description
AUC	> 0.85	Ability to distinguish good vs bad borrowers
Gini Coefficient	> 0.85	Measures model discriminatory power
KS Statistic	> 40	Separation between good & bad customers
KS Deciles	High KS in first 3 deciles	Risky borrowers ranked at the top
Interpretability	Mandatory	Must explain why predictions occur

These targets follow industry standards in banking and credit risk.

🗂️ Dataset Description
📅 Time Period

Training & Validation: Feb 2022 → Feb 2024

Out-of-Time (OOT) Test: Mar 2024 → May 2024

🔀 Train-Test Split

75% Training

25% Testing

OOT testing ensures the model works well on future unseen data.

🔍 Feature Categories
1️⃣ Customer Features

Demographic and socio-economic data:

Age

Income

Employment type

Marital status

Location

2️⃣ Loan Features

Details of the current loan:

Loan amount

Tenure

EMI

Interest rate

Loan purpose

3️⃣ Bureau Features

External credit performance:

Past delinquency

Outstanding loans

Credit utilization

Recent credit inquiries

Bureau data is typically the most predictive for credit scoring.

🧹 Data Preprocessing
✔ Cleaning

Fixed invalid values (e.g., incorrect loan purposes)

Imputed missing values

✔ Feature Selection

Used a combination of:

Information Value (IV) → Identify predictive variables

Variance Inflation Factor (VIF) → Remove multicollinearity

Domain expert rules

✔ Scaling

Applied Min-Max Scaling to numerical attributes.

🤖 Modeling
🔧 Algorithms Trained

Logistic Regression (Baseline + Highly interpretable)

Random Forest (Handles nonlinear patterns)

XGBoost (High-performance gradient boosting model)

⚙ Hyperparameter Tuning

RandomizedSearchCV

Optuna (Automated tuning)

Optuna significantly improved accuracy & reduced training time.

📈 Evaluation Metrics
✔ AUC (Area Under ROC Curve)

Measures model’s ability to rank borrowers correctly.

✔ Gini Coefficient

Derived from AUC → Industry standard for scorecards.

✔ KS Statistic

Indicates how well the model separates good vs bad customers in deciles.

✔ Classification Report

Includes precision, recall, f1-score.

✔ Decile (Rank Ordering) Analysis

Ensures bad borrowers appear in top risk buckets.

🧪 Experiment Summary

Multiple experiments were performed by testing:

Different models

Different hyperparameters

Different feature sets

The final chosen model exhibited:

High AUC

Strong KS

Good Gini

Excellent stability on OOT data

Clear interpretability