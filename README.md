# ML_House_Data




# Linear Regression




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

