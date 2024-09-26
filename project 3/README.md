# HR Analytics
## Project Description
The company specializes in HR analytics, helping businesses optimize workforce management by using data to minimize financial losses and employee turnover. Machine learning plays a key role in this process, enabling faster and more accurate predictions. The company provided data on employee characteristics, including job satisfaction, which is derived from employee feedback surveys and scored between 0 (completely dissatisfied) and 1 (fully satisfied).

Task 1: Build a model to predict employee satisfaction based on the provided data. This is critical because job satisfaction directly impacts employee turnover, which is a major concern for HR teams.

Task 2: Build a model to predict whether an employee will leave the company based on the available data. This helps mitigate the risks associated with sudden departures, especially of key employees.

## Data Description
For this task, the client provided data with the following features:

- id — unique identifier for the employee;
- dept — department where the employee works;
- level — level of the position held;
- workload — level of employee workload;
- employment_years — duration of employment in the company (in years);
- last_year_promo — indicates whether the employee received a promotion in the last year;
- last_year_violations — indicates whether the employee violated the employment contract in the last year;
- supervisor_evaluation — performance evaluation given to the employee by their supervisor;
- salary — monthly salary of the employee;
- job_satisfaction_rate — employee's job satisfaction level, which is the target variable.

## Libraries Used
- Pandas: For data manipulation and analysis.
- NumPy: For numerical operations.
- Matplotlib: For creating visualizations.
- Seaborn: For enhanced data visualization, including heatmaps.
- Scikit-learn: For machine learning tasks, including:
RandomizedSearchCV, GridSearchCV, StratifiedKFold, cross_val_score: For model selection and validation.
OneHotEncoder, StandardScaler, LabelEncoder, MinMaxScaler, OrdinalEncoder: For preprocessing and encoding categorical variables.
LogisticRegression, LinearRegression, DecisionTreeClassifier, DecisionTreeRegressor, SVC, KNeighborsClassifier: For classification and regression modeling.
DummyClassifier, DummyRegressor: For baseline performance comparison.
confusion_matrix, roc_auc_score, make_scorer, mean_absolute_error, r2_score: For evaluation metrics.
SelectKBest, f_classif, mutual_info_classif: For feature selection.
- Phik: For calculating correlations using the phik_matrix.
- SHAP: For analyzing feature importance.
- Statsmodels: For statistical analysis, including calculating the variance inflation factor (VIF) and performing t-tests.

## Findings and Recommendations
We trained and optimized several models, selecting a DecisionTreeRegressor with hyperparameters max_depth=13, max_features=8, and min_samples_split=8 for predicting satisfaction, achieving SMAPE ≤ 15. For turnover prediction, the best model was a DecisionTreeClassifier with parameters max_depth=6, max_features=19, and min_samples_split=10, achieving ROC AUC scores of 0.895 for training and 0.92 for testing, indicating high effectiveness.

Business Recommendations: Given the high accuracy of the satisfaction prediction model, the company should use it for targeted surveys to improve work conditions and reduce turnover. Attention should be focused on key factors influencing satisfaction and turnover, such as supervisor evaluations, job levels, and salaries. Regularly updating prediction models is crucial to maintain their relevance and accuracy. Further exploration of additional features impacting turnover is recommended to enhance predictive quality, ultimately leading to more effective personnel management and increased employee satisfaction.