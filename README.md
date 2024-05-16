# Advertising Modeling Analysis


## Introduction
This analysis aims to build predictive models to estimate sales based on advertising budgets across three channels: TV, Radio, and Newspaper. This is a regression problem where the goal is to predict the continuous outcome (sales) based on the input features (advertising budgets). The process involves data cleaning, exploratory data analysis (EDA), feature selection, model building, model evaluation, and selecting the best-performing model.

## 1. Data Cleaning
The dataset was loaded, and it was confirmed that there were no missing values. Summary statistics were generated to understand the basic distribution of the data.

## 2. Exploratory Data Analysis (EDA)
EDA was performed using pair plots and a correlation heatmap:
- **Pair Plots**: Visualized the relationships between TV, Radio, Newspaper budgets, and Sales.
- **Correlation Heatmap**: Indicated positive correlations between the advertising budgets and sales, with TV showing the strongest correlation.

## 3. Feature Selection
The features selected for modeling were:
- **TV**: Advertising budget for TV.
- **Radio**: Advertising budget for Radio.
- **Newspaper**: Advertising budget for Newspaper.
The target variable was **Sales**.

## 4. Model Building
The following models were built and evaluated:
- **Linear Regression**
- **Decision Tree**
- **Random Forest** (with hyperparameter tuning using GridSearchCV)
- **Gradient Boosting** (with hyperparameter tuning using GridSearchCV)

## 5. Model Evaluation
The models were evaluated using Mean Squared Error (MSE) and R-squared (R²) metrics:

| Model              | MSE       | R-squared |
|--------------------|-----------|-----------|
| Linear Regression  | 3.174097  | 0.899438  |
| Decision Tree      | 2.175000  | 0.931091  |
| Random Forest      | 0.573405  | 0.981833  |
| Gradient Boosting  | 0.601117  | 0.980955  |



**Decision Tree** was identified as the best-performing model based on the highest R-squared value and lowest MSE.

## Best Model Saving and Loading
The best model (Decision Tree) was saved for future use, and predictions were made on new, unseen data using the saved model.

## Feature Importance Analysis
Feature importance was analyzed for the Decision Tree model, highlighting the contributions of each feature (TV, Radio, Newspaper) to the sales predictions.

## Conclusion
The Decision Tree model provided the highest predictive accuracy, making it the best choice for predicting sales based on advertising budgets. This model can be used to make reliable predictions and informed decisions regarding advertising budget allocations.

**Note**: The saved best model can be loaded and used for making predictions on new data. The analysis also provides insights into which advertising channels are most influential in driving sales.
