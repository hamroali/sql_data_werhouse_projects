# sql_data_werhouse_projects
Building and modern data werehouse with sql server, inculuding ETl processes, data modeling and analitiys
# Data Warehouse and Analytics Project

Welcome to my **Data Warehouse and Analytics Project** repository! 🚀
This project demonstrates a complete data warehousing solution, from raw source data to business-ready insights. It was built as a hands-on portfolio project to practice industry best practices in data engineering and analytics.

---

## 🏗️ Data Architecture

The project follows the **Medallion Architecture** with three layers: **Bronze**, **Silver**, and **Gold**.

![Data Architecture](docs/data_architecture.png)

1. **Bronze Layer**: Stores raw data as-is from the source systems. Data is loaded from CSV files into SQL Server.
2. **Silver Layer**: Cleans, standardizes, and normalizes the data to prepare it for analysis.
3. **Gold Layer**: Holds business-ready data modeled into a **star schema** for reporting and analytics.

---

## 📖 Project Overview

This project covers:

- **Data Architecture**: Designing a modern data warehouse using the Medallion Architecture.
- **ETL Pipelines**: Extracting, transforming, and loading data from source systems into the warehouse.
- **Data Modeling**: Building fact and dimension tables optimized for analytical queries.
- **Analytics & Reporting**: Writing SQL queries to generate insights about customers, products, and sales.

---

## 🛠️ Tools Used

- **SQL Server** – database engine for hosting the data warehouse
- **SSMS (SQL Server Management Studio)** – for writing and running SQL
- **Draw.io** – for architecture, data flow, and data model diagrams
- **Git & GitHub** – for version control and project hosting
- **Notion** – for project planning and task tracking

---

## 🎯 Project Requirements

### Building the Data Warehouse (Data Engineering)

**Objective:** Develop a modern data warehouse in SQL Server to consolidate sales data and enable analytical reporting.

**Specifications:**
- **Data Sources:** Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality:** Cleanse and resolve data quality issues before analysis.
- **Integration:** Combine both sources into a single, user-friendly data model.
- **Scope:** Focus on the latest dataset only; historization is not required.
- **Documentation:** Provide clear documentation of the data model for business users and analytics teams.

### Analytics & Reporting (Data Analysis)

**Objective:** Develop SQL-based analytics to deliver insights into:
- Customer behavior
- Product performance
- Sales trends

---

## 📂 Repository Structure

```
sql-data-warehouse-project/
│
├── datasets/                     # Raw source data (ERP and CRM CSV files)
│
├── docs/                         # Documentation and diagrams
│   ├── data_architecture.drawio  # Overall project architecture
│   ├── data_flow.drawio          # Data flow / lineage diagram
│   ├── data_models.drawio        # Star schema data model
│   ├── data_catalog.md           # Description of Gold layer tables and columns
│   └── naming_conventions.md     # Naming rules for tables, columns, and files
│
├── scripts/                      # SQL scripts
│   ├── init_database.sql         # Creates the database and schemas
│   ├── bronze/                   # Load raw data
│   ├── silver/                   # Clean and transform data
│   └── gold/                     # Create analytical views
│
├── tests/                        # Data quality check scripts
│
├── README.md                     # Project overview
└── LICENSE                       # License information
```

---

## 🚀 How to Run

1. Clone this repository.
2. Open `scripts/init_database.sql` in SSMS and run it to create the `DataWarehouse` database and the `bronze`, `silver`, and `gold` schemas.
3. Run the scripts in the `bronze`, `silver`, and `gold` folders in order.
4. Load the data:
   ```sql
   EXEC bronze.load_bronze;
   EXEC silver.load_silver;
   ```
5. Query the Gold layer:
   ```sql
   SELECT * FROM gold.fact_sales;
   ```

---

## 🙏 Acknowledgements

This project was built by following the
[SQL Data Warehouse from Scratch](https://www.youtube.com/@datawithbaraa) course by **Data With Baraa**.

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE).

---

## 👋 About Me

Hi, I'm **Hamroali Safarov** – a Data Analyst transitioning into Data Engineering.

- 💼 LinkedIn:(https://www.linkedin.com/in/hamroali-safarov-0a053439a/?isSelfProfile=true)
- 📧 Email: Hamroalisafarov4@gmail.com
