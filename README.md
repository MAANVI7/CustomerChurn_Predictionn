# CustomerChurn_Predictionn
Customer churn rate is a measure of the proportion of individuals or items moving out of a group over a specific period. It is one of two primary factors that determine the steady-state level of customers a business will support. Churn is widely applied in business for contractual customer bases.
For EDA, please refer to: EDA-Churn Analysis.ipynb
For Model Building, please refer to: Model-Customer Churn.ipynb
Steps followed for project
1.	Dataset Info: Sample Data Set containing customer data for an internet service provider company, and showing how long the customers have used their subscription.
2.	Information present in dataset: CustomerID, Name, Age, Gender, Location, Subscription length, Monthly Bill, Total Usage of Data, Churn.
3.	Checking the various attributes of data like shape (rows and cols), Columns, datatypes
4.	 Checking the descriptive statistics of numeric variables.
Inference: 
	Churn is actually a categorical hence the 25%-50%-75% distribution is not propoer.
	75% customers have subscription length less than 19 months.
	Average Monthly Bill is USD 65.05 whereas 75% customers pay more than USD 82.64 per month
	Average data usage is 274.39 GB
	CustomerID statistics are insignificant here.
	The average age of the customers is 44 years whereas 75% of the people are above 57 years age
5.	Checking if data is balanced or not.
 6.	Checking for missing values of data. 
 7.	Data cleaning- 
	Making a copy of original dataset.
	Ensuring no missing data is there. 
	Converting monthly bill into numeric amount.
	Making bins of Age group and Subscription duration. 
	Removing columns not required for processing further such as Name and customer ID. 
8.	Data Exploration-
	Plot distribution of individual predictors by churn
  	Convert all the categorical variables such as location, gender into dummy variables
	Relation of monthly bill with churn- No relation found.
	Relation of monthly GB usage with churn- No relation found.
	Correlation of all variables with churn- No correlation found.
9.	Bivaraiate analysis. 
  
 Conclusion 
1.People having longer subscription duration have high churn rates specially females. 
2. People in the age group below 21 years have very low churn rate. 
3. Miami has high churn rate compared to other places.

Model for Prediction
1.	Importing necessary libraries. 
2.	Reading data.
3.	Applying min_max normalization on Monthly_Bill and Total_Usage_GB.
4.	Train Test splitting- Splitting data in ratio of 80%-20%.
5.	Evaluation using Decision Tree Classifier.
Classification Report: accuracy-0.50 
precision    recall f1-score   support
6.	Using pruning methods and Grid Search CV for optimization of DT classifier.
No improvement in parameters seen. 
7.	Random forest classifier
   Classification Report: accuracy-0.50
8.	Performing Principal Component Analysis 
Classification Report: accuracy-0.50
9.	Applying ANN
Classification Report: accuracy-0.50
With DT, PCA &ANN, we couldn't see any better results, hence let's finalise the model which was created by Random Forest Classifier, and save the model so that we can use it in a later stage. 

