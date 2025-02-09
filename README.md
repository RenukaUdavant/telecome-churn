
# Telecom Churn Prediction

### Business Problem Overview

In the telecom industry, customers are able to choose from many service providers and actively switch from one operator to another. In this highly competitive market, the telecoms industry has an average yearly turnover rate of 15-25%. Given that it costs 5-10 times more to acquire a new customer than to maintain an existing one, customer retention has taken precedence over customer acquisition.

Retaining profitable customers is the primary business goal for many existing operators.

To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.

### Definitions of Churn
There are various ways to define churn, such as:

Revenue-based churn: Customers that have not used any revenue-generating services, including mobile internet, outgoing calls, SMS, etc., over a given period of time. Aggregate metrics like "customers who have generated less than INR 4 per month in total/average/median revenue" could also be used.



This definition's primary flaw is that some customers merely get calls or SMS messages from their wage-earning peers; in other words, they use the services without making any money. For instance, a large number of rural users only get calls from their metropolitan siblings who earn a living.



Usage-based churn: Customers who have not done any usage, either incoming or outgoing - in terms of calls, internet etc. over a period of time.



One potential limitation of this concept is that if the customer has stopped using the services for an extended period of time, it may be too late to take any corrective action to keep them. Predicting churn, for instance, could be pointless if you base it on a "two-months zero usage" period because the client would have already moved to a different operator by then.

#### In this project, usage-based  is used to define churn.

### High-value Churn
About 80% of revenue in the Indian and Southeast Asian markets originates from the top 20% of consumers, also referred to as high-value clients. Thus, if we can reduce churn of the high-value customers, we will be able to reduce significant revenue leakage.


### Understanding the Business Objective and the Data
The dataset contains customer-level information for a span of four consecutive months - June to September. The months are encoded as 6, to 9, respectively.


The objective of the company is to use the data (features) from the first three months to predict the churn in the last month, or the ninth month. Understanding typical customer behavior during churn will help you complete this work successfully.



### Understanding Customer Behaviour During Churn
Customers usually do not decide to switch to another competitor instantly, but rather over a period of time (this is especially applicable to high-value customers). In churn prediction, we assume that there are three phases of customer lifecycle :

The ‘good’ phase: In this phase, the customer is happy with the service and behaves as usual.

The ‘action’ phase: The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a  competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour than the ‘good’ months. Also, it is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)

The ‘churn’ phase: In this phase, the customer is said to have churned. You define churn based on this phase. Also, it is important to note that at the time of prediction (i.e. the action months), this data is not available to you for prediction. Thus, after tagging churn as 1/0 based on this phase, you discard all data corresponding to this phase.



In this case, over a four-month window, the first two months are the ‘good’ phase, the third month is the ‘action’ phase, while the fourth month is the ‘churn’ phase.


### Modelling
The predictive model  will serve two purposes:

* It will be used to predict whether a high-value customer will churn or not, in near future (i.e. churn phase). By knowing this, the company can take action steps such as providing special plans, discounts on recharge etc.

* It will be used to identify important variables that are strong predictors of churn. These variables may also indicate why customers choose to switch to other networks.


### Steps performed to build the model:
1. Process data (convert columns to appropriate formats, handle missing values, etc.)

2. Conduct  exploratory analysis to extract useful insights (whether directly useful for business or for eventual modelling/feature engineering).

3. Derive new features.

4. Reduce the number of variables using PCA.

5. Train a variety of models, tune model hyperparameters, etc.

6. Evaluate the models using appropriate evaluation metrics. .

7. Finally, choose a model based on  evaluation metric.
8. Build another model with the main objective of identifying important predictor attributes which help the business understand indicators of churn.

