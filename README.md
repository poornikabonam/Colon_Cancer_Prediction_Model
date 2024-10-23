# Colon_Cancer_Prediction_Model
A machine learning solution to predict colon cancer types by combining clinical and pathological data. The project focuses on merging two unrelated datasets while maintaining data integrity and predictive accuracy.

# Data Analysis and Preprocessing
## Initial Dataset Overview
   - Two datasets containing clinical records of colon cancer patients were analyzed

   - Clinical Dataset: 300 records with clinical measurements and patient history
Pathological Dataset: 100 records with pathology results and risk factors

## Data Preprocessing Steps
### Categorical Variable Handling
Label encoding transformed categorical variables into numerical format for model processing. For example, 'Yes/No' responses in Family History became '1/0'.

### Missing Value Treatment
The unique approach involved class-based imputation, where missing values were filled based on the specific cancer type. This preserved the relationship between features and the target variable, resulting in more meaningful data.

### Outlier Analysis
![image](https://github.com/user-attachments/assets/15cf1cb5-3cd4-46e5-bd45-8f1aa2d980fe)

The box plots revealed:
   - Age distribution varies across cancer types with minimal outliers
   - CEA Level showed significant outliers particularly in Type 2 cancer
   - Polyp Size maintained consistent range across types
   - Tumor Grade showed discrete value distribution

### Feature Analysis
![image](https://github.com/user-attachments/assets/d210971d-1221-45ea-9c71-c8a24926b3db)

The correlation matrix highlighted:
   - Strong correlations between pathological features
   - Weak correlations among clinical measurements
   - Independent nature of features between datasets

## Model Development
Why Random Forest?
   - Handling Complex Data
      - Effectively manages both numerical and categorical features
      - Robust to outliers and non-linear relationships
      - Handles missing values effectively

   - Feature Importance
     - Provides clear feature importance rankings
     - Helps understand key predictive factors
     - Guides future data collection priorities

   - Ensemble Advantage
     - Reduces overfitting through multiple decision trees
     - Improves generalization
     - Provides robust predictions
    
### Feature Importance
![image](https://github.com/user-attachments/assets/6dac6483-560b-4e21-8acb-22ff4d0928a5)

    
## Model Optimization
### Hyperparameter Tuning
   - Selected Parameters
      - n_estimators=100: Balances complexity and performance
      - max_depth=10: Prevents overfitting
      - min_samples_split=10: Ensures robust splits
      - min_samples_leaf=5: Maintains prediction stability

### Overfitting Prevention
   - Cross-Validation Strategy
      - Implemented 5-fold stratified cross-validation
   - Results:
      - Average CV Score: 0.961
      - Standard Deviation: ±0.014
      Demonstrates model stability and reliability

## Model Performance
![image](https://github.com/user-attachments/assets/2f51cc60-b64e-4149-987b-dbdc65290914)

Confusion Matrix Analysis
   - Type-Specific Performance
      - Type 1: 100% recall, 88% precision
      - Type 2: 91% recall, 95% precision
      - Type 3: 90% recall, 100% precision
   - Overall Metrics
      - Test Accuracy: 94%
      - Weighted Average F1-Score: 0.94
      - Consistent performance across all cancer types


