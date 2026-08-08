# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: GOPINATH S
RegisterNumber: 212225040097
*/

import pandas as pd
print("X_test:", X_test.shape)
print("y_train:", y_train.shape)
print("y_test:", y_test.shape)

# 8. Create and Train the Logistic Regression Model
# solver='liblinear' works well for small datasets
lr = LogisticRegression(solver="liblinear")

# Train the model
lr.fit(X_train, y_train)

# 9. Make Predictions on the Test Set
y_pred = lr.predict(X_test)

print("\nPredicted values (y_pred):")
print(y_pred)

# 10. Evaluate Model Performance
# Accuracy: percentage of correctly predicted labels
accuracy = accuracy_score(y_test, y_pred)
print("\nModel Accuracy:", accuracy)

# Classification Report: precision, recall, F1-score
print("\nClassification Report:")
print(classification_report(y_test, y_pred))

# 11. Predict Placement for a New Student
# Order of features must match X columns:
# ['gender', 'ssc_p', 'ssc_b', 'hsc_p', 'hsc_b', 'hsc_s',
#  'degree_p', 'degree_t', 'workex', 'etest_p', 'specialisation', 'mba_p']

# Example student data (after encoding categorical values manually)
# NOTE: These categorical numeric codes depend on how LabelEncoder encoded them.
# Here we assume:
# gender: 1 (e.g., Male)
# ssc_p: 80
# ssc_b: 1
# hsc_p: 90
# hsc_b: 1
# hsc_s: 1
# degree_p: 90
# degree_t: 1
# workex: 0 (No work experience)
# etest_p: 85
# specialisation: 1
# mba_p: 85

new_student = [[1, 80, 1, 90, 1, 1, 90, 1, 0, 85, 1, 85]]

new_prediction = lr.predict(new_student)

print("\nPrediction for new student (0 = Not Placed, 1 = Placed):")
print(new_prediction[0])
```

## Output:
<img width="380" height="604" alt="image" src="https://github.com/user-attachments/assets/02e619d0-1c4a-4be5-a2b6-49af417709b8" />

<img width="554" height="440" alt="image" src="https://github.com/user-attachments/assets/15cf7fa5-e9ab-442a-a337-ca5a3ceff490" />


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
