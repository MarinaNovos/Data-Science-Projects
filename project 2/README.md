# Online Store Data Analysis
## Project Description
An online store offers a variety of products: children’s goods, home items, small appliances, cosmetics, and even food. Recent reports have shown a decline in customer activity. Attracting new customers is no longer as effective, as most of the target audience is already aware of the store. To counter this, the company aims to retain current customers by increasing their engagement through personalized offers. As a modern company, "One Click" wants to base decisions on data analysis and business modeling. You are assigned as an intern in the digital technologies department to help develop a solution for personalizing offers and boosting customer activity.

## Data Description
The data file includes customer behavior on the website, communication records, and product-related behavior.

## Libraries Used
- Pandas: For data manipulation and analysis.
- NumPy: For numerical operations.
- Matplotlib: For creating visualizations.
- Seaborn: For enhanced data visualization, including heatmaps.
- Scikit-learn: For machine learning tasks, including:
train_test_split: To split the dataset.
OneHotEncoder: For encoding categorical variables.
StandardScaler: For feature scaling.
LabelEncoder: For encoding the target variable.
LogisticRegression, DecisionTreeClassifier, SVC: For classification modeling.
DummyClassifier: For baseline performance comparison.
confusion_matrix, roc_auc_score, f1_score: For evaluation metrics.
- Phik: For calculating correlations using the phik_matrix.
- SHAP: For analyzing feature importance.

## Findings and Recommendations
After data preprocessing and exploratory analysis, we tested several models including Logistic Regression, SVC, KNeighborsClassifier, and DecisionTreeClassifier. Using RandomizedSearchCV, the Support Vector Classifier (SVC) with optimal parameters was selected as the best model for predicting customer activity. SHAP and SelectKBest were used to assess feature importance, revealing that key factors influencing purchasing activity included pages per visit, time on site, and category views. Less significant factors were promotional purchases, unpaid products, and marketing activity. KMeans clustering segmented users into five groups, with Cluster 0 identified for further analysis due to high revenue and category views but low page views and time on site. Recommendations were developed based on this segmentation.