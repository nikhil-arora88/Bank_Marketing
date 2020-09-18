
Motivation: In the current Covid scenario where governments around the world are slashing interest rates to all time lows to support economic growth, banks are rolling up their sleeves to retain deposits on their books. As against corporates which have more volatile liquidity positions, consumer deposits are increasing with decrease in discretionary spending. In the past few months, banks have tried to woo consumers to place deposits with them even at such low interest rates.
Across geographies, banks are digging into historical data to understand consumer behaviour to focus their marketing dollars on customers which are most likely to respond positively towards marketing campaigns. At a time where banks profitability have been severely hit, such insights are nothing less than gold.


In this project, we will study a publicly available data set from UCI’s Machine Learning repository (source: https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)to understand the factors that can help determine consumers’ probability of positive response to a Fixed Deposit (FD) marketing campaign. The data is from a campaign run by a Portuguese bank on getting new FDs from existing customers. It has various features on each customer along with a decision variable which indicates where he/she decided to place a FD during the campaign (a positive response).


Business understanding: The project relates to understanding the factors that may determine whether a client can be expected to take up a Fixed deposit during a campaign. There are many features present in the data set that can help us understand the same, of which we shall attempt to explore a few of them.

Data understanding: The data has 20 predictor variables and an output variable (y). The output variable indicates whether the client took up a FD during the campaign or not. The description of predictor variables is provided in bank-additional-names.txt file


Data Modelling: First we study 3 variables - previous (number of contacts performed before this campaign and for this client), days (number of days that passed by after the client was last contacted from a previous campaign) and outcome (outcome of the previous marketing campaign) against their effect on y using visualizations. We also look at movement of 3M Euribor (an external benchmark rate) and mean conversion rate i.e. y with each month using a line graph.



Evaluation: Results of the first few questions (prior to the modelling process) are described in detail in this blogpost: https://medium.com/@niksarster/what-banks-should-do-to-get-more-fixed-deposits-1e99bcda7aa5

The results of each model on the test test w.r.t various metrics such as accuracy, precision, recall etc. are mention in respective sections of the notebook.


Additional steps: In the modelling process we try multiple ML techniques - logistic regression, Random Forest, GBM and XGBoost to build a predictive model for prediction of y.

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
Bank_Marketing_v2.ipynb : Analysis notebook
bank-additional-names.txt : Description of data
