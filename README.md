# ML_House_Data




# Linear Regression
# 🏠 Housing Price Prediction — Machine Learning Project (Random Forest)
#
# ## 📌 Project Summary
# This project builds a machine learning model to predict housing prices using a 
# Random Forest Regressor. Beyond model accuracy, the focus is on extracting 
# actionable insights from data — aligning technical modeling with business value.
#
# The project demonstrates:
# - End-to-end ML workflow (data → model → evaluation → insights)
# - Model interpretability via feature importance
# - Practical understanding of regression metrics
# - Structured experimentation with hyperparameter tuning
#
# ---
#
# ## 🎯 Business Context
# Accurate housing price prediction is critical for:
# - Real estate valuation
# - Investment decision-making
# - Risk assessment in lending
#
# This model aims to support data-driven pricing strategies by identifying 
# the key drivers behind property value.
#
# ---
#
# ## 🧠 Model Choice
# The core model used is:
# 👉 Random Forest Regressor (from scikit-learn)
#
# Why Random Forest?
# - Handles non-linear relationships well
# - Robust against overfitting (vs single decision trees)
# - Provides built-in feature importance (interpretability)
#
# ---
#
# ## ⚙️ Tech Stack
# - Python
# - pandas / numpy
# - scikit-learn
# - matplotlib
# - (optional experimentation with XGBoost)
#
# ---
#
# ## 🔄 Workflow
#
# ### 1. Data Preparation
# - Load cleaned dataset
# - Define features (X) and target (y)
# - Train-test split
#
# ### 2. Model Training
# Random Forest with controlled complexity:
#
# - n_estimators = 200
# - max_depth = 20
# - min_samples_split = 2
#
# ### 3. Evaluation Metrics
# The model is evaluated using:
#
# - R² Score → goodness of fit
# - MAE → average prediction error
# - RMSE → penalty on large errors
# - MAPE → percentage-based error (business-friendly)
#
# This combination ensures both statistical and practical interpretability.
#
# ---
#
# ## 📊 Results & Interpretation
#
# Key observations:
# - The model captures non-linear relationships effectively
# - Train vs Test performance indicates controlled overfitting
# - Feature importance highlights the strongest price drivers
#
# This enables moving from "prediction" → "decision support"
#
# ---
#
# ## 🔍 Feature Importance
#
# Feature importance analysis answers:
# 👉 What actually drives house prices?
#
# This is critical in business contexts where stakeholders need:
# - transparency
# - explainability
# - justification of model outputs
#
# ---
#
# ## ⚡ Hyperparameter Tuning
#
# A GridSearchCV approach is used to optimize:
# - max_depth
# - n_estimators
#
# This ensures the model is not just functional, but tuned for performance.
#
# ---
#
# ## 🚧 Limitations
#
# - Limited hyperparameter search space
# - No advanced feature engineering
# - No external data enrichment
# - No model comparison benchmark (e.g., XGBoost vs Linear Regression)
#
# ---
#
# ## 🔮 Future Improvements
#
# Planned upgrades:
#
# - Expand tuning (RandomizedSearch / Bayesian optimization)
# - Add feature engineering (interaction terms, scaling where relevant)
# - Compare multiple models:
#   - XGBoost
#   - Gradient Boosting
#   - Linear Regression (baseline)
# - Residual diagnostics
# - Deploy model (API or dashboard)
#
# ---
#
# ## ▶️ How to Run
#
# 1. Install dependencies:
#    pip install pandas numpy scikit-learn matplotlib xgboost
#
# 2. Launch notebook:
#    jupyter notebook
#
# 3. Open:
#    03_random_forest.ipynb - Features 2nd attempt.ipynb
#
# ---
#
# ## 💡 Key Takeaway
#
# This project goes beyond building a model — it focuses on translating 
# machine learning outputs into interpretable, business-relevant insights.
#
# It reflects a practical approach to data science:
# 👉 not just predicting outcomes, but enabling better decisions.
#
# ---
#
# ## 👤 Author
# Alex
#
# Background:
# - Sales & Customer Operations (SaaS / Industrial Tech)
# - Transitioning into Data & Machine Learning
# - Strong interest in applying AI to real-world business problems
#
# ---



# Random Tree




# Boosting 
## Model Development: Boosting Algorithms
In this project, we focused on implementing and optimizing ensemble boosting models for house price prediction. The models explored include:
* XGBoost Regressor 
* AdaBoost Regressor
* Gradient Boosting Regressor 

These models were selected due to their ability to capture non-linear relationships and interactions between features, which are common in real estate data. 

## Hyperparameter Tuning 

To improve model performance, hyperparameters were optimized (for example, number of estimators, learning rate, max depth, sub-sampling).

The tuning process aimed to balance:
* Model complexity
* Overfitting vs. Generalization
* Computational efficiency 

XGBoost, in particualr, benefited from tuning parametrs such as:

* n_estimators
* learning_rate
* max_depth
* subsample
* colsample_bytree

## Feature Engineering 

To enhance predictive performance, additional features were created while retaining the original dataset:

* Distance from city center (distance_center): derived from latitude and longitude
* Engineered features were added without removing original variables to preserve information 

This approach ensured that:
* Spatial relationships were maintained
* The model could learn both raw and transofmred representations 

## Model Evaluation 

Models were evaluated using:

* Mean Absolute Error (MAE): measures average prediction error 
* R-squared: measures explained variance 

## Key Results (Test Set)
| Model                   | MAE           | R_squared     | 
|-------------------      |-------------  |------------   |
| XGBoost                 | 6.4e4         | 0.89          | 
| AdaBoost                | 9.3e4         | 0.85          | 
| Gradient                | 6.7e4         | 0.88          | 
## Key Findings

* Boosting models significantly outperformed baseline models (Linear Regression, KNN)
* XGBoost achieved the best overall performance
* Feature engineering provided a modest improvement, especially for XGBoost
* All models showed slight overfitting, but generalization remained strong

## Conclusion

* XGBoost was selected as the final model due to its superior predictive performance and ability to generalize well to unseen data. 

