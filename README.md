# 📊 DarLy Data Analysis & Dashboard Project

## 📌 Project Overview

This project focuses on analyzing a service-based platform (**DarLy**) using **Power BI**.
The goal is to clean messy data, build a structured data model, and create a **multi-page interactive dashboard** to extract business insights.

---

## 🎯 Objectives

* Clean and transform raw data using **Power Query**
* Build a relational data model
* Create KPIs for business performance tracking
* Design a **multi-page dashboard** with navigation and tooltips
* Provide insights for operations, providers, and financial performance

---

## 🗂️ Dataset Description
<img width="512" height="285" alt="image" src="https://github.com/user-attachments/assets/250fa2c7-1f58-4bf5-b95b-630c09685e34" />

The dataset simulates a service platform and includes the following tables:

* **USERS** → Customer information
* **PROVIDERS** → Service providers data
* **SERVICES** → Available services
* **PROVIDER_SERVICES** → العلاقة بين providers والخدمات
* **REQUESTS** → طلبات المستخدمين
* **PAYMENTS** → بيانات الدفع

---

## 🧹 Data Cleaning (Power Query)

The dataset initially contained multiple issues such as:

* Missing values (NULLs)
* Invalid data types
* Inconsistent text values (e.g., cairo / CAIRO)
* Wrong timestamps (response before request)
* Invalid ratings and payment values
* Duplicate records

### ✔️ Cleaning Steps:

* Removed null and invalid records
* Standardized text formats
* Fixed date and time inconsistencies
* Corrected invalid values (e.g., ratings, payment amounts)
* Removed duplicates
* Validated relationships between tables

---

## 🧠 Data Model

Relationships were created between tables:

* USERS → REQUESTS
* PROVIDERS → REQUESTS
* SERVICES → REQUESTS
* REQUESTS → PAYMENTS
* PROVIDERS → PROVIDER_SERVICES

---

## 📊 Dashboard Structure

<img width="512" height="298" alt="image" src="https://github.com/user-attachments/assets/026b44ce-3ad8-43a5-b98b-0adfefb9dc9a" />
<img width="512" height="296" alt="image" src="https://github.com/user-attachments/assets/25f7287c-feb1-49cd-a2d1-cca7ae262045" />
<img width="512" height="296" alt="image" src="https://github.com/user-attachments/assets/240c0d83-32e4-4a40-aaaf-8a2e11e8fbb9" />
<img width="512" height="297" alt="image" src="https://github.com/user-attachments/assets/7bdaf87d-713d-4087-8e47-3386fe937305" />
<img width="512" height="296" alt="image" src="https://github.com/user-attachments/assets/fe1b0bb8-55e9-4cff-969f-2a7197155fe0" />



### 🏠 Home Page

* Navigation buttons to all pages
* Project logo and overview

---

### 📊 Overview Dashboard

**KPIs:**

* Total Requests
* Completed Requests
* Cancellation Rate
* Avg Response Time
* Avg Completion Time

**Charts:**

* Requests by Status
* Requests Over Time
* Top Services

---

### ⚙️ Operations Dashboard

**KPIs:**

* Avg Response Time
* Avg Completion Time
* % No Response
* % Late Requests

**Charts:**

* Response Time Distribution
* Requests by Hour
* Status Trend Over Time

---

### 👷 Providers Dashboard

**KPIs:**

* Total Providers
* Active Providers
* Average Rating

**Charts:**

* Top Providers
* Rating Distribution
* Availability Status

---

### 💰 Financial Dashboard

**KPIs:**

* Total Revenue
* Average Payment
* Paid Rate

**Charts:**

* Revenue Over Time
* Revenue by Service
* Payment Status Distribution

---

## 🧮 Key DAX Measures

```DAX
Total Revenue = SUM(PAYMENTS[Amount])

Avg Payment = AVERAGE(PAYMENTS[Amount])

% Paid = 
DIVIDE(
    CALCULATE(COUNT(PAYMENTS[Request_ID]), PAYMENTS[Payment_Status] = "Paid"),
    COUNT(PAYMENTS[Request_ID])
)
```

---

## 💡 Key Insights

* Identified delays in response times
* Detected inactive providers receiving requests
* Found inconsistencies between services and providers
* Measured revenue trends and payment performance

---

## 🛠️ Tools Used

* Power BI
* Power Query
* DAX

---

## 🚀 Future Improvements

* Add real-time data integration
* Implement advanced KPIs (SLA, churn rate)
* Enhance UI/UX design
* Add predictive analytics

---

## 📎 How to Use

1. Open the Power BI file
2. Refresh data
3. Navigate through dashboard pages
4. Use filters and tooltips for deeper insights

---

## 👩‍💻 Author

**SHIMAA EMAD**

---

## ⭐ If you like this project

Feel free to ⭐ the repo and share feedback!
