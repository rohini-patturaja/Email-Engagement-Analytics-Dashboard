# 📧 Email Engagement Analytics Dashboard

## 📌 Project Overview

This project analyzes **email campaign engagement** data to understand how alumni and stakeholders interact with university communications. The goal is to uncover actionable insights related to **opens, clicks, delivery performance, and engagement timing**, and present them through an **interactive Tableau dashboard**.

The dashboard is designed with a **business storytelling approach**, enabling marketing and advancement teams to optimize email strategy based on data-driven insights.

---

## 🎯 Business Objectives

* Measure and compare engagement performance across email campaigns
* Identify high-performing campaigns based on open and click behavior
* Understand **when** users are most likely to engage (day, hour, month)
* Analyze delivery effectiveness and bounce behavior
* Enable dynamic exploration using parameters (Top N, Metric Selection, Time Filters)

---

## 📊 Dataset Description

The dataset contains email-level engagement data with the following fields:

* **Email Address**
* **Email Name (Campaign)**
* **Email Type**
* **Delivery Status** (Delivered, Bounced, Blocked, etc.)
* **Opened** (Binary)
* **Clicked** (Binary)
* **First Opened UTC**
* **Last Opened UTC**
* **First Clicked UTC**
* **Last Clicked UTC**
* **Marked as Spam**
* **Unsubscribe**
* **Group Unsubscribe**

⚠️ Note: The dataset does not contain a sent timestamp or revenue metrics. All time-based analyses are derived from engagement events.

---

## 🧹 Data Preparation & Cleaning

Data preprocessing was performed using **Python (pandas)** and includes:

* Standardizing email addresses (lowercase, trimmed)
* Removing fully duplicate records
* Handling missing timestamps (NaT values)
* Normalizing categorical fields (Email Type, Delivery Status)
* Creating safe binary aggregations for Opened and Clicked metrics

---

## 📐 Key KPIs Calculated

* **Emails Sent**
* **Emails Delivered**
* **Open Count & Open Rate**
* **Click Count & Click-Through Rate (CTR)**
* **Open-to-Click Rate (CTOR)**
* **Bounce Rate**
* **Unsubscribe Rate**
* **Spam Rate**
* **Unique Opens & Unique Clicks**
* **Campaign Rank (by volume and engagement)**

---

## 📈 Dashboard Components (Tableau)

### 1️⃣ KPI Summary Cards

* Emails Sent
* Emails Delivered
* Emails Opened
* Unique Clicks
  Includes month-over-month comparison indicators.

---

### 2️⃣ Performance by Campaign Table

An interactive table displaying:

* Campaign Name
* Sent Rank (visualized using circular badges)
* Delivered & Opened (bar indicators)
* Open Rate, Click Rate, Open-to-Click Rate (donut-style visuals)
* Dynamic **Top N** and **Sort By** controls

---

### 3️⃣ Calendar Heatmap (Engagement Activity)

* Shows engagement intensity by **day of month**
* Driven by **First Opened UTC**
* Supports dynamic metric selection (Sent, Opened, Clicked, Bounced)

---

### 4️⃣ Weekday & Hour Analysis

* Bar charts highlighting engagement by:

  * Day of week
  * Hour of day
* Helps identify optimal email timing

---

### 5️⃣ Open Rate vs Click Rate Scatter Plot

* Each point represents a campaign
* Used to identify:

  * High open but low click campaigns
  * Highly engaged campaigns
  * Optimization opportunities

---

## 🎛 Parameters & Interactivity

* **Year Selector**
* **Month Selector**
* **Metric Selector** (Sent, Opened, Clicked, Bounced)
* **Top N Campaigns**
* **Sort Table By Metric**

All parameters are fully interactive and dashboard-driven.

---

## 💡 Key Insights

* Certain campaigns achieve high open rates but underperform on clicks, indicating content optimization opportunities.
* Engagement varies significantly by weekday, with mid-week showing higher activity.
* Campaign ranking changes depending on whether volume or engagement metrics are used.
* Open-to-click rate reveals which campaigns truly convert attention into action.

---

## 🧠 Tools & Technologies

* **Python** (pandas, numpy) – data cleaning & feature engineering
* **Tableau** – visualization & dashboard development
* **Figma** – dashboard layout inspiration
* **GitHub** – version control & portfolio hosting

---

## 🚀 Future Enhancements

* Add subject-line sentiment analysis
* Build predictive models for open/click likelihood
* Integrate sent timestamp for latency analysis
* Include cohort-based engagement tracking
* Automate data refresh pipeline

---

## 📷 Dashboard Preview

*(Insert dashboard screenshots here)*

---

## 🙋‍♀️ About Me

**Roni**
Aspiring Data Analyst / Business Intelligence Analyst
Background in ETL & Data Engineering | Passionate about storytelling with data

📫 *Open to opportunities in Data Analytics & BI roles*

---

⭐ If you found this project interesting, feel free to star the repo!
