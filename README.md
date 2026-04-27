# SGD-Regressor-for-Multivariate-Linear-Regression

## AIM:
To write a program to predict the price of the house and number of occupants in the house with SGD regressor.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Read the dataset using pandas and remove unwanted spaces from column names.

Step 2: Select input features (Size, Bedrooms) and output values (Price, Occupants).

Step 3: Normalize the input data and train two separate SGD regression models.

Step 4: Get user input (size and bedrooms) and predict the price and number of occupants.
## Program:
```
/*
Program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor.
Developed by: THULEER R
RegisterNumber: 212225230285
import pandas as pd
from sklearn.linear_model import SGDRegressor
from sklearn.preprocessing import StandardScaler
data = pd.read_csv("house.csv")
print(data.columns)
data.columns = data.columns.str.strip()
X = data[['Size', 'Bedrooms']]
y_price = data['Price']
y_occ = data['Occupants']
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
price_model = SGDRegressor(max_iter=1000, learning_rate='constant', eta0=0.01)
occ_model = SGDRegressor(max_iter=1000, learning_rate='constant', eta0=0.01)
price_model.fit(X_scaled, y_price)
occ_model.fit(X_scaled, y_occ)
size = float(input("Enter house size: "))
bed = int(input("Enter number of bedrooms: "))
new_data = scaler.transform([[size, bed]])
pred_price = price_model.predict(new_data)
pred_occ = occ_model.predict(new_data)
print("Predicted Price:", pred_price[0])
print("Predicted Occupants:", round(pred_occ[0]))
*/
```

## Output:
<img width="408" height="86" alt="Screenshot 2026-04-27 091238" src="https://github.com/user-attachments/assets/290b5ff8-79b6-4baf-9744-cda170158b11" />


## Result:
Thus the program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor is written and verified using python programming.
