# Retail Sales Analysis (Beginner Level)

Data cleaning, KPI reporting and an Excel dashboard for a retail sales dataset, built with **Python (pandas, matplotlib)** and **Excel**.
Project for the **ShadowFox Data Analyst Internship – Beginner Level**.

## Objective
Turn raw sales data into clear business insights: what sells, when it sells, where it sells, and what the business should do next.

## Dataset
- `raw_retail_sales_data.csv` – 310 raw orders, Jan–Dec 2025 (INR).
- Columns: Order_ID, Order_Date, Customer_ID, Region, City, Category, Product, Quantity, Unit_Price, Unit_Cost, Discount_Pct, Payment_Mode, Sales_Channel.
- **Note:** this is a synthetic practice dataset created for learning, not real company data.

## Project Files
| File | Description |
|---|---|
| `raw_retail_sales_data.csv` | Original messy data |
| `retail_sales_analysis.ipynb` | Python notebook: cleaning, KPIs, trends, charts, insights |
| `cleaned_retail_sales.csv` | Cleaned dataset (created by the notebook) |
| `Retail_Sales_Dashboard.xlsx` | Excel dashboard: KPIs, charts, insights, cleaning log |
| `charts/` | Chart images exported by the notebook |

## Data Cleaning
| Problem | Fix |
|---|---|
| 10 duplicate rows | Removed |
| Inconsistent text (upper/lower case, extra spaces) in Category, Region, City | Trimmed and standardised to Title Case |
| Dates in 3 different formats | Converted to one date format |
| Missing Region (9) | Filled using the City's region from other rows |
| Missing Payment_Mode (7) | Filled with "Unknown" |
| Missing Discount_Pct (8) | Filled with 0 (assumption: no discount) |
| 3 rows with negative Quantity | Removed |

Result: 310 raw rows → **297 clean rows**. New columns added: Total_Sales, Profit, Month, Quarter, Profit_Margin_Pct.

## Key Metrics
| KPI | Value |
|---|---|
| Total Sales | ₹10.45 lakh |
| Total Profit | ₹3.22 lakh |
| Profit Margin | 30.8% |
| Total Orders | 297 |
| Average Order Value | ₹3,519 |
| Units Sold | 605 |

## Analysis Done
- Monthly sales and profit trend
- Category-wise sales, profit and margin
- Top and bottom products
- Region and city performance
- Online vs Offline sales
- Payment mode usage
- Impact of discounts on profit margin
- Repeat customers

## Key Insights
1. **November** is the best month (₹1.44 lakh) and **June** is the weakest (₹0.30 lakh). Q4 (Oct–Dec) brings about 33% of yearly sales.
2. **Furniture** is the top category (33.4% of sales); **Office Supplies** has the highest profit margin (35.8%).
3. **Study Table** is the best-selling product by revenue.
4. **West** is the leading region and **East** is the weakest.
5. **Online** channel contributes about 56% of sales.

## Business Recommendations
- Increase stock and run campaigns before November–December.
- Promote high-margin categories (e.g. Office Supplies) with bundles and cross-selling.
- Run targeted offers in the East region to close the gap with the West.
- Review high discounts (15–20%) because they reduce profit margin.


## How to Run
1. Clone the repo and keep the files in one folder.
2. Install the libraries: `pip install pandas numpy matplotlib openpyxl`
3. Open `retail_sales_analysis.ipynb` in Jupyter Notebook, VS Code or Google Colab and click **Run All**.
4. Open `Retail_Sales_Dashboard.xlsx` in Excel to see the dashboard.

## Tools Used
Python · pandas · NumPy · Matplotlib · Jupyter Notebook · Microsoft Excel (SUMIFS, COUNTIFS, charts)
