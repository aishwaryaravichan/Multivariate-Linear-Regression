# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.Import Pandas and the required module from Scikit-learn.
2.Read the carsemission.csv dataset.
3.Select Weight and Volume as independent variables.
4.Select CO2 as the dependent variable.
5.Create and train a Multivariate Linear Regression model.
6.Display the regression coefficients and intercept.
7.Predict the CO₂ emission for:
Weight = 3300
Volume = 1300
8.Display the predicted CO₂ emission.

## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:
<img width="1213" height="657" alt="image" src="https://github.com/user-attachments/assets/dfb1de35-069c-4738-95bd-7b5745c47309" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
