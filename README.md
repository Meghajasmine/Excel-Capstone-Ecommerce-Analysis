# E-Commerce Store Sales & Performance Analysis

## Project Overview
This project performs end-to-end data cleaning, relational table integration, statistical analysis, and interactive dashboard reporting on an E-Commerce Store dataset using Microsoft Excel. The dataset comprises 2,000 sales transactions across 500 customers, 100 products, and 20 stores spanning October 2023 to October 2025.

## Repository Structure
- `Ecommerce_Sales_Dataset_Solution.xlsx` — Complete 7-worksheet Excel solution (`Executive Dashboard`, `Sales_Master_Cleaned`, `Customer_Dim`, `Product_Dim`, `Store_Dim`, `Pivot & Summary`, `Descriptive Statistics`).
- `Ecommerce_Sales_Dataset_updated.xlsx` — Raw source dataset.
- `One_Page_Executive_Summary.docx` — One-page summary of key findings and strategic decisions.

## Data Cleaning & Preprocessing Steps
1. **Primary Key Standardization:** Standardized malformed IDs (`C-1464`, `C-1486`, `C-1491`, `C-1499` to `CUST####` and `P-3`, `P-16` to `PROD#`), restoring 100% lookup integrity across all 2,000 transactions.
2. **Text & Country Standardization:** Applied `TRIM()` and `PROPER()` to clean whitespace and casing in `Name` and `City`; unified country variations (`United States of America`, `usa`) into `USA`.
3. **Missing Value Imputation:** Imputed missing `Loyalty_Level` entries with the mode (`Platinum`), imputed missing product `Cost` and `Stock` values using category medians, and algebraically recovered all 16 missing numeric fields in `Sales_Fact`.
4. **Relational Integration & Calculated Fields:** Used `XLOOKUP` to merge customer, product, and store attributes into `Sales_Master_Cleaned`, and derived `Order_Month` (`TEXT`), `Gross_Profit`, and `Order_Tier` (`IF`).

## Key Analytical Findings
- **Overall Performance:** Generated **$2,174,394.70** in total revenue and **$892,124.43** in gross profit (**41.0%** margin) across **2,000** orders and **4,964** units sold (Mean AOV: **$1,087.20**; Median AOV: **$868.72**).
- **Category Leaders:** **Sports** ($542,010.17 revenue; $287,778.34 profit) and **Electronics** ($504,311.35 revenue) lead total sales.
- **Regional Opportunity:** **North** ($646.1K), **South** ($635.2K), and **East** ($622.4K) perform evenly, while **West** ($270.7K, 12.4% share) represents a primary growth opportunity.
- **Channel & Payment Mix:** **Online** ($914.3K) and **Flagship** ($848.6K) stores drive 81.0% of revenue; **PayPal** ($756.8K) is the leading payment method.
