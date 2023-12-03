# AtliQ-Sales-Insight_Data_Analysis-using_MySQL_and_Tableau

## OVERVIEW:

       PROJECT NAME

       PROBLEM STATEMENTS

       APPROACH - PROJECT PLANNING & AIMS GRID

       DATA ANALYST APPROACH

       DATA ANALYSIS USING SQL

       DATA ANALYSIS USING TABLEAU

       NOTE


## PROJECT NAME:

### ATLIQ SALES INSIGHT – DATA ANALYSIS USING SQL AND TABLEAU

### About Project:
    •	Performed Data Cleaning, Analysis, and Visualization on India-based hardware company sales insights.

    •	Developed ETL mappings using SQL to extract the data from unstructured data and 
            transformed it to the staging area to conduct data cleaning and design star 
            schema data model on Tableau.

    •	Developed a Tableau dashboard to perform analysis, producing quantitative visualizations 
            in Tableau to draw valuable insights based on different parameters affecting the company 
            performance year on year and further provide business solutions.



### About AtliQ:

    •	AtliQ Hardware is a Computer Hardware and peripheral Manufacturer company.

### Tools Used:
    •	Advance Excel

    •	SQL | MySQL

    •	Tableau

    •	Statistics


## PROBLEM STATEMENTS:

The sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.
   
    Q1. Revenue breakdown by cities.

    Q2. Revenue breakdown by years & months. 

    Q3. Top 5 customers by revenue & sales quantity.

    Q4. Top 5 Products by revenue.

    Q5. Net Profit & Profit Margin by Market.


## APPROACH - PROJECT PLANNING AND AIMS GRID

   1. Purpose: What? Why? What do we want to achieve?


          To unlock sales insights that were not visible before to the sales team for decision support 
          & automate them to reduce manual time spent in data gathering.
   
   
   2. Stakeholders: Who will be involved?

          •	Sales Director
          •	I.T. Team
          •	Customer Service Team
          •	Data & Analytics Team


    3. End Result: What do we want to achieve?

          An automated dashboard providing quick & latest sales insights to support data-driven decision-making.
                 
    
    4. Success Criteria: What will be our success criteria?

          •	Dashboards are uncovering sales order insights with the latest data available.
          •	Sales team able to make better decisions & prove 10% cost savings of total spend.
          •	Sales analysts manually stop data gathering to save 20% off. 


# DATA ANALYST APPROACH:
![flow](https://github.com/AnandSheel/AtliQ_Sales_Insight_Data_Analysis-using_MySQL_and-Tableau/assets/149947209/1d3c94f3-19b7-4cbd-80f8-2ccb2e12bda4)


#### Setup Process:

    •	Step 1: Download file: db_dump.sql or db_dump.xlsx.

    •	Step 2: Import it in MySql do ETL(Extract, Transform, Load) if required.

    •	Step 3: Download Tableau Public (Free) or Tableau Desktop (14 days trial) to perform Data Analysis.

    •	Step 4: Connect Tableau with MySql database or Excel database.

    •	Step 5: Save the file as (.twb or .twbx).


# DATA ANALYSIS USING SQL:


     • Show all customer records
           
           SELECT * FROM customers;

     • Show the total number of customers
           
           SELECT count(*) FROM customers;

     • Show transactions for the Chennai market (market code for Chennai is Mark001)
           
           SELECT * FROM transactions where market_code='Mark001';

     • Show distinct product codes that were sold in Chennai.
           
           SELECT distinct product_code FROM transactions where market_code='Mark001';

     • Show transactions where the currency is US dollars.
           
           SELECT * from transactions where currency="USD"

     • Show transactions in 2020 join by date table.
            
           SELECT transactions., date. FROM transactions INNER JOIN date ON 
           transactions.order_date=date.date where date.year=2020;

     • Show total revenue in the year 2020.
           
           SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date 
           where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

     • Show total revenue in the year 2020, January Month.
    
           SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date 
           where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");


# DATA ANALYSIS USING TABLEAU:

    Tableau Public Dashboards: Revenue & Profit Analysis Tableau Creating Star Schema in Tableau


![Screenshot 2023-12-03 234500](https://github.com/AnandSheel/AtliQ_Sales_Insight_Data_Analysis-using_MySQL_and-Tableau/assets/149947209/24acbd85-0889-4758-9347-dee1d9fd0e71)


## Tableau Dashboard: Revenue Analysis
![Screenshot 2023-12-03 235044](https://github.com/AnandSheel/AtliQ_Sales_Insight_Data_Analysis-using_MySQL_and-Tableau/assets/149947209/bcd59cd6-179d-45a1-9934-82765df80a70)


## Tableau Dashboard: Profit Analysis
![Screenshot 2023-12-03 235357](https://github.com/AnandSheel/AtliQ_Sales_Insight_Data_Analysis-using_MySQL_and-Tableau/assets/149947209/a9c527f1-9011-45e7-bd79-942403fb0f49)


# RECOMMENDATION:

Based on dashboard insights:

    1. Maintain a healthy relationship with the customers in Bhubaneshwar, Hyderabad, and Chennai as they have the highest profit % by market.
   
    2. Make some strategy for the Lucknow market as its revenue is less and also profit % is negative.
    
    3. Figure out what needs to be done as sales quantity in Kanpur, Surat, Patna, Bhubaneshwar, and Chennai are the lowest.
    
    4. The north zone has the highest revenue contribution but the lowest profit % whereas the South zone has the lowest revenue contribution but highest 
       profit %. Try to increase customers in the South zone.
    
    5. Delhi is the highest revenue contributor and second highest profit contributor whereas Mumbai is the second highest revenue contributor 
       and highest profit contributor. So it needs to implement the same market strategy as in Mumbai to increase the profit % in Delhi.






    
