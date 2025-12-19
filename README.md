# Email Engagement Analysis & Predictive Modeling

## Project Overview
This project analyzes email campaign performance and builds predictive models to optimize user engagement. The goal is to understand email open and click behavior, calculate key KPIs, and identify high-potential segments for personalized targeting.

---

## Dataset
The dataset contains email campaign logs with the following key columns:

- `Email Address` – recipient email  
- `Email Name` – name of the email campaign  
- `Email Type` – type/category of the email  
- `Delivery Status` – whether the email was successfully delivered  
- `Opened` – binary flag indicating if the email was opened  
- `Clicked` – binary flag indicating if any link was clicked  
- `Marked as spam` – binary flag indicating if the email was marked as spam  
- `Unsubscribe` – binary flag indicating user unsubscribed  
- `Group Unsubscribe` – binary flag for group unsubscribe  
- `First Opened UTC` / `Last Opened UTC` – timestamps of email opens  
- `First Clicked UTC` / `Last Clicked UTC` – timestamps of email clicks  

> Note: The dataset has been anonymized for confidentiality.

---

## Objectives
1. **Email Campaign Analysis**
   - Calculate KPIs: Delivery Rate, Open Rate, Click Rate, Click-to-Open Rate, Spam Rate, Unsubscribe Rate, Engaged Rate  
   - Analyze trends by Email Type, Hour of Day, and Email Version  

2. **Segmentation Analysis**
   - Segment users by time-of-day, weekday, and email version  
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
- **Engaged Rate**: 40.05%  
- **Expected improvement** by targeting top 30% of predicted high-click users: **225%**

> Note: Clicks in this dataset are a subset of opens, so engagement is defined as `Opened`.

---

## Visualizations

[View Interactive Dashboard](https://public.tableau.com/views/)

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
