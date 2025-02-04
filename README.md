Objective of the Analysis

The main objective of this analysis is to specify the best best machine learning model and summary technique when applied to the german credit dataset "credit129" related to deciding the good and bad risk of people obtaining loans.The techniques which will be used are;
1) Decision Tree 2) Logistic Binary Regression 3) Discriminant Analysis (LDA- Linear Discriminant Analysis)

Interpretation of the dataset
![image](https://github.com/user-attachments/assets/1fce2291-926c-4e30-ba8c-031d35d49a57)
Data Transformation

In order to see the creditability of the loans the chosen continuous variables from the data set is duration of credit months, credit amount and age in years.

Then in order to see if the variables are normal or not histograms are plotted for each. It was identified that only credit amount is not normal, and therefore it is logged, in order to create a normal distributed histogram as shown in the right side:

Other two continuous variables in which the duration of the month and age in years shows a normal distribution histogram, therefore it is not logged as shown in the right side.

![image](https://github.com/user-attachments/assets/d8428b47-ea2d-4b9b-a06e-2585a01f91b5)

1. Decision Tree
   
![image](https://github.com/user-attachments/assets/21adb915-11f3-42d0-a3aa-d1b67550cc83)
Interpretation of the Decision Tree

The most significant factor to consider when analysing the creditability of a loan applicant is the “Account Balance”. If a loan applicant that has an account balance < 2.5, he/she has a greater chance of receiving a loan and is considered a good loan and if the value is > 2.5, it is considered a bad loan.

The next substantial factor to consider is the “Duration of Credit Month”. If the Duration of Credit is <= 22.5 months, the loan applicants savings accounts/bonds will be checked, if so the payment status of previous credit will be assessed. In the event where the savings account/bonds are >1.5 the status of previous credit will be checked.

Suppose the status of previous credit is >2.5, the loan application will be rejected as it is considered a bad loan with high risk and if <2.5 the savings accounts/bonds will be re-checked. If >2.5,  the loan application will be rejected and <2.5 the loan will be approved proving that it is a good loan with less risk.

Likewise, same applies to the other paths in the decision tree depending on the highs and lows of variables. Ultimately, the Creditability is analysed as 0=Good Loans and 1=Bad Loans as per the German credit data.


2. Binary Logistic Regression

Based on the outcome of the Decision Tree, the three variables mentioned below were considered for the logistic regression model;

Credit Amount- Continuous independent variable
Age in Years- Continuous independent variable
Account Balance- Categorical independent variable                                                                                 

Coefficients:
-For every one unit decrease in the Credit Amount, the Creditability of a loan applicant increases
-For every one unit increase in Age years, the  Creditability of a loan applicant increases

![image](https://github.com/user-attachments/assets/07c70b0c-0799-4b35-bfa7-36d09ae21897)


The output displayed above depicts, loan applicants under Account Balance 2,3,4 are compared to applicants fallen under Account Balance 1 which is default. It can be understood that people categorized under Account balance 2,3,4 has a lower chance of getting loans. Account balance 3 overtakes applicants under Account Balance 4 and Account balance 2 overtakes 3. Overall, the creditability of people under group 1 has the highest creditability. (Less risk= good loan). 

Wald Test 

![image](https://github.com/user-attachments/assets/39538578-5835-4017-9158-ec73343b89cc)

The overall effect on the Account balance is statistically significant. Which in other terms can be said that the overall efficiency of loan applicants falling under Account balance 2,3,4 are analysed and it has an impact on the Creditability![image]
Wald Test (for the different groups of people under Account balance, e.g. Account balance 3 and 4)

![image](https://github.com/user-attachments/assets/bffcd584-cbbc-46a0-b262-90e867047745)
The difference between the coefficient of Account balance 3 and that of Account balance 4 is statistically significant. Meaning it is studying the contrast between Account balance 3 & 4 and proves that its different.

Odds Ratio Output & Interpretation

![image](https://github.com/user-attachments/assets/55f43138-9ba1-444e-b9bc-ecd0a3c50a1f)

The above output displays that for every one unit increase in the Age in years, the odds of creditability (chance of receiving a loan) increase by 1.01.

The reason why the Odds ratio is needed is for the plot and to see the impact of the Credit Amount and the Account balances on the Creditability

Predicted Probabilities

![image](https://github.com/user-attachments/assets/b1bd5927-7610-4c7f-9946-d32627104fbf)

The above plot signifies that the loan applicants falling under the category-Account Balance 4 has the lowest probability of receiving a loan and they are considered as applicants with high risk = bad loans. On the other hand, the loan applicants under the category-Account Balance 1 has a high probability of receiving a loan and they are categorized as less risk = good loans as per the predicted probabilities.

Generally, loan applicants that has a higher account balance and lesser credit amount has the least chance receiving a loan (High risk) and an applicant that has a higher credit amount and lesser account balance has a high chance of getting a loan ( Less Risk).

3. Discriminant Analysis (LDA- Linear Discriminant Analysis)
   
![image](https://github.com/user-attachments/assets/5bd2ba5c-9966-428a-a2e3-134267b2cfd9)

The summary statistics signifies that the data is misclassified. 

![image](https://github.com/user-attachments/assets/3e69b20e-77ea-4fa0-9180-b97771e3d57f)

The large coefficients indicate the importance (in absolute value).

All variables are not used. So it is difficult to interpret the linear discriminants. 

![image](https://github.com/user-attachments/assets/09e30e22-7b05-4bb4-8215-87eb5ba200b3)

The output of the results displayed above depicts that 652 out of 900 loan applications are correctly classified at a percentage of 72.4%.

However, the accuracy of the model is very low.

![image](https://github.com/user-attachments/assets/7ae32627-78c8-443e-a9b3-f91d323e2d6f)


Conclusion

The German Credit dataset has been modelled using three supervised learning methodologies which are decision tree- classification tree, Logistic Regression Model and Discriminant Analysis. 

The Logistic Regression model requires all continuous & categorical variables to be analysed. It is difficult to analyse all the variables with the nature of the logistics regression model.

The Discriminant Analysis requires all categorical variables to be analysed. The reason why this technique will not do well is because most of the variables are categorical and continuous variables are not considered in this analysis. And also with a lot of variables it is too much to be analysed through the discriminant analysis. So the accuracy of the output will be low. 

Given the circumstances, it can be understood that the Decision Tree Method seems to be working better on this dataset compared to the Logistic Regression Model & Discriminant Analysis. It is easy to analyse and interpret the data in a Decision Tree as it can accommodate all the variables.



