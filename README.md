# 📊 Finance Analytics Dashboard

> A Power BI dashboard for financial transaction intelligence — built with DAX, dynamic metrics, and multi-dimensional customer segmentation.

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Time%20Intelligence-0078D4?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-27AE60?style=flat)

---

## 📌 Overview

This project is a **Finance Analytics Dashboard** built in Microsoft Power BI Desktop. It consolidates multi-source financial data into two interactive report pages, providing decision-makers with real-time, dynamic insight into transaction volumes, revenue trends, customer segments, and Year-over-Year (YoY) financial performance.

---

## 🖥️ Dashboard Pages

### Page 1 — Overview Analysis
The primary landing view. Contains KPI cards, trend charts, and segmentation visuals.

> 📸 _Add screenshot: `<img width="1373" height="770" alt="Over_view_analysis_dashboard" src="https://github.com/user-attachments/assets/83cfe970-c069-4b09-a05e-1f06a0a1a37d" />

`_

| Visual | Description |
|--------|-------------|
| KPI Card Block | Total Amount, Transactions, Avg Value, Fees & Tax with YoY % |
| Area Chart | Monthly trend of Total Transactions |
| Donut Chart 1 | Transactions by Status (completed / pending / failed) |
| Bar Chart 1 | Transactions by Customer Segment |
| Bar Chart 2 | Transactions by State |
| Donut Chart 2 | Transactions by Gender |
| Detail Table | Transaction Type Analysis — Amount, Fees, Tax, Count |

**Slicers:** Year · Dynamic Metric · Occupation · Merchant Category

---

### Page 2 — Transaction Drill-through
Row-level transaction explorer for operations, compliance, and audit teams.

> 📸 _Add screenshot: `<img width="1373" height="766" alt="Transaction_dashboard" src="https://github.com/user-attachments/assets/3ebb3f5f-8b8e-4782-ae80-b13dbae49ed0" />

`_

| Visual | Description |
|--------|-------------|
| Transaction Table | ID, Customer, Date, Type, Status, Gender, Segment, State, Amount, Fees, Tax |
| KPI Card Block | Consistent 5-KPI summary (same as Page 1) |

**Slicers:** Year · Dynamic Metric · Occupation · Merchant Category · Back Navigation

---

## 📐 Data Model

| Table | Type | Key Fields |
|-------|------|------------|
| `finance_transactions` | Fact | transaction_id, date, type, status, merchant_category, amounts |
| `customers` | Dimension | customer_name, segment, gender, state, occupation |
| `Calendar` | Date Dimension | Year, Month |

### DAX Measures
- `Total Amount` · `Total Transactions` · `Average Transaction Value` · `Total Fees` · `Total Tax`
- `YoY % Amount` · `YoY % Transaction` · `YoY % Avg` · `YoY % Fees` · `YoY % Tax`
- `Selected Dynamic Measure` · `Selected Year` · `Dashboard Title`

---

## ✨ Key Features

- **Dynamic Metric Switching** — single slicer updates KPIs across all visuals using a disconnected parameter table
- **Year-over-Year Tracking** — all 5 KPIs include DAX time-intelligence YoY % change
- **Cross-Page Navigation** — Page Navigator + Action Button for seamless drill-through
- **7 Filter Dimensions** — Time, Gender, Occupation, Segment, State, Transaction Type, Merchant Category
- **Full Transaction Drill-through** — 10+ column table for row-level audit and compliance

---

## 🗂️ Repository Structure

```
finance-analytics-dashboard/
├── dashboard/
│   └── new.pbix                    ← Power BI report file
├── screenshots/
│   ├── overview-page.png           ← Add your dashboard screenshot here
│   └── transaction-page.png        ← Add your drill-through screenshot here
├── data/
│   ├── finance_transactions.csv    ← (add if data is shareable)
│   └── customers.csv               ← (add if data is shareable)
├── README.md
└── Finance_Analytics_Dashboard_Report.docx
```

---

## 🚀 How to Use

1. **Clone this repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/finance-analytics-dashboard.git
   ```
2. **Open the report** in Power BI Desktop (`dashboard/new.pbix`)
3. **Refresh data sources** — update connection paths to your local data files if needed
4. **Explore** — use the slicers on Page 1 to filter by Year, Metric, Occupation, or Merchant Category
5. **Drill through** — click on any data point to navigate to the Transaction detail page

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Report authoring & visualisation |
| DAX | Calculated measures, YoY time intelligence |
| Power Query (M) | Data transformation & model shaping |

---

## 📈 Potential Enhancements

- [ ] Add a Forecast page with Power BI analytics pane
- [ ] Implement Row-Level Security (RLS) for team-based access
- [ ] Connect live to SQL Server / Azure Synapse
- [ ] Add geo-map visual for richer geographic analysis
- [ ] Publish to Power BI Service and embed in a web app

---

## 📄 License

MIT — free to use, modify, and distribute with attribution.

---

*Built with Power BI Desktop · Documented with Claude AI*
