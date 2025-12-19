# Email Engagement Analysis & Predictive Modeling

## Project Overview
This project analyzes email campaign performance and builds predictive models to optimize user engagement. The goal is to understand email open and click behavior, calculate key KPIs, and identify high-potential segments for personalized targeting. When I began exploring the email engagement data, I expected to find a few simple patterns—perhaps certain email types or times of day performing slightly better. Instead, I uncovered a complex and fascinating story of user behavior, shaped by timing, personalization, and loyalty. Each insight revealed not just what was happening, but why, helping me understand how to craft campaigns that truly connect with users and drive engagement.

---

## Dataset

The dataset used in this project contains detailed logs from email campaigns. It includes the following key columns:

| Column Name             | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `Email Address`         | Recipient email address                                                     |
| `Email Name`            | Name of the email campaign                                                 |
| `Email Type`            | Category or type of email (e.g., newsletter, promotion)                    |
| `Delivery Status`       | Status of email delivery (e.g., Delivered, Bounced)                        |
| `Opened`                | Binary flag (1/0) indicating whether the email was opened                  |
| `First Opened UTC`      | Timestamp of the first time the email was opened                            |
| `Last Opened UTC`       | Timestamp of the last time the email was opened                             |
| `Clicked`               | Binary flag (1/0) indicating whether any link in the email was clicked      |
| `First Clicked UTC`     | Timestamp of the first time a link was clicked                               |
| `Last Clicked UTC`      | Timestamp of the last time a link was clicked                                |
| `Marked as spam`        | Binary flag (1/0) indicating if the email was marked as spam                |
| `Unsubscribe`           | Binary flag (1/0) indicating if the recipient unsubscribed                  |
| `Group Unsubscribe`     | Binary flag (1/0) indicating if the recipient unsubscribed from the group   |

> **Note:** The dataset has been anonymized for confidentiality and privacy. All personally identifiable information (PII) has been removed or masked.


---

## Objectives
1. **Email Campaign Analysis**
   - Calculate KPIs: Delivery Rate, Open Rate, Click Rate, Click-to-Open Rate, Spam Rate, Unsubscribe Rate, Engaged Rate  
   - Analyze trends by Email Type and Hour of Day 

2. **Segmentation Analysis**
   - Segment users by time-of-day and weekday  
   - Identify high-engagement groups  

3. **Predictive Modeling**
   - Build models to predict the probability of a user clicking an email  
   - Compare Logistic Regression, Random Forest, and Gradient Boosting models using cross-validation (ROC AUC)  
   - Optimize Gradient Boosting with hyperparameter tuning  
   - Estimate expected improvement in click rate for targeted campaigns  

---

## Methodology
1. **Data Cleaning**
   - Convert Boolean fields (`Opened`, `Clicked`, `Marked as spam`, etc.) to 0/1  
   - Handle missing values  
   - Remove duplicate email records  

2. **Exploratory Data Analysis (EDA)**
   - Visualize open/click rates by Email Type, Version, and Time  
   - Heatmaps for weekday vs. hour engagement  
   - Identify patterns in user behavior  

3. **KPI Calculations**
   - `Delivery Rate = Delivered / Sent`  
   - `Open Rate = Opened / Delivered`  
   - `Click Rate = Clicked / Delivered`  
   - `Click-to-Open Rate = Clicked / Opened`  
   - `Engaged Rate = Opened / Delivered`  

4. **Modeling**
   - Split data into training and test sets (70/30 stratified)  
   - Encode categorical features using OneHotEncoder  
   - Train models: Logistic Regression, Random Forest, Gradient Boosting  
   - Evaluate with 5-fold cross-validation (ROC AUC)  
   - Hyperparameter tuning for Gradient Boosting using GridSearchCV  

---

## Key Results
- **Gradient Boosting** achieved the highest CV ROC AUC: **0.9108**  
- **Open Rate**: 38.97%  
- **Click Rate**: 1.08%  
- **Click-to-Open Rate**: 2.78%  
- **Delivery Rate**: 87.71%  
- **Expected improvement** by targeting top 30% of predicted high-click users: **225%**

> Note: Clicks in this dataset are a subset of opens, so engagement is defined as `Opened`.

---

## Dashboard Visualization
[![Email Engagement Dashboard](images/dashboard.png)](https://public.tableau.com/app/profile/rohini.patturaja/viz/EmailEngagementDashboard/EmailEngagementDashboard)


---

## Recommendations
- Implement **personalized targeting** using predicted click probability  
- Optimize sending times based on high-engagement segments  
- Tailor email content length to user preferences  
- Conduct A/B testing with at least 340 users per group for 80% statistical power  
- Develop strategies for high-value and high-engagement user segments  

---

## Technologies Used
- Python: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`  
- Tableau for KPI dashboards and visualizations  

---
