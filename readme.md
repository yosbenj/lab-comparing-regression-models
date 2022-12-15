![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Comparing regression models


For this lab, we will be using the same dataset we used in the previous labs. Load the cleaned categorical and numerical dataframes that you saved at the end of Monday's labs.

### Instructions

Concatenate Numerical and Categorical dataframes into one dataframe called data.

1. In this final lab, we will model our data. Import sklearn `train_test_split` and separate the data.

2. Separate X_train and X_test into numerical and categorical (X_train_cat , X_train_num , X_test_cat , X_test_num)

2. Use X_train_num to fit scalers.  Transform BOTH X_train_num and X_test_num.

5. Encode the categorical variables X_train_cat and X_test_cat (See the hint below for encoding categorical data!!!)

6. The time variable can be useful. Try to transform its data into a useful one. Hint: Day week and month as integers might be useful.

7. Since the model will only accept numerical data, check and make sure that every column is numerical, if some are not, change it using encoding.


## Hint for Categorical Variables

You should deal with the categorical variables as shown below (for ordinal encoding, dummy code has been provided as well):
Encoder Type | Column 
-----------------|-----------------
One hot | state
Ordinal | coverage
Ordinal | employmentstatus
Ordinal | location code
One hot | marital status
One hot | policy type
One hot | policy
One hot | renew offercustomer_df
One hot | sales channel
One hot | vehicle class
Ordinal | vehicle size

### Dummy code

data["coverage"] = data["coverage"].map({"Basic" : 0, "Extended" : 1, "Premium" : 2})

given that column "coverage" in the dataframe "data" has three categories:

"basic", "extended", and "premium" and values are to be represented in the same order.



8. Try a simple linear regression with all the data to see whether we are getting good results.

9. Great! Now define a function that takes a list of models and train (and tests) them so we can try a lot of them without repeating code.

10. Use the function to check `LinearRegressor` and `KNeighborsRegressor`.

11. You can check also the `MLPRegressor` for this task!

12. Check and discuss the results.
