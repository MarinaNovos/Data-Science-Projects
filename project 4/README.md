# Well Location Selection
## Project Description
The project involves selecting the optimal location for drilling a new oil well within a mining company by leveraging machine learning. Using data from three regions, each containing 10,000 oil deposits with measured quality and volume, we will build a model to identify the region with the highest potential profit, analyze potential returns and risks using Bootstrap, and select the best 200 deposits for development based on budget constraints and profit estimates.

## Data Description
The geological exploration data for three regions is contained in the files:

- id — unique identifier for the well;
- f0, f1, f2 — three features of the points (the specific meaning of these features is not important, but they are significant);
- product — volume of reserves in the well (in thousands of barrels)

## Libraries Used
- Pandas: For data manipulation and analysis.
- NumPy: For numerical operations.
- Matplotlib: For creating visualizations.
- Seaborn: For enhanced data visualization, including heatmaps.
- Scikit-learn: For machine learning tasks, including:
train_test_split: To split the dataset.
GridSearchCV: For hyperparameter tuning.
cross_val_score: For cross-validation.
StandardScaler and MinMaxScaler: For feature scaling.
SimpleImputer: For handling missing data.
Pipeline and ColumnTransformer: For streamlined preprocessing.
Ridge, Lasso, and ElasticNet: For regression modeling.
DummyRegressor: For baseline performance comparison.
confusion_matrix and mean_squared_error: For evaluation metrics.
- Statsmodels: For statistical analysis, including:
variance_inflation_factor: For assessing multicollinearity.
add_constant: For adding a constant to the dataset.
- Phik: For calculating correlations using the phik_matrix.

## Findings and Recommendations
Region 1 is the most profitable area for drilling based on the model, showing the highest average profit of 421,219 thousand rubles and a minimal loss risk of 1.8%. In contrast, Regions 0 and 2 present similar outcomes, but their loss risks exceed the acceptable threshold of 2.5%. Specifically, Region 2 has a loss risk of 8.3%, making it less attractive despite relatively high average profits. The confidence intervals for Regions 0 and 2 also include negative values, indicating potential investment risks in these areas.