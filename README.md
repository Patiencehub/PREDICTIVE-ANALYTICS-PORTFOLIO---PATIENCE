# PREDICTIVE-ANALYTICS-PORTFOLIO---PATIENCE
# TruSource Churn Prediction Project

## Overview
This project builds a predictive analytics solution to identify customers at risk of churn for TruSource. The goal is to move from reactive retention strategies to a proactive, data-driven approach that detects high-risk customers early and enables targeted interventions. The solution combines machine learning, feature engineering, and customer segmentation to generate actionable business insights.

## Project Objectives
- Predict likelihood of customer churn
- Identify key factors driving churn
- Segment customers into risk groups
- Support targeted retention strategies
- Optimize retention spending efficiency

## Repository Contents
├── GROUP_8_XGBOOST_MODEL.ipynb  
Full modeling pipeline including preprocessing, feature engineering, model training, and evaluation  

├── GROUP 8_SCORED_HOLDOUT_CODES.ipynb  
Applies trained model to holdout dataset for prediction  

├── featured_dataset_with_target.csv  
Prepared dataset with engineered features and target variable  

## Modeling Approach

### Models Tested
- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost (final model)

### Final Model Selection
XGBoost was selected because it produced the strongest performance for detecting churners, especially within the minority class, while maintaining a strong balance between precision and recall.

## Evaluation Metrics
Models were evaluated using:

- ROC-AUC
- F1 Score
- Recall (priority metric)
- Accuracy

**Why Recall was prioritized:**  
Missing a churner is more costly than incorrectly flagging a loyal customer.

## Feature Engineering
Key preprocessing steps included:

- Missing value imputation
- Tenure binning into lifecycle categories
- Aggregation of fee variables into a single friction metric
- Binary feature creation
- One-hot encoding of categorical variables

## Key Model Insights
Important predictors of churn:

- Low tenure
- Month-to-month contracts
- Manual payment methods
- Low service engagement

Factors associated with retention:

- Longer tenure
- Higher usage
- Automatic payment enrollment
- Bundled services

## Customer Segmentation Strategy

| Segment | Description | Strategy |
|--------|-------------|---------|
| Loyal Backbone | Long-tenured stable customers | Technology upgrades |
| VIP Band | Highest value customers | Premium loyalty perks |
| Red Hot | High churn risk | Incentives + friction reduction |


## Business Recommendations
Model insights support targeted retention strategies:

- Proactive outreach for high-risk customers
- Incentives for autopay adoption
- Service upgrades for loyal customers
- Premium engagement for high-value clients


## Trade-Off Considerations
- Incentives reduce short-term margins
- Upgrades require infrastructure investment
- Premium experiences increase cost

However, customer acquisition costs are significantly higher than retention costs, making targeted retention financially beneficial.


## How to Run

Clone repository:
