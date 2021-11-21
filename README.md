# Jobathon-Nov-AnalyticsVidhya

Problem Statement
You are working as a data scientist with HR Department of a large insurance company focused on sales team attrition. Insurance sales teams help insurance companies generate new business by contacting potential customers and selling one or more types of insurance. The department generally sees high attrition and thus staffing becomes a crucial aspect.

To aid staffing, you are provided with the monthly information for a segment of employees for 2016 and 2017 and tasked to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not, given:

Demographics of the employee (city, age, gender etc.)
Tenure information (joining date, Last Date)
Historical data regarding the performance of the employee (Quarterly rating, Monthly business acquired, designation, salary)

**Public Leaderboard Rank - 305**

# Approach

Dataset:

![alt text](https://github.com/itsravneet/Jobathon-Nov-AnalyticsVidhya/blob/main/TrainImage.png?raw=true)

# Target Variable
In this problem, we have to predict if the employee will leave the company or not in coming 180 days by given these features. The target variable is not given as it is in dataset, so I have made a target variable by grouping the dataset by group by Emp_ID and checking if the person has left in future 180 days. 

# Feature Engineering
Made features like how much days of experience the person has in the company, previous month business value, previous month salary. LabelEncoded the Gender, City and Education Level. So, now the final dataset will have 12 features and target variable.

# Model Building
Neural Network is used with loss of binary_crossentropy and metric as f1_score and fitted on the data till the validation loss becomes low as 3.05. Also tried Random Forest Classifier with GridSearchCV and fitted on the data. I got highest f1 score of 0.70 in neural network and selected this model.

Public Score of 0.535

Skillset score: 22/30 
