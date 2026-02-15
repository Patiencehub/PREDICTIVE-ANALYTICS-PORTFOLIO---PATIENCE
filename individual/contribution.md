Project Overview: Developed a high-performance customer retention engine for a telecommunications provider to identify at-risk customers and provide actionable insights for reducing churn.

Core Contributions & Technical Expertise
Advanced Feature Engineering: Engineered a sophisticated feature set to capture behavioral patterns, including Tenure Log-Scaling for normalized growth tracking, Bundle Scoring to quantify multi-service engagement, and Penalty Fee Analysis to monitor customer friction points.

End-to-End Pipeline Architecture: Designed a production-ready data pipeline using Scikit-Learn’s ColumnTransformer and Pipeline modules. This automated the integration of median-based imputation, standard scaling, and one-hot encoding, ensuring consistency between training and real-world holdout data.

Predictive Modeling: Implemented and optimized an XGBoost Classifier, leveraging its gradient boosting capabilities to handle non-linear relationships and missing data effectively.

Customer Segmentation & Dimensionality Reduction: integrated K-Means Clustering and Principal Component Analysis (PCA) (retaining 90% variance) into the modeling bundle to segment the customer base and reduce noise before prediction.

Strategic Decision-Making
Advocated for an Interpretable AI Framework: I led the decision to integrate SHAP (SHapley Additive exPlanations) values into our final output. While predictive accuracy was paramount, I successfully advocated for this approach because business stakeholders required transparency into why customers were churn risks (e.g., impact of monthly fees vs. tenure) to design effective marketing interventions.

Implementation of a Model Bundle: I proposed packaging the pre-processing, clustering, and predictive stages into a single joblib model bundle. This decision prioritized scalability and ease of deployment for the holdout scoring phase.

Key Lessons & Future Optimization
Data Integrity as a Performance Driver: A critical takeaway was that data cleaning—standardizing service tokens and handling categorical missingness (e.g., "recent_offer_missing")—contributed as much to model stability as hyperparameter tuning.

Roadmap for Improvement: Given more time, I would implement Automated Hyperparameter Optimization (Optuna) to further push the ROC-AUC boundaries. Additionally, I would add a Financial Impact Layer to the model to predict the "Value at Risk," allowing the business to prioritize retention efforts for high-LTV (Lifetime Value) customers.