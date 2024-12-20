# Performance Report

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiNWVlNGM1NjQtNjU1Ny00NjgwLWE0OGMtMzc2NDgyN2Q2Y2QzIiwidCI6ImE1MzRkNGVhLTdiN2QtNGJhYy1hMDBmLTFkZTE4OGE4ZTk3MSJ9

## Overview

The Plant Co. Quantity Performance 2024 dashboard provides a comprehensive overview of the company's sales performance, profitability, and other key metrics. It is designed to help stakeholders understand the company's overall financial health and identify areas for improvement.

### Key Features 

- Quantity Performance: The dashboard shows the overall quantity performance for the year, including year-over-year (YTD vs PYTD) comparisons and month-by-month breakdowns.

- Revenue Analysis: It provides a breakdown of revenue by product type, country, and month, allowing for easy identification of top-performing and underperforming areas.

- Profitability Analysis: The dashboard includes gross profit margin calculations and a segmentation of accounts based on profitability.

- Bottom 10 Analysis: A section highlights the bottom 10 performing countries or regions based on YTD vs PYTD performance.

- Account Profitability Segmentation: A scatter plot visualizes the relationship between gross profit percentage and quantity sold for each account.

### Financial Metrics Overview:

- Quantity: Overall quantity sold (YTD vs PYTD)

- Sales: Total revenue generated

- Gross Profit: Total profit before operating expenses

- GP%: Gross profit percentage

- YTD vs PYTD: Year-to-date performance compared to the previous year

### Revenue Breakdown:

- Product Type: Revenue by indoor, landscape, and outdoor products

- Country: Revenue by country or region

- Month: Revenue performance by month

### Product-Specific Metrics (Second Page):

- Product Ratings: Shows customer ratings for different products, helping to assess product quality and customer satisfaction.

- Stock Levels: Displays current stock levels of products, aiding inventory management.

- Cost and Revenue by Product: Provides detailed insights into the cost and revenue generated by each product, helping to identify the most profitable products.

### Data Sources:

- Sales Data: Presumably from the company's sales database or ERP system

- Financial Data: Likely from the company's accounting system or financial reporting software.

### Technical Details:

- Visualization Tools: The dashboard appears to be created using a business intelligence or data visualization tool like Power BI, Tableau, or Qlik.

- Data Model: The underlying data model is likely a relational database that stores information about sales, products, customers, and financial metrics.

- Filters and Slicers: The dashboard likely includes interactive filters and slicers to allow users to drill down into specific data points.

### Following DAX expression was written to calculate YTD, PYTD, GP% & YTD vs PYTD
 

