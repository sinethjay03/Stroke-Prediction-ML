
# Stroke Prediction Using Machine Learning

## Project Overview
This project focuses on predicting the likelihood of stroke using machine learning classification algorithms. The objective is to compare different machine learning models and investigate techniques to improve prediction performance, particularly when dealing with an imbalanced dataset.

This project was completed as an individual academic project for the Statistical and Machine Learning module at the University of Moratuwa.

## Dataset
The project uses the Stroke Prediction Dataset.

- Total records: 5,110
- Predictive features: 10
- Target variable: Stroke
- Stroke cases: 249 (4.87%)
- Non-stroke cases: 4,861 (95.13%)
- Missing BMI values: 201

The dataset contains demographic, health-related, and lifestyle features such as age, gender, hypertension, heart disease, average glucose level, BMI, smoking status, and work type.

### Dataset Source
The dataset used in this project was obtained from Kaggle.

- Dataset: Stroke Prediction Dataset
- Source: [Kaggle – Stroke Prediction Dataset] (https://www.kaggle.com/datasets/fedesoriano/
stroke-prediction-dataset))

## Machine Learning Models
Five classification algorithms were implemented and evaluated:

1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. Support Vector Machine (SVM)
5. K-Nearest Neighbours (KNN)

## Techniques Applied
Several techniques were investigated to improve model performance:

- Random Oversampling to address class imbalance.
- Class Weighting as an alternative imbalance-handling technique.
- Stratified 5-Fold Cross-Validation for more reliable model evaluation.
- RandomizedSearchCV for hyperparameter tuning.
- Threshold Optimization to improve stroke detection.

Oversampling was applied only within the training folds to prevent data leakage.

## Evaluation
Model performance was assessed using metrics suitable for imbalanced classification problems, with particular attention to Average Precision, precision, recall, and accuracy.

Accuracy alone can be misleading when the target classes are highly imbalanced.

## Key Findings
- The dataset showed a significant class imbalance, with stroke cases representing only 4.87% of observations.
- Initial models achieved relatively high accuracy but showed poor recall for stroke cases.
- Gradient Boosting with Random Oversampling achieved the highest cross-validation Average Precision of 0.1962 before hyperparameter tuning.
- After tuning, the Average Precision increased to 0.2073.
- Threshold optimization increased test recall from 0.76 to 0.80 by reducing the classification threshold from 0.50 to 0.42.
- Age, average glucose level, and BMI were among the most influential features in the Gradient Boosting model.

Feature importance indicates predictive contribution within the model and does not establish causation.

## Tools and Technologies
- Python
- Jupyter Notebook / Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Limitations
- The dataset contains a relatively small number of stroke cases.
- Improving recall may increase false positive predictions.
- External validation using independent datasets was not performed.
- The models are developed for academic purposes and are not intended for clinical diagnosis.

## Author
**Sineth Jayasooriya**

Business Analytics Undergraduate  
University of Moratuwa

---

*This project is intended for educational and academic purposes only.*
