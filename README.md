# Chocolate Sales Analysis

### Project Overview
This data analysis project aims to provide insights about Chocolate Sales for a period of two years. By analyzing various aspects of this Chocolate Sales data, we seek to indentify trends, make data driven recommedations, and gain deeper understanding of company performance. The analysis is broken down into four parts:
- **Overoll Business Summary**
- **Geographical Performance**
- **Team and People Performance**
- **Product Performance**

### Data Sources
Sales Data: The primary data source used is "sales_data.xlsx" file with four tables:
1. **Sales Data:** contains all records of all sales made indicating the amount of sale, boxes of chocolates sold and also the number of customers who bought. Also it shows the salesperson who made the sale, the geography where the sale was made and the date.
2. **Product Data:** containts all the different products availaible their respective categories, size and cost per box.
3. **Location Data:** contains geographical information of countries and regions.
4. **People Data:** contains information about the sales persons and their respective teams

### Tools
- Microsoft Excel- Data Cleaning, Analysis and Visualisation [Download Here](https://www.microsoft.com)

### Data Cleaning and Preparation
In this phase I performed the following tasks:
1. Data Inspection and Relationship Creation of the four tables using their common linking columns
2. Data Calculations

### Explatory Data Analysis
EDA involved exploring the sales data to answer key questions, such as:
1. What is the total sales, boxes, shipments, cost, profit and profit percentage for overoll level and also specific category?
2. What is the Month on Month sales, boxes, cost, profit and profit percentage for overoll level and also specific category?
3. What is the best and worst countries based on sales and profit percentage?
4. How is the team performance based on sales and profit?
5. Who is the best sales person based on sales, profit, profit in a given team?
6. How is the performance of total shipments, sales, boxes per sales person in the last 28 days?
7. How is individual category performance based on profit, profit percentage and total sales?
8. How is the product performace in each category based on total sales, boxes sold, shipments, profit percentage?
9. How is the performance of shipments, sales, boxes of individual product in the last 28 days?

### Data Analysis
```Excel
=CHOOSE($AG$137,COUNTIFS(sales[Product],$AF140#,sales[Date],AG$139)>0,
SUMIFS(sales[Amount],sales[Product],$AF140#,sales[Date],AG$139),
SUMIFS(sales[Boxes],sales[Product],$AF140#,sales[Date],AG$139),
COUNTIFS(sales[Product],$AF140#,sales[Date],AG$139))
```
```
=SORTBY(O140:S161,M140:M161,-1,INDEX(O140:S161,,K148),K150)
```
```
=CHOOSE($Q$98,COUNTIFS(sales[Sales Person],$R91#,sales[Date],S$90)>0,
SUMIFS(sales[Amount],sales[Sales Person],$R91#,sales[Date],S$90),
SUMIFS(sales[Boxes],sales[Sales Person],$R91#,sales[Date],S$90),
COUNTIFS(sales[Sales Person],$R91#,sales[Date],S$90))
```
```
=SORT(FILTER(D91:G115,C91:C115=selected.team),$Q$111,$Q$114)
```
### Recommedations
1. Focus on reducing the cost for Bites and Others Category.
2. More marketing efforts should be invested on the Bites and others categories in order to increase sales.

### Results and Findings
Based on the analysis, results are summarized as follows:
1. All product categories the sales, profit, boxes, shipments and cost have increased based on previous year, except profit percentage for Bites and Others which reduced.
2. On teams the Tempo sales are the lowest and Yummies highest
3. New Zealand is the best country in terms of sales and USA in terms of Profit Percentage
4. In terms of Profit percentage most products are above the 40% mark.

### References
[Excel Documentation](https://learn.microsoft.com/en-us/office/client-developer/excel/excel-home)
