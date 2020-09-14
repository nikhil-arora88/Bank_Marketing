<<<<<<< HEAD
Motivation: In the current Covid scenario where governments around the world are slashing interest rates to all time lows to support economic growth, banks are rolling up their sleeves to retain deposits on their books. As against corporates which have more volatile liquidity positions, consumer deposits are increasing with decrease in discretionary spending. In the past few months, banks have tried to woo consumers to place deposits with them even at such low interest rates.
Across geographies, banks are digging into historical data to understand consumer behaviour to focus their marketing dollars on customers which are most likely to respond positively towards marketing campaigns. At a time where banks profitability have been severely hit, such insights are nothing less than gold.


In this project, we will study a publicly available data set from UCI’s Machine Learning repository (source: https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)to understand the factors that can help determine consumers’ probability of positive response to a Fixed Deposit (FD) marketing campaign. The data is from a campaign run by a Portuguese bank on getting new FDs from existing customers. It has various features on each customer along with a decision variable which indicates where he/she decided to place a FD during the campaign (a positive response).


Business understanding: The project relates to understanding the factors that may determine whether a client can be expected to take up a Fixed deposit during a campaign. There are many features present in the data set that can help us understand the same, of which we shall attempt to explore a few of them.

Data understanding: The data has 20 predictor variables and an output variable (y). The output variable indicates whether the client took up a FD during the campaign or not. The description of predictor variables is as below:

1 - age (numeric)
   2 - job : type of job (categorical: "admin.","blue-collar","entrepreneur","housemaid","management","retired","self-employed","services","student","technician","unemployed","unknown")
   3 - marital : marital status (categorical: "divorced","married","single","unknown"; note: "divorced" means divorced or widowed)
   4 - education (categorical: "basic.4y","basic.6y","basic.9y","high.school","illiterate","professional.course","university.degree","unknown")
   5 - default: has credit in default? (categorical: "no","yes","unknown")
   6 - housing: has housing loan? (categorical: "no","yes","unknown")
   7 - loan: has personal loan? (categorical: "no","yes","unknown")
   
   # related with the last contact of the current campaign:
   8 -	contact: contact communication type (categorical: "cellular","telephone") 
   9 - month: last contact month of year (categorical: "jan", "feb", "mar", ..., "nov", "dec")
  10 - day_of_week: last contact day of the week (categorical: "mon","tue","wed","thu","fri")
  11 - duration: last contact duration, in seconds (numeric). Important note:  this attribute highly affects the output target (e.g., if duration=0 then y="no"). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
   # other attributes:
  12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
  13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
  14 - previous: number of contacts performed before this campaign and for this client (numeric)
  15 - poutcome: outcome of the previous marketing campaign (categorical: "failure","nonexistent","success")
   # social and economic context attributes
  16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)
  17 - cons.price.idx: consumer price index - monthly indicator (numeric)     
  18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)     
  19 - euribor3m: euribor 3 month rate - daily indicator (numeric)
  20 - nr.employed: number of employees - quarterly indicator (numeric)


Data Preparation: First we do missing value treatment for overall data on the following columns at respective replacement values:

'job' : 'unemployed'
'marital' : 'single'
'education' : 'illiterate'
'default' : 'no'
'housing' : 'no'
'loan' : 'no'

For the questions where are trying to study the effect of numerical features against y, we divide the respective feature into discrete buckets using pandas cut function.

For the modelling process, we divide the data into training and test set (using sklearn's stratified sample split function) in 80:20 ratio. Next, we encode categorical variables into multiple columns (also called one hot encoding) using pandas get dummies function).


Data Modelling: First we study 3 variables - previous (number of contacts performed before this campaign and for this client), days (number of days that passed by after the client was last contacted from a previous campaign) and outcome (outcome of the previous marketing campaign) against their effect on y using visualizations. We also look at movement of 3M Euribor (an external benchmark rate) and mean conversion rate i.e. y with each month using a line graph.

In the modelling process we try multiple ML techniques - logistic regression, Random Forest, GBM and XGBoost to build a predictive model for prediction of y.


Evaluation: Results of the first few questions (prior to the modelling process) are described in detail in this blogpost: https://medium.com/@niksarster/what-banks-should-do-to-get-more-fixed-deposits-1e99bcda7aa5

The results of each model on the test test w.r.t various metrics such as accuracy, precision, recall etc. are mention in respective sections of the notebook.


Libraries Used:
pandas
numpy
os
matplotlib
seaborn
sklearn
xgboost


Files Present:
bank-additional-full.csv : Full data set with all features
bank-additional.csv : Sample data with all features
Bank_Marketing.ipynb : Analysis notebook
bank-additional-names.txt : Description of data








=======
Blog Post: https://medium.com/@niksarster/what-banks-should-do-to-get-more-fixed-deposits-1e99bcda7aa5?source=friends_link&sk=26ab7e6ac0587468ab2ed33956f80c96

In this project, we will study a publicly available data set from UCI’s Machine Learning repository (source: https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)to understand the factors that can help determine consumers’ probability of positive response to a Fixed Deposit (FD) marketing campaign. The data is from a campaign run by a Portuguese bank on getting new FDs from existing customers. It has various features on each customer along with a decision variable which indicates where he/she decided to place a FD during the campaign (a positive response).

>>>>>>> dc3b748030f97a7b387527791e76ee32e3cb40c4
