# 📉 Customer Churn Analysis Dashboard — Tableau

An interactive Tableau dashboard that analyzes customer churn for a telecom company. It shows how many customers leave, how much monthly revenue is at risk, and which contract types, internet services, payment methods and tenure groups are linked to the highest churn.

---

## 🎯 Project Objective

Help retention and customer success teams answer questions like:

- What is the overall churn rate, and how many customers do we have?
- How much monthly revenue is at risk because of churn?
- Which contract types, internet services and payment methods see the most churn?
- How does churn change with customer tenure?
- Does churn differ by gender?

---

## 🗂️ Dashboard Components

The workbook contains one dashboard built from **10 worksheets**.

| Worksheet | Type | What it shows |
|-----------|------|---------------|
| **Churn Rate** | KPI card | Share of customers who churned |
| **Total Customers** | KPI card | Number of distinct customers |
| **Total Monthly Revenue** | KPI card | Total monthly charges |
| **Revenue at Risk** | KPI card | Monthly charges from customers who churned |
| **Churn by Contract** | Bar chart | Churned customers by contract type |
| **Churn by Payment Method** | Bar chart | Churned customers by payment method |
| **Churn by Internet Service** | Chart | Churn across internet service types |
| **Churn by Tenure** | Line chart | Churn rate by tenure group |
| **Churn by Gender** | Pie chart | Churn split by gender |
| **Contract Type** | Pie chart | Customer mix by contract type |

---

## 🎛️ Interactivity

- **Filters** on the dashboard: Contract, Gender, Payment Method, Internet Service and Tenure Group
- **Cross-filtering** so every chart and KPI card responds to the filters

---

## 🧮 Calculated Fields

| Field | Definition |
|-------|------------|
| **Tenure Group** | Groups customers by months of tenure: 0–12, 13–24, 25–48 and 49+ months |
| **Churn Count** | `1` if Churn = "Yes", otherwise `0` |
| **Churn Rate** | `SUM(Churn Count) / COUNTD(customerID)` |
| **Revenue at Risk** | Monthly charges for customers with Churn = "Yes", otherwise `0` |

**Data fields used:** customerID, gender, SeniorCitizen, Partner, Dependents, tenure, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, Churn.

---

## 🛠️ Tools & Techniques

- **Tableau** — worksheets, dashboard design and filters
- **Calculated fields** — tenure grouping, churn rate and revenue at risk
- **Visualization types** — KPI cards, bar charts, pie charts and a trend line

---

## 📁 Repository Structure

```
├── CUSTOMER_CHURN_DASHBOARD.twb   # Tableau workbook
└── README.md
```

---

## 🚀 How to Use

1. Download or clone this repository
2. Open `CUSTOMER_CHURN_DASHBOARD.twb` in **Tableau Desktop** or **Tableau Public**
3. If Tableau asks for the data source, point it to the CSV file the workbook was built on
4. Use the filters to explore the dashboard

---

## 💡 Key Insights

- **Overall churn:** The company has **7,043 customers** and a **26.54%** churn rate, which is about **1,869 customers** who left.
- **Revenue at risk:** Customers who left represent **$139,131** in monthly charges, about **30.5%** of the **$456,117** total monthly revenue. That is a bigger share than the churn rate alone, so churned customers pay more than average.
- **Contract type is the biggest driver:** Month-to-month customers make up 3,875 of the customers and account for the vast majority of churn (roughly 1,650 customers). One-year and two-year contracts show very little churn.
- **New customers are most at risk:** Churn rate falls steadily with tenure, from **47.44%** in the first 12 months to 28.71% (13–24 months), 20.39% (25–48 months) and **9.51%** after 49 months.
- **Internet service:** Fiber optic customers churn at **41.9%**, compared with 19.0% for DSL customers and just 7.4% for customers with no internet service.
- **Payment method:** Electronic check accounts for **1,071** of the churned customers (about 57%), far more than mailed check (308), bank transfer (258) and credit card (232).
- **Gender:** Churn is almost evenly split, with 939 female and 930 male customers.

---

## 👤 Author

**Hammad**

- LinkedIn: [linkedin.com/in/hammad-ali-baig](https://www.linkedin.com/in/hammad-ali-baig)
- GitHub: [github.com/HammadAliBaig-Analytics](https://github.com/HammadAliBaig-Analytics)

Feedback and suggestions are welcome!
