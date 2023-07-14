# Power BI Report Samples

Welcome to the Power BI Report Samples repository! Here you will find a collection of sample reports showcasing various data analysis scenarios and demonstrating the usage of DAX formulas. These reports are designed to help you learn and explore the capabilities of Power BI.

## Report List

### 1. Sales Performance Dashboard

This dashboard provides an overview of sales performance for different regions and product categories. It includes visualizations such as sales by region, top selling products, and year-over-year sales growth. The following DAX formulas were used:

- **Total Sales**: `Total Sales = SUM(Sales[Amount])`
- **Year-over-Year Growth**: `YoY Growth = DIVIDE(SUM(Sales[Amount]), CALCULATE(SUM(Sales[Amount]), SAMEPERIODLASTYEAR(Dates[Date]))) - 1`

### 2. Customer Segmentation Analysis

This report analyzes customer segmentation based on their purchasing behavior. It includes visualizations like customer distribution, average purchase value, and customer lifetime value. The following DAX formulas were used:

- **Purchase Frequency**: `Purchase Frequency = COUNTROWS(Sales) / DISTINCTCOUNT(Sales[CustomerID])`
- **Customer Lifetime Value**: `CLTV = SUMX(Sales, [Average Order Value] * [Purchase Frequency] * [Average Customer Lifespan])`

### 3. Inventory Management Dashboard

This dashboard provides insights into inventory levels and stock movement. It includes visualizations such as current stock levels, stock turnover rate, and top-selling products. The following DAX formulas were used:

- **Stock Turnover Rate**: `Stock Turnover Rate = DIVIDE(SUM(Sales[Quantity]), SUM(Inventory[Stock]))`
- **Average Days to Sell**: `Avg Days to Sell = DIVIDE(DISTINCTCOUNT(Dates[Date]), SUMX(Inventory, IF([Stock]>0, 1, 0)))`

## Getting Started

1. Clone or download the repository to your local machine.
2. Open the Power BI Desktop application.
3. Select "Open" and navigate to the downloaded report (.pbix) file.
4. Explore the report visuals, filters, and interactions.
5. Review the DAX formulas in the "Fields" pane and the "Modeling" tab.

Feel free to customize and enhance these reports to suit your specific needs. We hope these samples inspire you to unlock the full potential of Power BI for your data analysis projects!

If you have any questions or suggestions, please feel free to reach out. Happy analyzing with Power BI!