![CARD](https://github.com/user-attachments/assets/84c1c0ba-e196-42ee-ac7c-dc3177d12326)

- #### COGs

        COGs = SUM(FACT_Sales[COGS_USD])

- #### Sales

        Sales = SUM(FACT_Sales[Sales_USD])

- #### Quantity

        Quantity = SUM(FACT_Sales[quantity])

- #### Gross Profit

        Gross Profit = [Sales]-[COGs]
    
- #### YTD
 
        S_YTD = 
        VAR selected_value = SELECTEDVALUE(Slc_Values[Values])
        VAR result = SWITCH(selected_value,
        "Sales", [YTD_Sales],
        "Quantity", [YTD_Quantity],
        "Gross Profit", [YTD_GrossProfit],
        BLANK()
        )
        RETURN
        result

     
- #### PYTD
 
       S_PYTD = 
       VAR selected_value = SELECTEDVALUE(Slc_Values[Values])
       VAR result = SWITCH(selected_value,
       "Sales", [PYTD_Sales],
       "Quantity", [PYTD_Quantity],
       "Gross Profit", [PYTD_GrossProfit],
       BLANK()
       )
       RETURN
       result

- #### GP%

         GP% = DIVIDE([Gross Profit],[Sales])

- #### YTD vs PYTD

         YTD vs PYTD = [S_YTD]-[S_PYTD]   

### Switch for switching between, Gross Profit, Quantity & Sales

![Switch](https://github.com/user-attachments/assets/8a76c0c1-e90e-4bef-beb6-3a8908214b70)
 
 
## Performance Report Dashboard
 
 
![Dashboard](https://github.com/user-attachments/assets/7de1e55b-8b00-4466-821e-74be95d730b4)


# Insights

- Quantity Decline: The overall quantity sold has declined by 12.37K units compared to the previous year.

- Top-Performing Products: Identify the product types or countries that are driving revenue growth.

- Underperforming Regions: Identify regions or countries that are experiencing declining sales or profitability.

- Profitable Accounts: Use the account profitability segmentation to identify accounts with high GP% and quantity sold.

- Seasonal Trends: Analyze monthly revenue data to identify seasonal patterns or fluctuations.

## Financial Metrics

- Gross Profit Margin: Calculate the gross profit margin to assess the company's profitability.

- Revenue Growth: Analyze the year-over-year revenue growth to assess the overall health of the business.

- Cost Analysis: Break down costs by product type, country, or other relevant categories to identify areas for cost reduction.


## Sales Analysis

![image](https://github.com/user-attachments/assets/7775ca00-b23d-4f10-9958-6d45cdaee7b7)

(Based on the provided dashboard, here's a breakdown of Plant Co.'s sales performance)

### Overall Sales Performance
  
- Year-over-Year Decline: Sales have declined by 135.89K units compared to the previous year.

- YTD Sales: Total sales for the year-to-date (YTD) amount to 3.57M units.

- PYTD Sales: Previous year-to-date sales were 3.71M units.

- Gross Profit Margin: The gross profit percentage is 39.15%. 
  
### Sales by Product Type
  
- Indoor: Sales for indoor products have declined.

- Landscape: Sales for landscape products have increased.

- Outdoor: Sales for outdoor products have increased.

- Overall: The increase in landscape and outdoor sales has not offset the decline in indoor sales.

### Sales by Month

- January: Sales were higher than the previous year.

- February: Sales were higher than the previous year.

- March: Sales were higher than the previous year.

- April: Sales were lower than the previous year.

- Overall: The company experienced a strong increase in sales from February to March.
 
### Sales by Country
 
- Canada: Sales have declined.
- Colombia: Sales have declined.
- Croatia: Sales have declined.
- Germany: Sales have declined.
- Hungary: Sales have declined.
- Czech Republic: Sales have declined.
- Greece: Sales have declined.
- Vietnam: Sales have declined.
- South Korea: Sales have declined.
- Kenya: Sales have declined.
- Overall: All countries experienced a decline in sales.
         
### Account Profitability Segmentation

- High GP%, High Sales: There are a few accounts with high gross profit percentages and high sales volumes.
- Low GP%, High Sales: There are several accounts with low gross profit percentages but high sales volumes.
- High GP%, Low Sales: There are a few accounts with high gross profit percentages but low sales volumes.
- Low GP%, Low Sales: There are several accounts with low gross profit percentages and low sales volumes.

### Key Insights

- Sales Decline: The overall decline in sales is a major concern.
- Product Mix: The company should evaluate its product mix and consider opportunities to expand or discontinue product lines.
- Account Profitability: The company should focus on improving the profitability of accounts with low GP%.
- Sales Strategy: The company should review its sales strategy and identify areas for improvement.
- Customer Segmentation: Segmenting customers based on profitability can help the company tailor its marketing efforts and improve customer satisfaction.


(Note: This analysis is based on the provided dashboard and may not capture all relevant factors. Further investigation and analysis may be necessary to gain a deeper understanding of the company's sales performance.)

### General Insights

- Sales Strategy: Evaluate the effectiveness of the company's sales and marketing strategies based on the revenue data.

- Product Mix: Assess the company's product mix and consider opportunities to expand or discontinue product lines.

- Customer Segmentation: Segment customers based on profitability or other criteria to tailor marketing efforts and improve customer satisfaction.

- Operational Efficiency: Analyze operational costs and identify areas for improvement to increase efficiency and profitability.
