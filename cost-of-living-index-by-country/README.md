![banner](https://i.imgur.com/NZfh8kK.png)

# Cost of Living Index Analysis

Analyze the cost of living indices across countries and predict cost of living categories (Low, Medium, High) using a Random Forest classification model and other models as comparison. Address class imbalance using SMOTE and optimize model performance through hyperparameter tuning.

## Data Understanding

**Data Description**  
The dataset contains cost of living indices across countries. The dataset contains the following columns:
- Rank
- Country
- Cost of Living Index
- Rent Index
- Cost of Living Plus Rent Index
- Groceries Index
- Restaurant Price Index
- Local Purchasing Power Index

**Initial Data Exploration**
1. Load the dataset.
2. Display the first five rows.
3. Sort the data by Cost of Living Index in descending order.
4. Display the top 10 countries with the highest and lowest Cost of Living Index.

## Data Preparation

1. Feature Selection
   
   - Selected features
        
     - Groceries Index
     - Restaurant Price Index
     - Rent Index
   - Target variable
     - Cost of Living Index (categorized into Low, Medium, High)

2. Categorization

   - Create a function to classify the Cost of Living Index into Low, Medium, and High categories.
   - Apply the function to create a new column 'Cost of Living Class'.

3. Train-Test Split

   - Split the data into training and testing sets.

4. Resampling

   - Apply SMOTE to address class imbalance in the target variable.

## Modeling

**Model Selection**

1. Random Forest Classifier

    - Train the Random Forest model on the resampled training data.
    - Generate prediction on the test set.

## Evaluation

**Metrics**

- Accuracy
- Classification Report

**Results**

1. Initial model accuracy: 0.76 or 76%
2. Cross-validated accuracy: 0.876 or 87.6%

**Observations**

- The model showed somewhat good precision, recall, and F1-score for the "High" class but the performance for the "Low" and "Medium" classes needed improvement.

## Optimization

**Model Validation**

- Used Stratified K-Fold Cross-Validation to evaluate the model’s generalizability.

**Hyperparameter Tuning**

- Used Grid Search, `GridSearchCV`, to find the best hyperparameters for the Random Forest model.

  - Best parameters are
    - `max_depth`: None
    - `min_samples_leaf`: 1
    - `min_samples_split`: 10
    - `n_estimators`: 50
- Optimized model accuracy: 0.9533 or 95.33%

The hyperparameter tuning significantly improved model performance, achieving an accuracy of 95.33%.

## Data Visualization

**Exploratory Data Analysis**

1. Visualize the top and least expensive countries by various indices (Cost of Living Index, Groceries Index, Restaurant Price Index, Rent Index).
2. Pairplot to visualize relationships between indices.
3. Correlation Matrix to understand relationships between different indices.

**Key Insights**

- Strong positive correlations between Cost of Living Index and Groceries Index, and between Cost of Living Index and Restaurant Price Index.
- Moderate positive correlation between Cost of Living Index and Rent Index.