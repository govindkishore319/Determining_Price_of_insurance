# Determining_Price_of_insurance
Analyse the factors that determine the charges of the insurance. Can you predict the price of the insurance?

Insights from the data:
The dataset consists of 1338 * 7 and has no null values. It comprises of numerical variables such as age, bmi, charges and categorical features such as sex, children, smoker and region.

Exploratory Data Analysis:

UNIVARIATE ANALYSIS

- Age column is left skewed. So applying the log to convert into normal distribution.
- Sex feature is almost evenly distributed between male and female
- BMI is a numerical variable. Categorising BMI into underweight, healthy, overweight and obesity. We found only 16.6% od the customers are healthy. Thus, it seems that this feature is going to play a role in determining price.
- Number of Children varies from 0 to 5.
- variable Charge also is right skewed. This is our target variable.
- Distribution of customers across regions like Northwest, Northeast, Southwest and Southeast. Soutwest region is densely populated.
- 247 people smoke and 1047 don't.
MULTIVARIATE ANALYSIS

- Higher charges to be paid by the smokers 
- People with children tend to have higher medical costs overall as well.
- As we can see from these barplots the highest charges due to smoking are still in the Southeast but the lowest are in the Northeast
- Charges are based on the healthy status of the customers. Obese customers pay higher charges.
- Smoking has the highest impact on medical costs, even though the costs are growing with age, bmi and children. Also people who have children generally smoke less, which the following violinplots shows too
CORRELATION MATRIX

- Smoking came out to be the most important featur in determining the charges. (correlation- 0.79)
MODEL BUILDING

 Choosing Linear regression to be our model since assumptions are justified.
         - variables are normally distributed
         - No sign of multicollinearity
         - no heteroscedasticity
         - no auto correlation
EVALUATING LINEAR REGRESSION MODEL

Metrics: MAE: 3990.2503849796185, MSE: 33530131.141361613, RMSE: 5790.520800529224

R square: 76%. Very good model accuracy.

Coefficients of the model :

              age    241.214356
              sex    65.157046
              bmi    364.764764
              children    498.862812
              smoker    23440.629389
              region    -340.606493
CONCLUSION

Smoking is the most important feature in determining the charges. After this, children, BMI and age play a role.
