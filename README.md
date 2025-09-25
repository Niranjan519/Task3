# Task3
# Coffee Chain Sales Dashboard (Task 3)

The dashboard highlights sales performance, profitability, product trends, and regional insights, enabling informed decision-making.

## Dataset
- **File:** `Coffee_Chain_Sales.csv`
- **Fields used:** Date, Sales, Profit, Quantity, Product, Category, Region/Store

## Key Transformations
- Converted `Date` column to proper Date type.
- Derived `Order Month` and `Order Year` for time-series analysis.
- Ensured `Sales`, `Profit`, and `Quantity` were numeric.
- Aggregated data by month, product, category, and region.

## KPIs
- **Total Sales**
- **Total Profit**
- **Number of Transactions**
- **Average Ticket Value**
- (Optional) Profit Margin %, YoY Growth, MoM Growth

## Dashboard Layout (Power BI)
Refer to `CoffeeChain_Dashboard_Preview.png` for layout mockup.

- **Top Row (Cards):** Total Sales, Total Profit, #Transactions, Avg Ticket  
- **Left Sidebar (Slicers):** Year, Category, Region  
- **Center:** Monthly Sales Trend (Line chart)  
- **Right Column:**  
  - Top: Top Products (Bar chart, Top 10)  
  - Middle: Sales by Category (Bar chart)  
  - Bottom: Sales by Region/Store (Bar chart or Map)  

## Step-by-Step Build Guide
1. **Load Data**
   - Power BI Desktop → Home → Get Data → Text/CSV → select `Coffee_Chain_Sales.csv`.
   - In Power Query: Convert Date column → add Month/Year columns → ensure numeric data types.

2. **Create DAX Measures**
   ```DAX
   Total Sales = SUM(Coffee_Chain_Sales[Sales])
   Total Profit = SUM(Coffee_Chain_Sales[Profit])
   Transactions = COUNTROWS(Coffee_Chain_Sales)
   Avg Ticket = DIVIDE([Total Sales], [Transactions])
   Profit Margin % = DIVIDE([Total Profit], [Total Sales])
   ```

3. **Build Visuals**
   - KPI Cards for measures.
   - Line chart for Monthly Sales.
   - Bar charts for Sales by Category, Top Products, and Sales by Region/Store.
   - Add slicers for Year, Category, Region/Store.

4. **Add Interactivity**
   - Enable cross-filtering between visuals.
   - Use tooltips to show Profit and Profit Margin.

5. **Design & Publish**
   - Apply consistent theme/colors.
   - Add dashboard title: *Coffee Chain Sales Dashboard*.
   - Publish PBIX to Power BI Service for sharing.

## Insights Storyboard
- Monthly sales trend reveals seasonality in performance.
- Certain products drive majority of sales; some show lower margins.
- Regional sales comparison highlights strong vs weak stores/locations.
- High concentration of revenue from top products/customers requires risk management.


