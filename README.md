# Test
1)	Objective: This project is to find the customers whom a company should approach to increase the sales of ‘ABC’ product.

2)	Meta Data: from the given ‘DS_Dataset.csv’
Independent Variables:
Customer_ID, Var1,Var2, Group(8 groups,G1,G2...G8),Category(C1,C2..C5), Rating(rating of a customer) and output variable ‘Purchased_ABC_product’
3)	EDA Process: Performed data cleaning on dataset
i.	Removed Customer_ID column since it is not a important variable model in training.
ii.	Checking for null values and 
iii.	Basic statistical values of given variables of all 4 business moments.
iv.	Pre-processing categorical data into numerical data, categorical variable to actual values and creating dummy variables
v.	Visualizing Heat map and Scatter plots for numerical data

4)	Train and Test splitting the data

5)	Feature selection: Using extra tree classifier we found out  the variables Var1,Var2 and Rating are influencing the purchase of product ABC. 

6)	Building a Model: Testing different classification algorithms on data to find out better performing algorithm. We found out xgboost was giving better results compared  to other algorithms.

7)	Hyper parameter tuning the XGBoost model

8)	Evaluating the results: based on confusion matrix out of all customers bought ABC_product, the model has predicted correctly 82%

9)	Checking the real time predictions on model

      10)  SHAP : Performed SHAP analysis on trained model: from summary plot
•	The y-axis indicates the variable name, in order of importance from top to bottom. The value next to them is the mean SHAP value.
•	On the x-axis is the SHAP value. Indicates how much is the change in log-odds. From this number we can extract the probability of success

 
We can see that Var2,Category_C5, var1 and Rating are important variables influencing  model.

10)	Understandings : The variables var1,var2, Category 5 and Rating are highly influencing the customer to buy a ABC product. we built trained XGBoost model and found the customer who have  higher probability of purchasing a ABC product have high var2,Category_C5 and gold rating and also customer with bronze rating has very less probability rate of purchasing a product. So the company should focus on the group of customers where there is high probability of purchasing a ABC product to increase sales.


