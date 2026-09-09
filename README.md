# Sales Growth Analysis

An end-to-end sales data analysis project: raw sales data is cleaned and transformed in Python (Pandas), loaded into a MySQL database via SQLAlchemy, and visualized in an interactive Power BI dashboard.

## Overview

This project takes raw transactional sales data and turns it into a clean, query-ready dataset and a visual dashboard for tracking sales growth, profit, and trends over time.

**Pipeline:**
1. **Extract** — Load raw sales data (`data/sales_raw_500.csv`)
2. **Clean** — Remove duplicates, fix malformed date values, drop invalid rows
3. **Transform** — Derive `Profit` (Sales − Cost), `Year`, and `Month` columns
4. **Load** — Push the cleaned dataset into a MySQL database
5. **Visualize** — Explore sales trends, growth, and profitability in Power BI

## Repository Structure

```
Sales-Growth-Analysis/
├── Sales_Growth_Analysis.ipynb   # Data cleaning + MySQL load pipeline
├── sales_Growth_Analysis.pbix    # Power BI dashboard
├── data/
│   └── sales_raw_500.csv         # Sample raw sales dataset
├── requirements.txt              # Python dependencies
├── .gitignore
└── README.md
```

## Tech Stack

- **Python** — Pandas for data cleaning and transformation
- **SQLAlchemy + PyMySQL** — Loading data into MySQL
- **MySQL** — Data storage
- **Power BI** — Dashboard and visualization

## Getting Started

### Prerequisites
- Python 3.8+
- MySQL Server
- Power BI Desktop (to open the `.pbix` file)

### Setup

1. Clone the repo:
   ```bash
   git clone https://github.com/barnabashansda01/Sales-Growth-Analysis.git
   cd Sales-Growth-Analysis
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set your database credentials as environment variables (do **not** hardcode them). Create a `.env` file in the project root:
   ```
   DB_USER=your_username
   DB_PASSWORD=your_password
   DB_HOST=localhost
   DB_PORT=3306
   DB_NAME=salesdb
   ```

4. Run `Sales_Growth_Analysis.ipynb` to clean the data and load it into MySQL.

5. Open `sales_Growth_Analysis.pbix` in Power BI Desktop and point it to your MySQL database (or the exported CSV) to refresh the dashboard.

## Key Results

- Cleaned and deduplicated 500+ raw sales records
- Standardized inconsistent date formats across the dataset
- Derived profit and time-based metrics for trend analysis
- Built a structured MySQL data store for repeatable querying and reporting
  
## License

MIT
Dashboard - <img width="1920" height="1080" alt="Screenshot (54)" src="https://github.com/user-attachments/assets/da27bf80-cc13-44b2-8cf8-dfad0a1423ca" />
