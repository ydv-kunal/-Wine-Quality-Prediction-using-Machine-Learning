# -Wine-Quality-Prediction-using-Machine-Learning
This project predicts the quality of wine based on its physicochemical properties (like acidity, sugar, pH, alcohol, etc.) using Machine Learning models.

## Project Overview

This project focuses on predicting the quality of wine using machine learning algorithms. The dataset contains physicochemical properties of wines (such as acidity, sugar, pH, alcohol, etc.) along with a quality score given by wine tasters.   

The goal is to classify wines into Good (quality ≥ 7) and Not Good (quality < 7) categories. This binary classification makes the model more practical and easier to evaluate compared to multi-class classification.     

##Dataset     

Source: [UCI Wine Quality Dataset From Kaggle] (https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)     

Features:     
Fixed acidity      
Volatile acidity    
Citric acid     
Residual sugar    
Chlorides    
Free sulfur dioxide    
Total sulfur dioxide    
Density    
pH    
Sulphates    
Alcohol    

Target: Wine quality (converted into binary: Good (≥7), Not Good (<7)).

## Steps in the Project
### 1) Data Preprocessing
- Loaded the dataset (winequality-red)    
- Converted the multi-class "quality" column into a binary label (Good / Not Good)     
- Split the dataset into training and testing sets
  
### 2) Model Training
- Trained three different models:       
-- Logistic Regression
-- Random Forest
-- XGBoost

### 3) Evaluation
- Compared models using accuracy, precision, recall, and F1-score (with focus on Good wines).
- Checked for overfitting (train vs test accuracy).

## Results
| Model               | Train Accuracy | Test Accuracy | F1-score (Good wines) | Recall (Good wines) | Precision (Good wines) |
| ------------------- | -------------- | ------------- | --------------------- | ------------------- | ---------------------- |
| Random Forest       | 96.3%          | 90.0%         | 0.60                  | 0.49                | 0.79                   |
| Logistic Regression | –              | 84.5%         | 0.35                  | 0.27                | 0.50                   |
| XGBoost             | –              | **91.1%**     | **0.66**              | **0.56**            | **0.81**               |

XGBoost outperformed other models, achieving the best balance of accuracy and recall for predicting good wines.

## Tech Stack
- Python 🐍
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib / Seaborn (for visualization)


## Major Key Learnings
- How to preprocess and handle imbalanced datasets.
- Difference between multi-class and binary classification.
- Model comparison and evaluation metrics beyond accuracy (precision, recall, F1).
- Overfitting detection and reduction.
