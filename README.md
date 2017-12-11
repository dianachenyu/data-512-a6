# A6: Final project report
# User Churn Prediction
## Project Goal
In this project, we use machine learning models to identify customers who are likely to stop using telecommunication service in the future. Furthermore, we will analyze top factors that influence user retention. 

## Motivation
Motivation of the study is to find if we can predict user behaviors and check the accuracy of prediction. The second motivation is to understand the reasons behind users' behaviors. In the future, service providers can use the results to improve their service, attract and retain more customers to stay in the business.

## Research Questions
* Question 1: For a specific user X, is this user going to continue use the service in the next month? What about in the next three months? What about in the next six months?
* Question 2: What are the top factors affecting users' decision to continue using the service or not?

## Hypothesis
* Hypothesis 1: we can use past user behaviors to predict future user churn decision on cell phone plan usage.
* Hypothesis 2: users with similar characteristics (e.g. gender, age, location) will have similar behaviors when using the service. So that we can use data from some users to predict other the behavior of similar users.

## Data Source and Data License
Data is from [UIC machine learning repository](https://archive.ics.uci.edu/ml/datasets.html).

There are four [churn datasets](https://www.sgi.com/tech/mlc/db/). Multiple datasets are used in the project. There are 21 variables in the main dataset. Some variables are as following: 

| Variable Name | Type          | Meaning  						    |
| :-----------: |:-------------:| :----------------------------:    |
| state	        | categorical 	| abbreviation of US state e.g. WA  | 
| area_code     | continuous    | area code in three digit e.g. 206	|
| accout_lenth  | continuous  	| how long the users have using the service; unit unkown 	|
| phone_num     | continuous  	| phone number without area code 	|
| intl_plan     | binary	| if the user has international plan	|
| voice_mail_plan  | binary 	| if the user has voice mail plan 	|
| number_vmail_messages  | continuous	|number of voice messages	|
| total_day_minutes	 | continuous	|total of day minutes	|
| total_day_calls    | continuous	|count of day calls     |
| total_day_charge   | continuous	|total of day charge	|





UCI dataset is a part of Open Science and, specifically, Open Data program. The churn dataset uses [Open Data Commons Open Database License (ODbL)](https://en.wikipedia.org/wiki/Open_Database_License)


## Analytical Methods and Process
### Analytical Methods 
The main methods used in the project is Data Analysis and Machine Learning.

In the Data Analysis process, Exploratory Data Analysis (EDA), Data Cleaning, and Data Manipulation are used. In the Machine Learning modeling process, linear regression, Logistic regression, K-nearest neighbor (k-NN), Random Forest algorithms are used. Grid Search are used to find optimal parameters. Recursive Feature Elimination (RFE) are used in feature selection.

### Analytical Process
The analytical process is planed as follow:

* Step 1: Data Exploration
* Step 2: Feature Preprocessing
* Step 3: Model Training and Results Evaluation
* Step 4: Feature Selection and Tuning
* Step 5: Conclusion

Step 1: the purpose of this step is to understand the dataset and clean messy data. To understand the dataset, the plan is to take a slice of data and simply examine the values; also various data visualizations are used, for example, scatter plot and box plot, to check data distribution. To clean messy data, the step checks missing data, identify outliers, and manually split, combine, and change some data field.

Step 2: because there are categorical features in the dataset, step 2 includes labelling categorical variables, maybe using one hot encoding. There are also some fields does not sound related to the output. An analysis will be needed if include the fields or not in the model. Transformation of these fields may be useful. Lastly, scaling features to normal is needed before feeding the features into the model.

Step 3: this is the most important of the model. I started with the simple linear regression, and then try Logistic regression, K-nearest neighbor (k-NN), and Random Forest algorithms. I evaluated the results using Confusion Matrix.

Step 4: in this step, I tuned model parameters and select features. Feature importance are also calculated, and then be used to answer the second research question, which factors are influential on user decisions.

Step 5: this step including discussion of the model and make a conclusion. This is a more qualitative step and focuses on making sense out of the model. Human-centered factors are also be analyzed and discussed in this step. 

## Limitations and Unknowns
### Validity of the dataset
The Customer churn data is commonly used machine learning dataset. The data files state that the data are "artificial based on claims similar to real world". Little is known on how the dataset is simulated/collected and processed. The representativeness and validity of the dataset needs a further analysis.

### Size of the Dataset
There are 5000 observations in the main churn dataset. It is not a huge dataset. The size needs to be taken into consideration in avoid of overfitting or too complicated model.


### Potential Additional Datasets
Due to the discussion above, it may be useful to include additional datasets into the study. These datasets could be similar data from sources with more information on the background, a larger dataset, or dataset which can provides additional features. 


## Human-centered Aspects
I consider the project as a human-centered data analysis on human produced data but without a direct contact with human. Combing the quantitative analysis methods (data analysis and machine learning) with some qualitative studies, like survey with telecommunication service users, would be optimal. Especially one purpose of the study is to understand service users, and figure out why they would continue using the service or not. What would be more straight forward than asking the users' opinions?

Unfortunately, interview with users is out of the scope of the final project. Instead, I will try to include more human factors into the analysis. It includes an emphasis on the interpretability of models and process instead of only focus on the model evaluation results.


## References 
[UW HCDS Class](https://wiki.communitydata.cc/HCDS_(Fall_2017))

[Assignment 3](https://wiki.communitydata.cc/HCDS_(Fall_2017)/Assignments)

[Definition of Customer Churn](https://en.wikipedia.org/wiki/Customer_attrition)

Some inspiring User Churn Studies:

[A Meta-Analysis of Churn Studies](https://medium.com/the-saas-growth-blog/a-meta-analysis-of-churn-studies-4269b3c725f6)

[9 Case Studies That’ll Help You Reduce SaaS Churn](https://conversionxl.com/blog/reduce-churn/)

[The World's Largest Study on SaaS Churn](https://blog.profitwell.com/saas-churn-benchmarks-mrr-churn-study)

[40 Customer Retention Statistics You Need to Know](https://www.getfeedback.com/blog/40-stats-churn-customer-satisfaction/)
