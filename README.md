# Northwind.DB

**Author:** Luka Gelashvili  
**Purpose:** Power BI portfolio project (Northwind dataset). Multi-version development showing progressive pages, model, and full set of measures. Built to demonstrate data modeling, DAX, and dashboard storytelling.

---

## Repository contents

- `MEASURES.csv`  
  All DAX measures used in the project (export of the model measures for review / reproducibility).

- `Northwind.09.12.25.pbix`  
  First version — **Executive Sales** page only.

- `Northwind.09.16.25.pbix`  
  Executive Sales + **Current Year** page (current vs LY comparisons).

- `Northwind.09.21.25.pbix`  
  Executive Sales + Current Year + **Customer Analysis**.

- `Northwind.09.22.25.pbix`  
  Adds **Employee** (HR) page to prior pages.

- `Northwind.09.23.25.final.pbix`  
  Final version — includes **Products & Categories** and **Orders / Operations** pages (complete report).

- `model.png`  
  Screenshot of the data model (star schema & relationships).

- `Screenshots.final.pdf`  
  PDF with exported screenshots of final pages (for portfolio & review).

---

## What each report page shows (high level)
- **Executive Sales** — company level KPIs and trends (sales, orders, AOV, YoY, month-to-month).
- **Current Year** — snapshot and quick health indicators (latest-date comparisons vs LY).
- **Customer Analysis** — cohorts, active customers, repeat purchase, segmentation.
- **Employee (HR)** — headcount, tenure, employee sales performance.
- **Products & Categories** — product/category performance, contribution analysis.
- **Orders / Operations** — order lead times, fulfillment KPIs, operations insights.

---

## Data model & naming conventions
Model built as a star schema. Main tables & notable columns (use these names when writing DAX):

- **Fact table:** `FactsTable`  
  Important columns: `OrderDate`, `OrderDateOnly`, `OrderID`, `OrderMonth`, `OrderMonthNumber`, `OrderMonthName` (`MonthShort`), `OrderYear`, `LineTotal`, `UnitPrice`, `Quantity`, `ProductID`, `ProductName`, `ShippedDate`, `ShipCountry`, `ShipCity`, `SupplierID`, `MonthNum`

- **Dimensions:** `DimCustomers`, `DimEmployee`, `DimSuppliers`, `DimShippers`, `orders`

- **Measures table:** `Measures` (container for measures; folders created per page)

---

## How to open & inspect
1. Install **Power BI Desktop** (latest stable version recommended).  
2. Open the desired `.pbix` file (each PBIX is a checkpoint/version). Data is embedded — you can explore visuals, model, and DAX in Power BI Desktop.
3. To explore the model visually, open `model.png` or open Model view in Power BI Desktop.


