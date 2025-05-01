
# 📊 Sales Analysis Project – PostgreSQL + Power BI

This project is a comprehensive **Sales Data Analysis** solution built using **PostgreSQL** for backend data handling and **Power BI** for interactive visualization. The dataset, consisting of over 2 million rows, is sourced from raw `.txt` files representing real-world sales data.

## 🔧 Tools & Technologies

- **PostgreSQL** – for data storage, querying, and transformation
- **Power BI** – for building dynamic dashboards and visual reports
- **Text Files (.txt)** – raw data source
- **SQL** – for cleaning, joining, and calculating KPIs

## 🧱 Database Schema

The database uses a star schema and includes the following tables:

- `fact_sales` – transaction-level sales data
- `dim_customers` – customer demographic and ID information
- `dim_products` – product catalog data
- `dim_stores` – store location and type
- `dim_dates` – calendar reference for time-based analysis

## 📁 Project Structure

```
sales-analysis-project/
│
├── data/
│   ├── dim_customers.txt
│   ├── dim_products.txt
│   ├── dim_stores.txt
│   ├── dim_dates.txt
│   └── fact_sales.txt
│
├── sql/
│   ├── create_tables.sql
│   ├── insert_data.sql
│   ├── data_cleaning.sql
│   ├── analysis_queries.sql
│
├── powerbi/
│   └── SalesDashboard.pbix
│
├── report/
│   └── Sales_Analysis_Report.docx
│
└── README.md
```

## 🚀 How to Use

### Step 1: Set Up PostgreSQL

1. Create a new PostgreSQL database (e.g., `sales_db`).
2. Run `create_tables.sql` to set up the schema.
3. Use `insert_data.sql` to load data from `.txt` files (adjust paths and delimiters as needed).

Example `COPY` command:
```sql
COPY dim_customers FROM '/path/to/dim_customers.txt' DELIMITER ',' CSV HEADER;
```

### Step 2: Clean & Transform Data

- Run `data_cleaning.sql` to standardize, format, and prepare the data for analysis.

### Step 3: Run SQL Analysis

- Use `analysis_queries.sql` to generate insights and KPIs such as:
  - Total sales and revenue
  - Best-selling products
  - Sales by region and time period
  - Customer segmentation

### Step 4: Power BI Visualization

1. Open `SalesDashboard.pbix` in Power BI Desktop.
2. Connect to your PostgreSQL instance.
3. Refresh the data to load live visualizations.

## 📈 Key Insights

- Revenue trends by month, region, and store
- Product and category-level sales performance
- Top customer segments and purchasing behaviors
- Growth patterns and business opportunities

## 📄 Documentation

For detailed explanations, SQL logic, and insights, refer to the full report located in:

```
/report/Sales_Analysis_Report.docx
```
