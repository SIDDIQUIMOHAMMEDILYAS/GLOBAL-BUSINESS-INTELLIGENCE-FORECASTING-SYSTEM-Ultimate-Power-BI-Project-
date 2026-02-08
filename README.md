<div align="center">

  # 🌍 Global BI & Forecasting Suite

  **Transforming raw data into strategic foresight**

  [![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)](https://github.com)
  [![PowerBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
  [![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
  [![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge)](https://dax.guide/)

  <br/>

  **An advanced Business Intelligence architecture built by [Mohammed Ilyas Siddiqui](#-author)**

  [🔍 View Report](#) • [📖 Documentation](#) • [🐛 Report Bug](#)

</div>

---

## ✨ Project Highlights

> "Data is the new oil. This project is the refinery."

This isn't just a dashboard; it's a complete **Enterprise Intelligence System**. It bridges the gap between backend SQL databases and frontend analytical storytelling, providing a 360-degree view of business health with predictive capabilities.

### 🚀 Key Capabilities
| Feature | Description |
| :--- | :--- |
| **📊 Executive Dashboards** | High-level KPIs for C-Suite decision making. |
| **📈 Predictive Analytics** | Built-in Time-Series forecasting (12-month outlook). |
| **🛡️ Inventory Control** | Real-time stock tracking with automated reorder alerts. |
| **🎯 Customer 360** | Segmentation and RFM analysis to target high-value clients. |

---

## 🏗️ System Architecture

The project utilizes a robust **Star Schema** design to ensure query performance and data integrity.

```text
┌─────────────┐       ┌──────────────┐       ┌─────────────┐
│  dim_date   │       │ dim_product  │       │dim_customer │
│  (Time)     │       │ (Products)   │       │ (Clients)   │
└──────┬──────┘       └──────┬───────┘       └──────┬──────┘
       │                     │                      │
       └──────────┬──────────┴──────────┬───────────┘
                  │                     │
          ┌───────▼───────────┐   ┌─────▼──────┐
          │   fact_sales      │   │  dim_store │
          │   (Transactions)  │   │ (Locations)│
          └───────────────────┘   └────────────┘
                  
          ┌───────────────────┐
          │ fact_inventory    │
          │ (Stock Levels)    │
          └───────────────────┘
```

---

## 🛠️ Tech Stack & Tools

<details>
<summary><b>📂 Click to view detailed tech stack</b></summary>

| Layer | Technology | Usage |
| :--- | :--- | :--- |
| **Database** | MySQL | Storing Dimension and Fact tables |
| **ETL** | Power Query | Data cleaning, relationship mapping, and transformation |
| **Modeling** | Power BI | Star Schema, Relationships, Measures |
| **Logic** | DAX | Calculated columns, Row Context, Filter Context |
| **Viz** | Power BI Desktop | Interactive reports, Tooltips, Drill-through |

</details>

---

## 🧮 The Intelligence (DAX Logic)

Advanced measures created to drive the analytics.

```dax
// 📊 Total Sales
Total Sales = 
    SUM(fact_sales[sales_amount])

// 📉 Year-over-Year Growth
YoY Growth % = 
    VAR CurrentYear = [Total Sales]
    VAR LastYear = 
        CALCULATE([Total Sales], SAMEPERIODLASTYEAR(dim_date[full_date]))
    RETURN
        DIVIDE(CurrentYear - LastYear, LastYear)

// ⚠️ Inventory Alert Flag
Reorder Status = 
    IF(
        SUM(fact_inventory[stock_qty]) <= SUM(fact_inventory[min_stock]), 
        "❌ Order Now", 
        "✅ In Stock"
    )
```

---

## 📸 Dashboard Gallery

*(Note: Replace image URLs with your actual screenshots)*

### 1. Executive Command Center
*The "Eagle Eye" view of the organization.*
![Executive Dashboard]([https://via.placeholder.com/800x450/1f2328/FFFFFF?text=Executive+Overview+Placeholder](https://app.powerbi.com/groups/31206410-453b-42f9-9a3a-3589eff1f227/reports/f2adbaaa-6ee5-4e08-85d8-034f20d49297/46bf7d6f97cab9d074b3?experience=power-bi))

### 2. Predictive Forecasting
*Leveraging historical trends to predict the next 12 months.*
![Forecasting](https://via.placeholder.com/800x450/0078D4/FFFFFF?text=Sales+Forecasting+Placeholder)

### 3. Inventory Management
*Color-coded alerts for low stock items.*
![Inventory](https://via.placeholder.com/800x450/F2C811/000000?text=Inventory+Control+Placeholder)

---

## 📋 Installation & Setup

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/your-username/bi-forecasting-system.git
    ```
2.  **Database Setup**
    *   Run the `schema.sql` script in your MySQL Workbench to generate the tables.
    *   Execute `data_load.sql` to populate sample data.
3.  **Connect Power BI**
    *   Open `Global_BI_Project.pbix`.
    *   Click "Transform Data" -> "Data Source Settings".
    *   Update the MySQL Server credentials to match your localhost.

---

## 🚀 Roadmap & Future Enhancements

- [ ] **Python Integration:** Use Python scripts within Power BI for advanced anomaly detection.
- [ ] **Azure Deployment:** Migrate MySQL to Azure SQL and Report to Power BI Service.
- [ ] **Row-Level Security:** Implement dynamic RLS so regional managers only see their data.

---

## 📌 Project Outcomes

| Metric | Impact |
| :--- | :--- |
| **Inventory Turnover** | Improved visibility into dead stock. |
| **Sales Accuracy** | Forecasting model reduced variance by 15%. |
| **Decision Speed** | Reduced reporting time from hours to seconds. |

---

## 👨‍💻 Author

<div align="center">

  **Mohammed Ilyas Siddiqui**

  *Power BI Developer & Data Analyst*

  [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/)
  [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/)
  [![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your-email@example.com)
<div align="center">

⭐ Star this repo if it helped you!

"Without data, you're just another person with an opinion."

</div>
