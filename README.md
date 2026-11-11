# E-Commerce Sales & Customer Behaviour Analysis

## Project overview
This project performs exploratory data analysis on supplied prepared extracts from the UCI Online Retail dataset. It examines sales performance, product demand, geographic revenue, monthly trends and customer RFM segments.

## Dataset
- Reference: https://archive.ics.uci.edu/dataset/352/online+retail
- Included inputs: `data/positive_sales_transactions.csv`, `data/returns_cancellations_transactions.csv`, and summary tables under `data/tables/`.
- The original UCI workbook was not included in the uploaded ZIP. The included CSVs are prepared analysis extracts, not a replacement for the original raw dataset.

## Analysis performed
- Data structure, types, missingness and duplicate checks
- Revenue, invoice, unit and customer KPIs
- Distribution and outlier review
- Country and product performance
- Monthly revenue and weekday/hour activity
- Price/quantity and order-size/revenue scatter analysis
- Numeric correlation heatmap
- Customer RFM segment review
- Return/cancellation extract review and reconciliation checks

## Key findings (from supplied outputs)
- KPI summary gross sales revenue: approximately £10.64m.
- UK revenue share in the country summary: approximately 84.6%.
- November 2011 is the peak month in the supplied monthly table at approximately £1.50m.
- RFM Champions: 1,312 customers and approximately £6.48m segment revenue.
- CustomerID is missing on 132,186 of 524,878 positive-sales lines (25.2%).

## Data-quality and reconciliation notes
- Cleaning summary: 541,909 original rows; 5,268 exact duplicates removed; 536,641 cleaned master rows.
- Positive-sales extract contains 524,878 rows; returns/cancellations extract contains 10,587 rows. Their combined row count is 535,465, which is 1,176 below the cleaned-master figure.
- KPI summary reports 19,960 invoices; positive-sales extract contains 19,962 distinct invoice identifiers.
- These differences are disclosed and not silently reconciled. Validate against the original workbook and preprocessing logic before financial reporting.

## Deliverables
- `notebooks/Ecommerce_EDA_Analysis.ipynb`
- `reports/Ecommerce_EDA_Report.pdf`
- `presentation/Ecommerce_EDA_Presentation.pptx`
- `charts/` supporting visualizations
- `data/` prepared CSV extracts and summary tables

## Run the notebook
From the `notebooks` directory, open `Ecommerce_EDA_Analysis.ipynb` in Jupyter. Install dependencies listed in `requirements.txt`. The notebook expects the `data/` and `charts/` directories to remain in the project structure.

## Tools
Python, Pandas, NumPy, Matplotlib and Seaborn.

## Resume-ready description
Analysed 524K+ prepared retail sales lines using Python, Pandas, NumPy, Matplotlib and Seaborn to examine revenue trends, product demand, geographic performance and customer RFM segments; identified UK revenue concentration, a November sales peak and data-quality reconciliation issues.
