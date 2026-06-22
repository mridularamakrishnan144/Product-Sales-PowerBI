# Product Sales Power BI Report

## Overview
A three-page interactive Power BI report analyzing product sales, 
performance, and profitability built using a star schema data model 
with DAX measures.

## Data Model
- **Sales** (Fact Table) — order transactions with revenue, cost, quantity
- **Product** (Dimension Table) — product details, category, subcategory, color
- Relationship: Sales[ProductKey] → Product[ProductKey] (Many-to-One)

## Report Pages

### Page 1 — Sales Overview
- KPI Cards: Total Sales, Total Cost, Total Profit, Total Quantity
- Line Chart: Sales vs Profit trend over time
- Bar Chart: Sales and Profit Margin % by Category

### Page 2 — Product Analysis
- Top 10 Products by Total Sales
- Treemap: Sales breakdown by Category and Subcategory
- Bar Chart: Sales by Color

### Page 3 — Profitability
- Clustered Column Chart: Sales vs Cost by Category
- Bubble Chart: Unit Price vs Quantity sized by Total Sales
- Matrix Table: Category-level Sales, Cost, Profit, Profit Margin %

## DAX Measures
- `Total Sales = SUM(Sales[Sales])`
- `Total Cost = SUM(Sales[Cost])`
- `Total Profit = [Total Sales] - [Total Cost]`
- `Total Quantity = SUM(Sales[Quantity])`
- `Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)`

## Tools Used
- Power BI Desktop (.pbip format)
- Power Query (data transformation and merge)
- DAX (measures and calculations)
- Git + GitHub (version control)

## Key Insights
- Bikes drive the highest revenue but operate at a loss (-1.56% margin)
- Accessories have the best profit margin at 35.29%
- Black colored products outsell all other colors significantly
- Mountain-200 series dominates the top 10 products by sales



