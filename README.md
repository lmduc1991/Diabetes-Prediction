# Diabetes-Prediction

<img src=https://scitechdaily.com/images/Diabetes-Treatments.jpg>

### **Project Overview**

In this project, the goal is to construct a **logistic regression model** and build **Tree-based machine learning models** to predict diabetes in patients based on their medical history and demographic information. Based on **XGBoost model**, Hemoglobin A1c, amount of glucose in the patient's bloodstream, their weight class according to BMI, patient's age and patient's hypertension status are the most important features to predict if patient is in risk of developing diabetes.

### **Business Understanding**

Hemoglobin A1c usually is the most important index to determine if patient is in diabetes risk. However, it doesn't mean that patient have Hemoglobin A1c classified as diabetes would have diabetes. It is important to understand beside this, what factors involve in predicting if patient can get diabetes.

### **Data Understanding**

**The Diabetes prediction dataset** is a collection of medical and demographic data from patients, along with their diabetes status (positive or negative). The dataset can be retrieved from [kaggle website](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset/data). The data contains 100,000 observations which has many of duplication and 9 variables. During feature engineering, some variables were transform and values were removed in order to fit the data at its best. Data columns detail is explained below:

        1. gender                   biology sex of patient
        2. age                      age of patient
        3. hypertension             medical condition in which the blood pressure in the ateries is persistently elevated [0:No - 1:Yes]
        4. heart-disease            if patient has heart disease [0:No - 1:Yes]
        5. smoking_history          smoking status of patients
        6. bmi                      body mass index
        7. HbA1c_level              Hemoglobin A1c - measure of patient's blood sugar level over the past 2-3 months.
        8. blood_glucose_level      amount of glucose in the patient's bloodstream
        9. diabetes                 if patient has diabetes [0:No - 1:Yes]

The target variable `diabetes` is imbalanced and needed to be upsampled during model constructing to get better scores.

### **Modeling and Evaluation**

a **logistic regression model** achieved precision of 94%, recall of 85%, f1 score of 88% (all weighted averages), and accuracy of 85%, on the test set. While **XGBoost model** outperforms **decision tree model** and **random forest model**, yielded 33% of precision, 95% of recall, 49% of f1 score and 83% of accuracy on test set.


### **Conclusion**

Either logistics regression model or XGBoost model, they all are great model to predict patients who are in risk of developing diabetes. It should be a good idea to test the model with selected group of patients in real work to get feedback.


