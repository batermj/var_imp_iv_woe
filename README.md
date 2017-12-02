# var_imp_iv_woe
Variable Importance Using Information Value &amp; Weight of Evidence

Disclaimer: This code snippet is developed with an intension for generic use only. I hereby declare that the code was not part of any of my professional development work. Also, no sensitive or confidential data sources are used for this development.

Description: This is a code for Variable Importance based on Weight of Evidence and Information Value. The user defined function takes following input parameters:
1.	Training Data Set
2.	Testing Data Set
3.	Dependent Variable name as Character
4.	No of bins to be created on dependent variable (ideally 10)

The script will produce Information value and Weight of Evidence for each independent variable with respect to the dependent variable. Using IV value user can gauge the relative importance of each independent variable in a typical binary classification problem. Also, WOE can be used for variable transformation like binning (for continuous independent variable) and banding (for categorical independent variable).

Note:
1.	The script can be used only for binary classification problem. 
2.	Training and Testing data must have target variable populated as binary numeric (i.e. either 0 or 1. No other format is permissible) and all other variables should be either numeric, integer or factor data type. Both the data set should have identical variables.
3.	The output of this user defined function will be a list. First element of the list is IV Table and second element of the list is WOE table. User need to extract these tables manually from the list.

Steps For Execution:
1.	Copy the code file to the current working directory of R session.
2.	Import the data in to a R data frame (df_name). Kindly ensure categorical variables are stored as factor data type. Target variable should be populated as binary numeric i.e. either 0 or 1. No other format is permissible.
3.	Load the code file using below command: source(“Variable Importance Using WOE And IV.R”)
4.	Execute the code using below command: list_var_imp <- woe_iv_function(df_train,df_test, "y", 10) Third Parameter is name of the dependent variable as character string and fourth parameter is the no of bins to be created on dependent variable (ideally 10).

Compatibility: The code is developed and tested on RStudio (Version 1.0.44) using R-3.3.2

