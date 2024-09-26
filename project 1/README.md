# Dairy Farm Data Analysis
## Project Description
A farmer, who owns a dairy farm, has approached us. He wants to buy cows to expand his herd. For this, he has signed a favorable contract with the "EcoFarm" Pasture Association. The terms allow the farmer to carefully select the cows. He determines milk quality using a strict methodology while needing to meet his dairy farm development plan. The farmer wants each cow to produce at least 6000 kilograms of milk per year, and the milk must be tasty — by his strict standards, no less. Sellers and technologists tend to exaggerate the qualities of their cows!
The task is to develop a machine learning model that will help manage risks and make an objective decision about purchasing cows. Two predictive models need to be created for selecting cows for the herd:
The first model will predict the cow's potential milk yield (target variable: Milk Yield).
The second model will calculate the probability of getting tasty milk from the cow (target variable: Milk Taste).
The model should help select cows based on two criteria:
- Annual average milk yield of at least 6000 kilograms.
- The milk must be tasty.

## Data Description
The file contains data about the farmer’s current herd.

- id: Unique identifier of the cow.
- Milk Yield (kg) (milk_yield_kg): The amount of milk the cow produces per year (in kilograms).
- Energy Feed Unit (energy_feed_unit): A measure of the nutritional value of the cow’s feed.
- Crude Protein (g) (crude_protein_g): The amount of crude protein in the feed (in grams).
- Sugar-Protein Ratio (sugar_protein_ratio): The ratio of sugar to protein in the cow’s feed.
- Breed (cow_breed): The breed of the cow.
- Pasture Type (pasture_type): The type of landscape on which the cow grazes.
- Sire's Breed (dad_breed): The breed of the cow's sire.
- Fat Percentage (%) (fat_percentage): The fat content of the milk (in percent).
- Protein Percentage (%) (protein_percentage): The protein content of the milk (in percent).
- Milk Taste (taste): The farmer's assessment of taste, a binary feature (tasty, not tasty).
- Age (age): The age of the cow, a binary feature (less than 2 years, more than 2 years).

The features in ferma_main can be grouped as follows:

- Cow Characteristics: id, Breed, Sire's Breed, Age.
- Feed Characteristics: Energy Feed Unit, Crude Protein, Sugar-Protein Ratio.
- Pasture Characteristics: Pasture Type.
- Milk Characteristics: Milk Yield (kg), Fat Percentage (%), Protein Percentage (%), Milk Taste.
- The ferma_dad file stores the name of the sire of each cow in the farmer’s herd.

## Libraries Used
- Pandas: For data manipulation and analysis.
- NumPy: For numerical operations.
- Matplotlib: For data visualization (plots and charts).
- Seaborn: For enhanced data visualization, including heatmaps and pairplots.
- Scikit-learn:
train_test_split: To split the dataset into training and test sets.
OneHotEncoder: For encoding categorical variables.
StandardScaler: For standardizing the features.
LabelEncoder: For encoding the target variable.
LinearRegression: For linear regression modeling.
LogisticRegression: For logistic regression modeling.
r2_score, mean_squared_error, mean_absolute_error: For regression model evaluation metrics.
accuracy_score, precision_score, recall_score, confusion_matrix, precision_recall_curve: For classification model evaluation metrics.
- Phik: For calculating the correlation matrix using the phik_matrix.
- SHAP: For feature importance analysis using SHAP values.

## Findings and Recommendations

Based on the analysis, after filtering cows with annual milk yield above 6000 kg and milk rated as "tasty" by the model, the following results were found:
For the model with a threshold of 0.82: No cows met the criteria, likely due to the high threshold, making the selection too strict.
For the model with a threshold of 0.73: Only two cows met the criteria. Both belong to the Vis Bic Ideal breed with milk yields of 6147.27 kg and 6065.42 kg, respectively. Lowering the threshold allowed the identification of these cows, indicating that a strict threshold might exclude suitable candidates.