# Waze_user_churn_project
Project done through Google's Advance Data Analytics to build machine learning models to predict user churn. 
Waze User Churn Project

Overview

The goal of this project was to analyze the data and create logistic regression, random forest, and XGBoost models to predict if a user will churn or not. This project utilized Waze's user data, given by the course. The final models did not score well enough to have confidence in their predictive powers. The binomial regression model had a 9% recall score to predict if a user will churn, meaning it will fail to predict if a user will churn. The random forest and XGBoost models had slightly better recall scores and scored similarly. However, the XGBoost model performed better based on the F1 score. These models would serve better for further understanding user churn relationships and should not be used to predict user churn. Based on the XGBoost model, km per hour, days after onboarding, and total sessions in the last month were the top 3 most influential factors in determining whether a user will churn or not. 

Business Understanding 

Waze is a navigation app that lets its users highlight potential risks on the road that can warn other nearby users. Since Waze is so community-driven, retaining as many users as possible is necessary to keep that flood of information about what is happening on the roads. If Waze can pinpoint areas where they can improve or find what type of users are more likely to churn, they can use that information to make their app better for those users. 

Data Understanding 

Explain what data you used in your analysis, the timeframe of the data, and any data limitations. This is also a good section to add visualizations of your exploratory data analysis. 

The Waze user data was supplied by the course. The data consists of 14999 users and 13 features. The features included in this data were: ID, label, sessions, drives, total_sessions, n_days_after_onboarding, total_navigations_fav1,  total_navigations_fav2, driven_km_drives 14999, duration_minutes_drives, activity_days, driving_days, and device. About 82.26% of the data was retained by users, and 17.74% was churned users. 

Modeling and Evaluation 

Binomial logistic Regression Model:
This model had decent precision scores, but with a 9% recall score for users, churn does not make this a viable model to be used for predictions. This model weighed activity days the heaviest in its prediction, with a negative correlation to user churn.
![image](https://github.com/landgrd/Waze_user_churn_project/assets/94145969/efef521f-1da8-45e9-8c6a-422f9e7ce652)

Random Forest Model:
This model has scores of 44% precision, 12% recall, .18 F1, and 81% accuracy. These scores are not high enough to have confidence that this model can predict user churn. 

XGBoost model:
This model has scores of 43% precision, 16% recall, .23 F1, and 81% accuracy. These scores, being better than the random forest model and the logistic model, are not high enough to have confidence that this model can predict user churn. This model weighted km per hour heaviest in its prediction of user churn.
![image](https://github.com/landgrd/Waze_user_churn_project/assets/94145969/59bc18b0-c78a-4d4a-a5e1-83d6d07f6134)

Conclusion
As these models do not have the power to predict if a user will churn, they gave insight into what type of user will be most likely to churn. Having more information on the users concerning how they use the app could make these models perform better and find more relationships. 
