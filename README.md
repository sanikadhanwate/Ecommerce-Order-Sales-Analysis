# Ecommerce-Order-Sales-Analysis
Ecommerce Order Sales Analysis highlights key DAX measures, including Total Sales, Profit, Profit Margin, 90th Percentile Sales, Median Sales, and Average Revenue per Product. It also covers customer count, order metrics, shipping efficiency, and cumulative sales trends.

PowerBI File Link : https://github.com/sanikadhanwate/Ecommerce-Order-Sales-Analysis/blob/2b6cc65292e542b6529b851a774db274af9618da/Excel%20data%201.pbix

Excel sheet : https://1drv.ms/x/c/088fb23c46fc8d10/EZbVuImvcrZJprO1OKeIUNkBO0Km35mIhUwAmfm7kGFVyw?e=phnvjl
### Below is the dashboard showcasing these insights.
![Screenshot 2025-02-08 215808](https://github.com/user-attachments/assets/b0ca2838-0398-4b55-a157-fbba26772f68)

1. **90th Percentile Sales**: Calculates the sales value at the 90th percentile.  

       90th Percentile Sales = PERCENTILEX.INC(Orders,Orders[Sales],0.9)

2. **Average Orders**: Determines the average quantity of products ordered.  

       Average orders = AVERAGE(Orders[Quantity ordered new])

3. **Average Revenue per Product**: Calculates the revenue generated per product on average.  

       Average Revenue per Product = DIVIDE([Total Sales], [Total Product], 0)

4. **Average Sales**: Computes the average sales value.  

       Average Sales = AVERAGE('Orders'[Sales])

5. **Cumulative Sales**: Tracks the running total of sales over time.  

       Cumulative Sales = CALCULATE([Total Sales], FILTER(ALL('Orders'[Order Date].[Date]), 'Orders'[Order Date].[Date] <= MAX('Orders'[Order Date].[Date])))

6. **Earliest Order Date**: Identifies the first recorded order date.  

       Earliest Order Date = MIN('Orders'[Order Date])

7. **Latest Order Date**: Identifies the most recent recorded order date.  

       Latest Order Date = MAX('Orders'[Order Date].[Day])

8. **Median Sales**: Finds the middle value of sales data.  

       Median Sales = MEDIAN('Orders'[Sales])

9. **Number of Customers**: Counts the unique customers.  

       Number of Customers = DISTINCTCOUNT('Orders'[Customer ID])

10. **Number of Orders**: Counts the total number of orders.  

        Number of Orders = COUNT('Orders'[Order ID])

11. **Profit Margin**: Calculates the profit percentage relative to sales.  

        Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

12. **ShipDate/OrderDate**: Measures the difference in days between the order and shipping dates.  

        ShipDate/OrderDate = DATEDIFF(Orders[Order Date].[Day],Orders[Ship Date].[Day],DAY)

13. **Total Products**: Counts the distinct product categories.  

        Total product = DISTINCTCOUNT(Orders[Product Category])

14. **Total Profit**: Sums up the total profit generated.  

        Total Profit = SUM('Orders'[Profit])

15. **Total Sales**: Sums up the total sales revenue.

        Total sales = SUM(Orders[Sales])
