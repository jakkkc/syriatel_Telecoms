![](download.png)
# syriatel_Telecoms
## Overview
This project focuses on analyzing and predicting customer churn for Syriatel, a telecommunications company. Customer churn is when customers stop using the company's services, which impacts revenue and growth. By identifying factors contributing to churn, Syriatel can develop strategies to improve customer retention.

## Objectives
Identify the main factors driving customer churn at Syriatel.
Predict which customers are likely to churn.
Develop strategies to retain customers and reduce churn.

## Data Understanding
The dataset comprises detailed information on 3,333 customers, encompassing 21 attributes that provide insights into customer behavior, service usage, and interactions with Syriatel.

### Key Variables
Customer Demographics: Information such as the customer's state and area code to identify geographic patterns.
Service Plans: Details about customers' international plans and voice mail plans.
Usage Metrics: Total minutes and calls during different times of the day and international calls.
Customer Service Interactions: Number of calls to customer service, indicating potential issues or dissatisfaction.

### Distribution Insights
Customer Service Calls: Skewed right, most values at 1.
Voice Mail Messages: Skewed right, most values at 0.
Account Length: Nearly normal distribution.
Area Code: Bimodal distribution with spikes at 408, 415, and 510.

## Data Exploration
Analyzing the key variables to understand their distribution and relationships helps identify factors contributing to customer churn.

### Geographic Distribution
Customers are distributed across various states and area codes, allowing us to identify regions with higher or lower churn rates.
### Service Plans
Understanding the distribution of customers with international and voice mail plans helps identify if certain plans are associated with higher or lower churn rates.
### Usage Patterns
Analyzing total minutes and calls during different periods provides insights into customer usage behavior.
### Customer Service Calls
The number of customer service calls is a critical factor, as frequent interactions may indicate unresolved issues or dissatisfaction.

## Feature Selection
Techniques used:

Multicollinearity Analysis: Identifies highly correlated feature pairs.
Feature Elimination: Removes features with high multicollinearity based on VIF scores.
### Selected Features
account length, total day minutes, total night minutes, total intl calls, total intl minutes, international plan, customer service calls, number vmail messages, state, total night calls, total day calls, total eve calls, total eve minutes, voice mail plan.

## Modeling
We employed various modeling techniques to predict customer churn, including Logistic Regression, Decision Tree, and Random Forest.

### Model Selection
Logistic Regression: Effective for binary classification tasks.
Decision Tree: Provides clear, visual decision rules.
Random Forest: Combines multiple decision trees for better accuracy and control over-fitting.
## Data Preprocessing
Scaling Numerical Features: Using StandardScaler.
Encoding Categorical Variables: Using OneHotEncoder.
Balancing Data: Applying SMOTE to address class imbalance.
## Training and Validation
Training Set: Split historical data into training and validation sets.
Cross-Validation: Used to evaluate model performance and ensure generalization to unseen data.
## Model Performance
Random Forest: Highest accuracy (93.9%) and precision (0.857).
Decision Tree: Balanced approach with good precision (0.667) and recall (0.693).
Logistic Regression: High recall (0.782) but low precision (0.401).
### Confusion Matrix
Random Forest: Highest true positives and true negatives, lowest false positives and negatives.
Decision Tree: Balanced approach with good precision and recall.
Logistic Regression: Highest recall but low precision.

Random Forest: Best performance with highest true positives and true negatives, lowest false positives, and false negatives.

### Accuracy
Random Forest: Best accuracy (93.9%), precision (0.857), and recall (0.713).
Decision Tree: Accuracy (90.1%), precision (0.667), and recall (0.693).
Logistic Regression: Accuracy (79.0%), precision (0.401), and recall (0.782).

### ROC Curve
Random Forest: Closest to the top left corner, indicating higher true positive rates for lower false positive rates.
## Conclusion
Accurately predicting customer churn allows Syriatel to implement targeted retention strategies, improving customer satisfaction and revenue stability. The Random Forest model is recommended for its high accuracy and precision.

## Recommendations
Implement Random Forest for Churn Prediction: Use for reliable identification of potential churners.
Proactive Retention Strategies: Develop targeted campaigns for high-risk customers.
Monitor Model Performance: Regularly evaluate and retrain the model with new data.
Analyze Churn Reasons: Focus on improving customer service, plan options, and network quality.
Customer Feedback Loop: Gather data from customers predicted to churn but chose to stay, refining retention strategies and improving the prediction model.
