# Excel-Sales-Dashboard-1

## Overview

**Excel Dashboard 1** (`ExcelReport1_Data.xlsx`) is a financial performance dashboard built in Microsoft Excel. It visualises transaction-level business data across regions, departments, product lines, and customer segments, covering the period **January 2022 – December 2023**.

The workbook contains **2,000 transactions** and a total recorded revenue of **$53,965,575**, with net profit of **$20,493,529**.

---

## Workbook Structure

| Sheet | Purpose |
|---|---|
| `Dashboard` | Main visual dashboard (charts, slicers, KPI tiles) |
| `Data` | Raw transaction data — the single source of truth |
| `Sheet1` | PivotTable: Profit, Expenses & Revenue by Category |
| `Sheet2` | PivotTable: Total Profit by Region and Product Line |
| `Sheet3` | PivotTable: Total Profit by Payment Method |
| `Sheet4` | PivotTable: Total Profit by Product Line |
| `Sheet5` | PivotTable: Average Expenses by Department |

---

## Data Schema (`Data` sheet)

The raw data sheet holds **2,000 rows** with the following 12 columns:

| Column | Type | Description |
|---|---|---|
| `Transaction_ID` | Text | Unique identifier (e.g. TXN0001) |
| `Transaction_Date` | Date | Date of the transaction (2022–2023) |
| `Revenue` | Number | Gross revenue for the transaction |
| `Expenses` | Number | Associated costs |
| `Profit` | Number | Revenue minus Expenses |
| `Category` | Text | Business category (HR, Marketing, Operations, R&D, Sales) |
| `Region` | Text | Geographic region (see below) |
| `Department` | Text | Internal department (see below) |
| `Product_Line` | Text | Product category sold (see below) |
| `Customer_Segment` | Text | Customer type (B2B, B2C, Enterprise, SMB) |
| `Payment_Method` | Text | How payment was made (see below) |
| `Discount` | Decimal | Discount rate applied (e.g. 0.09 = 9%) |

---

## Dimension Reference

**Regions:** Africa, Asia-Pacific, Europe, North America, South America

**Departments:** Finance, HR, IT, Marketing, Operations, Sales

**Product Lines:** Clothing, Electronics, Furniture, Healthcare, Software

**Customer Segments:** B2B, B2C, Enterprise, SMB

**Payment Methods:** Bank Transfer, Cash, Credit Card, PayPal

---

## Key Metrics Summary

### By Category (Profit / Expenses / Revenue)
| Category | Profit | Expenses | Revenue |
|---|---|---|---|
| R&D | $8,330,376 | $14,381,610 | $22,711,986 |
| Sales | $3,906,246 | $6,133,907 | $10,040,153 |
| Marketing | $3,338,910 | $5,417,002 | $8,755,912 |
| Operations | $2,766,291 | $4,291,785 | $7,058,076 |
| HR | $2,151,706 | $3,247,742 | $5,399,448 |
| **Grand Total** | **$20,493,529** | **$33,472,046** | **$53,965,575** |

### By Product Line (Total Profit)
| Product Line | Profit |
|---|---|
| Healthcare | $8,548,972 |
| Electronics | $3,782,643 |
| Software | $3,065,563 |
| Clothing | $2,924,461 |
| Furniture | $2,171,890 |

### By Payment Method (Total Profit)
| Payment Method | Profit |
|---|---|
| Cash | $9,013,666 |
| Credit Card | $5,030,165 |
| Bank Transfer | $3,629,433 |
| PayPal | $2,820,265 |

### Average Expenses by Department
| Department | Avg. Expenses per Transaction |
|---|---|
| HR | $17,352 |
| Operations | $17,174 |
| IT | $16,811 |
| Sales | $16,628 |
| Marketing | $16,478 |
| Finance | $15,749 |

---

## How to Use the Dashboard

1. **Open the file** in Microsoft Excel (2016 or later recommended for full PivotChart and slicer support).
2. **Navigate to the `Dashboard` sheet** to view the interactive visualisations.
3. Use any **slicers or filters** on the Dashboard to drill down by region, department, customer segment, or date range.
4. The PivotTables in Sheets 1–5 update automatically when the underlying `Data` sheet is refreshed.

### Refreshing Data
- To update all PivotTables after editing the `Data` sheet: go to **Data → Refresh All** (or press `Ctrl+Alt+F5`).

---

## Notes

- Profit can be negative for individual transactions (where Expenses exceed Revenue).
- The `Discount` column is stored as a decimal (0.0–1.0), not a percentage.
- Sheet names `Sheet1` through `Sheet5` are the backing PivotTable sheets for the dashboard charts — avoid renaming or deleting them.
