# Power BI for Data Analysts — 4-Week Roadmap

### Learning Objectives

- Clean and model data using Power Query
- Create calculated columns and DAX measures
- Build and publish interactive dashboards
- Tell compelling data stories with Power BI visuals

---

## **Week 1 — Data Preparation & Power BI Basics**
**Goal:** Understand the Power BI ecosystem and learn how to prepare clean, structured data.

### 🔹 Topics
- Power BI interface and workflow (Desktop, Service overview)
- Data import from Excel, CSV, and SQL databases
- Understanding Power Query Editor
- Data profiling (column quality, distribution, profile)
- Cleaning and transforming data:
  - Remove duplicates, split columns, replace values, fill blanks
  - Merge and append queries
- Basic data model setup (naming conventions, data types, relationships)

### 💻 Example Steps
```text
1. Load sales and customer data from Excel.
2. Use Power Query to remove null values and trim text columns.
3. Merge customer info into sales data for enrichment.
4. Load transformed data into the model view.

Week 2 — Data Modelling & DAX Fundamentals

Goal: Build a strong data model and use DAX for calculated columns and measures.

🔹 Topics

Star schema design: fact and dimension tables

Relationships (one-to-many, cross filter direction)

Calculated columns vs. measures

DAX basics:

SUM, AVERAGE, COUNTROWS, DISTINCTCOUNT

CALCULATE, FILTER, ALL

Conditional logic: IF, SWITCH

Time intelligence:

TOTALYTD, SAMEPERIODLASTYEAR, DATEADD

💻 Example DAX

```dax
-- Total Sales
Total Sales = SUM(Sales[SalesAmount])

-- Profit Margin
Profit Margin % = DIVIDE(SUM(Sales[Profit]), SUM(Sales[SalesAmount]))

-- Sales Growth YoY
Sales Growth % = 
VAR CurrentYear = [Total Sales]
VAR LastYear = CALCULATE([Total Sales], DATEADD('Date'[Date], -1, YEAR))
RETURN
DIVIDE(CurrentYear - LastYear, LastYear)
```

Week 3 — Data Visualisation & Interactivity

Goal: Create interactive dashboards that communicate insights effectively.

🔹 Topics

Chart types and when to use them:

Bar/Column, Line, Card, Pie, Map, Matrix

Hierarchies (e.g., Year → Quarter → Month)

Slicers, Filters, and Drill-throughs

Conditional formatting and custom tooltips

Using bookmarks for dynamic storytelling

Syncing slicers across pages

💻 Example Use Cases

```text
1. Create a Sales Overview dashboard with KPIs and region-wise charts.
2. Add a drill-through page for Customer Details.
3. Use slicers to filter by product category and date.
4. Add bookmarks for “Executive View” and “Detailed Analysis”.
```

Week 4 — Dashboard Design, Publishing & Storytelling

Goal: Refine dashboards for clarity, publish them, and share insights effectively.

🔹 Topics

Dashboard layout and design principles:

Consistent alignment, colours, and typography

Clear KPIs at the top, supporting visuals below

Storytelling techniques for business insights

Using Power BI Service:

Publishing reports

Creating and managing workspaces

Sharing dashboards and setting permissions

Report refresh and basic automation

Export options (PDF, PowerPoint, shared link)

💻 Final Project Idea

```text
📊 Build a 2-page Power BI dashboard:
Page 1: Sales Performance Overview
Page 2: Customer Insights (Age, Region, Purchase Trends)

Include:
- DAX-based KPIs (Total Sales, YoY Growth, Top 5 Customers)
- Interactive slicers and bookmarks
- Clean, minimal layout ready for stakeholder presentation
```
