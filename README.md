# Colon_Cancer_Prediction_Model
A machine learning solution to predict colon cancer types by combining clinical and pathological data. The project focuses on merging two unrelated datasets while maintaining data integrity and predictive accuracy.

## Data Analysis and Preprocessing
1. Initial Dataset Overview
   - Two datasets containing clinical records of colon cancer patients were analyzed:

   - Clinical Dataset: 300 records with clinical measurements and patient history
Pathological Dataset: 100 records with pathology results and risk factors

2. Data Preprocessing Steps
### Categorical Variable Handling
Label encoding transformed categorical variables into numerical format for model processing. For example, 'Yes/No' responses in Family History became '1/0'.
### Missing Value Treatment
The unique approach involved class-based imputation, where missing values were filled based on the specific cancer type. This preserved the relationship between features and the target variable, resulting in more meaningful data.
Outlier Analysis

### Outlier Analysis

