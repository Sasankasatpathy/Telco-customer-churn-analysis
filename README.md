# 📊 Telco Customer Churn Analysis | Power BI

## 🚀 Project Overview

Customer churn is one of the most critical challenges in the telecommunications industry. Retaining existing customers is significantly more cost-effective than acquiring new ones. This project analyzes customer churn behavior using Power BI to identify high-risk customer segments, uncover churn drivers, and provide actionable business recommendations.

The dashboard enables stakeholders to monitor customer retention, evaluate revenue impact, and make data-driven decisions to reduce churn.

---

## 🎯 Business Objective

The primary objectives of this project are:

* Analyze customer churn patterns.
* Identify key factors influencing customer attrition.
* Quantify revenue loss due to churn.
* Segment high-risk customer groups.
* Provide retention-focused business recommendations.

---

## 📁 Dataset Information

### Dataset Summary

| Metric          | Value              |
| --------------- | ------------------ |
| Total Records   | 7,043              |
| Total Features  | 21                 |
| Industry        | Telecommunications |
| Target Variable | Churn              |

### Key Features

* Customer Demographics
* Contract Type
* Internet Service
* Payment Method
* Monthly Charges
* Total Charges
* Tenure
* Additional Service Subscriptions
* Churn Status

---

## 🛠️ Tools & Technologies

* Power BI Desktop
* Power Query
* DAX
* Data Modeling
* Data Visualization
* Business Analytics

---

## 📋 Data Preparation

### Data Cleaning

* Handled missing values in Total Charges
* Converted data types
* Created Tenure Groups
* Verified data consistency
* Optimized model relationships

### Feature Engineering

Created customer tenure segments:

| Segment               | Tenure       |
| --------------------- | ------------ |
| New Customers         | 0-12 Months  |
| Growing Customers     | 13-24 Months |
| Established Customers | 25-48 Months |
| Loyal Customers       | 49+ Months   |

---

# 📊 Dashboard Pages

## 1️⃣ Executive Summary

### KPIs

* Total Customers
* Active Customers
* Churned Customers
* Churn Rate
* Revenue Lost
* ARPU (Average Revenue Per User)

### Visuals

* Churn by Contract Type
* Churn by Internet Service
* Churn by Payment Method

---

## 2️⃣ Customer Analysis

### Visuals

* Churn by Gender
* Churn by Senior Citizen
* Churn by Dependents
* Churn by Partner Status

Purpose:

* Understand customer demographics contributing to churn.

---

## 3️⃣ Service Analysis

### Visuals

* Churn by Online Security
* Churn by Tech Support
* Churn by Device Protection
* Churn by Streaming Services

Purpose:

* Identify service-related churn drivers.

---

## 4️⃣ Revenue Analysis

### Visuals

* Revenue by Contract Type
* Revenue by Internet Service
* Monthly Charges vs Churn
* Revenue Lost by Customer Segment

Purpose:

* Evaluate the financial impact of churn.

---

## 5️⃣ Advanced Analytics

### Decomposition Tree

Analyze churn by:

* Contract Type
* Internet Service
* Payment Method
* Tech Support

### Key Influencers

Identify the strongest factors contributing to churn.

Purpose:

* Discover root causes behind customer attrition.

---

# 📈 DAX Measures

### Total Customers

```DAX
Total Customers =
COUNT(Telecom[customerID])
```

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
    COUNT(Telecom[customerID]),
    Telecom[Churn] = "Yes"
)
```

### Active Customers

```DAX
Active Customers =
[Total Customers] - [Churned Customers]
```

### Churn Rate %

```DAX
Churn Rate % =
DIVIDE(
    [Churned Customers],
    [Total Customers]
)
```

### Revenue Lost

```DAX
Revenue Lost =
CALCULATE(
    SUM(Telecom[MonthlyCharges]),
    Telecom[Churn] = "Yes"
)
```

### ARPU

```DAX
ARPU =
DIVIDE(
    SUM(Telecom[MonthlyCharges]),
    [Total Customers]
)
```

---

# 🔍 Key Insights

### Customer Behavior

* Month-to-month contract customers have the highest churn rate.
* Customers with lower tenure are more likely to churn.
* Senior citizens show higher churn behavior compared to other segments.

### Service Insights

* Customers without online security exhibit higher churn.
* Lack of tech support increases churn risk.
* Fiber optic customers churn more frequently than DSL users.

### Revenue Impact

* Customer churn contributes significantly to revenue loss.
* High-value customers generate a disproportionate share of lost revenue.

---

# 💡 Recommendations

1. Encourage customers to switch from month-to-month to long-term contracts.
2. Bundle Online Security and Tech Support services.
3. Launch targeted retention campaigns for new customers.
4. Create loyalty programs for high-value customers.
5. Offer personalized discounts to high-risk segments.

---

# 📸 Dashboard Preview

Add dashboard screenshots here:

```markdown
![Executive Dashboard](Images/Executive_Dashboard.png)

![Customer Analysis](Images/Customer_Analysis.png)

![Revenue Analysis](Images/Revenue_Analysis.png)
```

---

# 📂 Repository Structure

```text
Telco-customer-churn-analysis/
│
├── Data/
│   └── customer_churn.csv
│
├── Dashboard/
│   └── Telecom_Churn_Dashboard.pbix
│
├── Images/
│   ├── Executive_Dashboard.png
│   ├── Customer_Analysis.png
│   └── Revenue_Analysis.png
│
└── README.md
```

---

# 👨‍💻 Author

**Sasanka Satpathy**

Aspiring Data Analyst | SQL | Power BI | Python | Excel | Statistics

LinkedIn: https://www.linkedin.com/in/sasanka-sekhar-satpathy-6b5b83232/

GitHub: https://github.com/Sasankasatpathy
