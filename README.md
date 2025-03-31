Financial Fraud Dataset - Basic Pipeline 


Background 

Throughout our exploration of various supervised learning algorithms, a common theme that you all might have detected (no pun intended) is the concept of extracting some signal from a noisy dataset. 

This often applies to datasets where our class of interest (fraud, basketball upset, etc) is in the “minority” class of an imbalanced dataset. 

This problem often occurs in the detection of financial fraud. While we can assume that most transactions are credible, classifying every new sample as non-fraudulent (0) will miss every single fraudulent case. 

Within this project, we will take a look at a synthetic dataset of bank transactions to see which strategies we can take in order to successfully capture as many fraudulent transactions as possible, while also minimizing false positives. 


This dataset contains a mix of discrete and continuous variables. As you review this list of columns, consider which columns might not be relevant to your analysis:

● Step: A unit of time that represents hours in the dataset. Think of this as the timestamp of the transaction (e.g. hour 1, hour 2, … hour 534, …) 

● Type: The type of transaction 

● Amount: The amount of money transferred 

● NameOrig: The origin account name

● OldBalanceOrg: The origin accounts balance before the transaction 

● NewBalanceOrg: The origin accounts balance after the transaction 

● NameDest: The destination account name 

● OldbalanceDest: The destination accounts balance before the transaction 

● NewbalanceDest: The destination accounts balance after the transaction 

● IsFlaggedFraud: A “naive” model that simply flags a transaction as fraudulent if it is greater than 200,000 (note that this currency is not USD) 

● IsFraud: Was this simulated transaction actually fraudulent? In this case, we consider “fraud” to be a malicious transaction that aimed to transfer funds out of a victim’s bank account before the account owner could secure their information. 
Within this project, you will be creating a comprehensive machine learning pipeline that satisfies the patterned steps of a classic machine learning project. You will: 

● begin with hypothesis formulation through EDA, 

● complete data cleaning & pre-processing, 

● and conclude with model generation and a report. 


Instructions 
The following is a list of expected notebooks that should be included in your project: 

1. Initial EDA 
○ Your project should begin with a notebook where you perform univariate, bivariate, and multivariate exploratory analysis. 
○ Be sure to create relevant graphs that will help you formulate a hypothesis. 
○ Keep in mind that we are not only interested in the relationships between our predictors and our target variable, but we are also interested in the 
relationship amongst predictors. 

2. Data cleaning, wrangling & pre-processing 
○ After completing your EDA, you should move forward with creating a notebook where you will clean and wrangle your dataset. This might include dropping null values, removing unnecessary columns, removing outliers, and 
potentially fixing incorrectly formatted data. 
○ Save this dataframe as a new csv file to be used in the next step.

3. Model creation, hyperparameter search, and model evaluation 
○ Once we’ve created this pre-processed dataset, we will then create a notebook where we will create train test splits and implement a RandomForestClassifier or a GradientBoostingClassifier (the choice is yours!) 
○ After training this initial classifier and viewing its accuracy measures, we will then move forward with hyperparameter tuning via GridSearchCV or 
RandomizedSearchCV (again, the choice is yours!) 
○ Upon finding optimal hyperparameters, we should re-train our model using these hyperparameters, generate predictions for this new model, and output the subsequent F1 score for this classifier. 

4. Report 
○ To conclude this project, we should answer the following 5 questions in a separate document attached to your project: 
i. Which insights did you gain from your EDA? 
ii. How did you determine which columns to drop or keep? If your EDA informed this process, explain which insights you used to determine which columns were not needed. 
iii. Which hyperparameter tuning strategy did you use? Grid-search or random-search? Why? 
iv. How did your model's performance change after discovering optimal hyperparameters? 
v. What was your final F1 Score? 


