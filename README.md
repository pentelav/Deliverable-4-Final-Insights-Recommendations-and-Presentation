# Deliverable-4-Final-Insights-Recommendations-and-Presentation

## Predicting Customer Churn with Data Mining Techniques

### Project Overview

Customer churn prediction is one of the important applications of data mining in the telecom sector. Lost customers can have a detrimental impact on revenue, profit and business growth. The aim of this project is to analyze customer behaviour with the help of regression, classification, clustering and association rule mining to find the important churn patterns. The key goal is to identify key churn drivers and formulate data-informed customer retention initiatives.

### Dataset Description

The project is based on the Telco Customer Churn dataset, which consists of 7,043 customer records and 21 attributes. Demographic, subscribed services, contract, payment, and billing details are included in the data set. The Churn variable is a customer retention or cancellation variable. The dataset can be used for various data mining methods as it contains both numerical and categorical variables.

### Dataset Source: Kaggle – Telco Customer Churn Dataset

#### Data Preparation and Preprocessing

The data set was loaded and analyzed in order to gain insight into the data types, variables and structure of the data set. TotalCharges was converted to a numerical format, leaving 11 missing values, which were filled in with the value of MonthlyCharges. There were no duplicate records found in the duplicate analysis. CustomerID was removed as identification values were not useful as predictive features, and Churn was converted to binary values. OneHotEncoder coded categorical variables, standardized numerical variables and split into 80/20 training and testing sets via stratified sampling.

#### Exploratory Data Analysis

These important patterns of customer retention were identified through exploratory analysis. The company experienced class imbalance with 73.46% keeping the company and 26.54% churning. The result was that churned customers tended to have higher monthly charges than retained customers. There was also a strong relationship between contract length and churn rate, as month-to-month contracts had a 42.71% churn rate, one-year contracts had an 11.27% churn rate, and two-year contracts had a churn rate of 2.83%. Fiber optic customers experienced a relatively high churn rate of 41.89%, indicating possible issues with pricing, service quality, or customer expectations.

#### Regression Analysis

The regression effort was on how well customers demographic, service, and account characteristics could be used to predict MonthlyCharges. Linear Regression achieved an MAE of 0.789, RMSE of 1.048, and R² of 0.999. Random Forest Regression achieved an MAE of 0.912, RMSE of 1.287, and R² of 0.998. Linear Regression outperformed all the other regression models and is the best model for prediction of the MonthlyCharges target variable.

#### Classification Analysis

The algorithms implemented for customer churn prediction are Decision Tree and K-Nearest Neighbour. The first Decision Tree had a score of 73.4% accuracy, 50.5% F1 score, and 66.3% ROC-AUC. The results were improved to 75.1% accuracy, 55.8% F1 score and 78.7% ROC-AUC for the Decision Tree after optimization using GridSearchCV. Initial KNN achieved 76.7% accuracy, 55.6% F1 score, and 80.2% ROC-AUC, while tuned KNN achieved 77.6% accuracy, 57.5% F1 score, and 81.1% ROC-AUC.

#### Best Classification Model

The tuned KNN model performed best of the tested models. The model recorded 77.6% accuracy, 57.5% F1 score, and 81.1% ROC-AUC. The classification performance was enhanced by the hyperparameter tuning, which is based on the nine nearest neighbors and the uniform weights. The ROC-AUC result suggests that the model has a good performance in differentiating between high and low-risk customers.

#### Customer Segmentation

K-Means clustering algorithm was used to find the customer groups having similar characteristic. CustomerID and Churn were excluded from the clustering process. OneHotEncoder was used for categorical variables and StandardScaler for numerical variables. Two to nine clusters were considered and evaluated using silhouette scores. The four clusters had the best silhouette scores and were chosen as the final structure of customer segmentation.

#### Cluster Analysis Findings

There were four customer segments that exhibited variation in tenure, charges, age and service characteristics. Cluster 0 were the customers who had lower charges and lower total purchases, whereas Cluster 1 were the longer-term customers who had higher monthly charges and longer tenure. Cluster 2 had the highest risk, with a churn rate of 46.58%, and Cluster 3 had a churn rate of 39.60%. The cluster results help to inform specific retention strategies according to customer attributes and churn propensity.

#### Association Rule Mining

The Apriori algorithm is used to find relationships between customers and customer characteristics and churn. Transaction analysis comprised of contract type, internet service, payment method, technical support, security services, and churn. Frequent itemsets were identified using minimum support of 5%, meaningful relationships were identified using minimum confidence of 50% and minimum lift of 1.

#### Association Rule Findings

Association analysis found that those customers who paid by electronic checks had more positive churn relationships, and month-to-month contracts more. Other churn associations emerged with fiber optic customers and with customers who did not have technical support or online security services. These patterns show the possibility that payment methods, contract structures, technical support and security services may affect the customer retention rates.

#### Feature Importance Analysis

Contract type was identified as the most powerful churn predictor with Feature importance analysis on the tuned Decision Tree. The importance value was 0.464 for two years contracts and 0.294 for one-year contracts. Billing variables and fiber optic internet services also showed some significance of 0.164 and 0.096 respectively. Results highlight the significance of contract, service and financial attributes in churn prediction.

### Major Findings

The most important churn-related factor was the contract type, as those on a month-to-month contract experienced significantly more churn. Internet service characteristics were also shown to have meaningful relationships with customer attrition, as were monthly charges. The tuned KNN model showed excellent results for the classification performance with 77.6% accuracy and 81.1% ROC-AUC. Four segments of customers were identified, of which the Cluster 2 is the highest risk segment with 46.58% churn.

### Business Recommendations

Loyalty rewards, discounts and contract upgrade offers should be used as a focus for retention campaigns, especially for customers who are on monthly contracts. High-risk Cluster 2 customers require personalized offers and proactive customer support. The use of technical support and online security service should be advocated within the proper customer base. The service reliability, pricing, technical support and customer expectations of fiber optic customers mean they need special handling. Quality of long-term predictions should be maintained by continuous monitoring of the model and periodic re-training.

### Ethical Considerations

Customer privacy must be handled carefully when dealing with predictive analysis of customers' information. CustomerID was dropped prior to modeling to minimize the exposure of identifying information. The fairness and bias should be assessed over various customer populations and the various performance measures should complement the overall accuracy. Feature importance analysis helps to understand more clearly the most important factors in churn predictions. Performance and fairness of models need to be continually monitored for responsible deployment.

### Challenges and Limitations

The data are from one telecommunications company; generalization is restricted to other telecommunications companies and markets. No information on customer satisfaction ratings, complaints, competitor offers, or detailed information on service quality was available. Although the classification models achieved good predictions, there were still some misclassifications. Periodic model retraining and segmentation may be necessary due to changes in customer behavior, market conditions and services.

### Future Improvements

Gradient Boosting, XGBoost and Neural Networks can be used in future analysis for better predictive results. Additional predictive features can be provided by customer satisfaction scores, complaint records, service-quality measurements, and competitor information. Real-time analytics can help continually track customer behavior and customer churn probability. The probability of churning and segmentation can be used in conjunction with automated recommendation systems to create personalized offers to retain customers.

### Conclusion

The project illustrates that using several data mining techniques to analyze the customer churn is effective. The support of the complementary information regarding customer behaviour has been gained from regression, classification, clustering and association rule mining. Some of the key factors that proved to be important for churn were contract type, internet service, monthly charges and support services. The tuned KNN model resulted in accuracy of 77.6% and ROC-AUC of 81.1% and four distinct customer segments were identified to facilitate retention planning. The results offer a basis for evidence-based customer retention strategies and for better business decisions.
