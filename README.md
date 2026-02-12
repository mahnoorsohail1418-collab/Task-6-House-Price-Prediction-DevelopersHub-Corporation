Task 6: House Price Prediction - DevelopersHub Corporation

Task Objective                                                                                                                                                                                                      
The main objective of this task is to build a regression model that predicts house prices based on property features such as square footage, number of bedrooms, bathrooms, grade, and location (zipcode).
This task demonstrates the practical implementation of regression modeling in real estate data analysis and highlights the importance of preprocessing, feature engineering, and evaluation metrics in machine learning pipelines.

Specifically, this task focuses on:                                                                                                                                                                                 
1.Loading and understanding a real-world housing dataset.                                                                                                                                                           
2.Performing preprocessing on numerical and categorical features.                                                                                                                                                   
3.Training regression models.                                                                                                                                                                                       
4.Evaluating performance using MAE and RMSE.                                                                                                                                                                        
5.Visualizing predicted vs actual prices.                                                                                                                                                                           

Dataset Used                                                                                                                                                                                                        
Name: King County House Sales Dataset                                                                                                                                                                               
Source: Kaggle                                                                                                                                                                                                      
Total Samples: 21,613 houses                                                                                                                                                                                        
Total Features: 21 columns                                                                                                                                                                                          

Target Variable:                                                                                                                                                                                                    
price (House sale price)

Main Features Used:                                                                                                                                                                                                 
sqft_living (Living area in square feet)                                                                                                                                                                            
bedrooms (Number of bedrooms)                                                                                                                                                                                       
bathrooms (Number of bathrooms)                                                                                                                                                                                     
grade (Overall grade given to the house)                                                                                                                                                                            
zipcode (Location feature)                                                                                                                                                                                          

Models Applied                                                                                                                                                                                                     Two regression models were implemented:                                                                                                                                                                             1️.Linear Regression                                                                                                                                                                                                
Baseline regression model,
Assumes linear relationship between features and price,
Simple and interpretable.

2️.Gradient Boosting Regressor                                                                                                                                                                                     
Ensemble-based model,
Handles non-linear relationships,
Typically performs better on complex datasets.

Tools and Technologies Used                                                                                                                                                                                         
Python                                                                                                                                                                                                              
Pandas (Data manipulation)                                                                                                                                                                                          
NumPy (Numerical operations)                                                                                                                                                                                        Matplotlib (Visualization)                                                                                                                                                                                          
Scikit-learn (Machine Learning models and preprocessing)                                                                                                                                                                  

Techniques Applied:                                                                                                                                                                                                 
Feature Scaling (StandardScaler)
One-Hot Encoding (for zipcode)                                                                                                                                                                                     

Train-Test Split (80-20 split)                                    
Pipeline & ColumnTransformer                                                                                                                                                                                        

Model Evaluation (MAE & RMSE)                                                                                                                                                                                       

Steps Performed                                                                                                                                                                                                     
1️.Import Libraries                                                                                                                                                                                                 
Imported required libraries:
pandas
numpy
matplotlib.pyplot
sklearn modules for preprocessing and modeling

2️.Load Dataset                                                                                                                                                                                                     
Loaded dataset into a pandas DataFrame.
Checked dataset shape.
Verified column names and structure.

3️.Feature Selection                                                                                                                                                                                                
Selected relevant features for prediction:
Numerical Features:
sqft_living
bedrooms
bathrooms
grade
Categorical Feature:
zipcode
Target:
price

4️.Data Preprocessing                                                                                                                                                                                               
Applied StandardScaler to numerical features.
Applied OneHotEncoder to zipcode.
Used ColumnTransformer to combine preprocessing steps.
Created a Pipeline for clean workflow.

5️.Train-Test Split                                                                                                                                                                                                 
80% training data
20% testing data
random_state=42 for reproducibility

6️.Model Training                                                                                                                                                                                                   
Trained Linear Regression model.
Trained Gradient Boosting model.
Generated predictions on test data.

7️.Model Evaluation                                                                                                                                                                                                 
Used two evaluation metrics:

 MAE (Mean Absolute Error)                                                                                                                                                                                          
Average absolute difference between predicted and actual prices.

RMSE (Root Mean Squared Error)                                                                                                                                                                                      
Penalizes larger errors more heavily.
Example Results:
Linear Regression:
MAE ≈ 110,423
RMSE ≈ 195,673
Gradient Boosting:
MAE ≈ 113,350
RMSE ≈ 201,489
Linear Regression performed slightly better in this implementation.

8️.Visualization                                                                                                                                                                                                    
Created a scatter plot of:
Actual Prices vs Predicted Prices
The red dashed line represents perfect predictions.
Points closer to the line indicate better predictions.
Some dispersion indicates prediction error.

Key Results and Findings                                                                                                                                                                                            
1.The dataset is clean and well-structured.                                                                                                                                                                         
2.Living area (sqft_living) strongly influences house prices.                                                                                                                                                       
3.Location (zipcode) plays a significant role in pricing.                                                                                                                                                           
4.Linear Regression performed slightly better than Gradient Boosting in this setup.                                                                                                                                 
5.Prediction error (~$110K MAE) suggests price variability in real estate data.                                                                                                                                       

Insights                                                                                                                                                                                                            
House prices are influenced by multiple interacting features.                                                                                                                                                       
Feature scaling is essential for stable regression performance.
Categorical encoding (zipcode) improves model performance.
Real estate datasets often have large variance in prices, which increases RMSE.
Adding more features or tuning hyperparameters could improve performance further.
