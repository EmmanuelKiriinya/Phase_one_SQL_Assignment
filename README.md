# Phas 1 SQL: International Debt Analysis Using SQL
## Overview
In this project, we are going to analyze international debt data collected by The World Bank. The dataset contains information about the amount of debt (in USD) owed by different countries across several categories. Obtain the international debt file from <a href = https://github.com/LuxDevHQ/Data-Analytics-Boot-camp-Projects/blob/main/international_debt_with_missing_values.csv> international_debt_with_missing_values. <a/><br/>
The following dataset has the following columns:
- country_name varchar
- country_code varchar
- indicator_name varchar
- indicator_code varchar
- debt float

### Tools used:  
- PostrgreSQL for Database Management
- DBeaver for query execution and database administration
- SQL as the query language
  
By the use of SQL queries, we will have a deeper understanding of the dataset. To be able to answer the questions, we need to have an overview of how the dataset looks like by querying the select all statement, more of reconnaissance.
```
  SELECT *
    FROM assignment.international_debt_with_missing_values;
```
**Note:** `assignment` is the Schema.  
 ## Let's answer the following key questions:
   
  ### What is the total amount of debt owed by all countries in the dataset?
As viewed during 'reconnaissance', there are different types/ categories of debt taken by different countries. To know the sum of all debt recorded, use the `SELECT` statement with the aggregate function `SUM` for the debt column.  
![A screenshot of an SQL query on the total debt owed by all countries](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q1.png)

### How many distinct countries are recorded in the dataset?  
When retrieving data, we realize a country might appear multiple times depending on the types of debts owed. Counting them as they appear on the dataset might bring undesired results during statistical analysis. In this section, we will be able to view unique countries without counting the same country repeatedly.  
![A screenshot of an SQL query on the distinct number of countries](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q2.png)

### What are the distinct types of debt indicators, and what do they represent?
Now we know the number of countries in the dataset, what of the number of unique debt indicators? The columns indicator_name and indicator_code represent different debt indicators, in this section we will be using either of them to know various unique debt indicators we have.  
![A screenshot of an SQL query on the distinct number of debt indicators](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q3.png)  

### Which country has the highest total debt, and how much does it owe?
Now that we have the exact total of the amounts of debt owed by several countries, let's find out the country that owes the highest amount of debt along with the amount(The cumulative debt owed across all debt_indicators).  
![A screenshot of an SQL query on the country with the highest debt owed](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q4.png)  

### What is the average debt across different debt indicators?  
Now that we have an idea of some of the data's summary, let's dig deeper and see the average debt across various debt indicators.  
![A screenshot of an SQL query on the average debt across different debt indicators](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q5.png)  

### Which country has made the highest amount of principal repayments?
In the distinct number of debt indicators, there's one that is named `Principal Repayments`. We'd like to know which country owes the highest amount in this category. When unsure of the preceding and following characters, we use the `%` popularly known as a percent sign but we'll call it a wildcard for our context.  
![A screenshot of an SQL query on which country has the highest amount of principal repayments](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q6.png)  

### What is the most common debt indicator across all countries?
  Now we find out the type of debt indicator that has the highest appearance across all the countries.  
  ![A screenshot of an SQL query on the most common debt indicator across all the countries](https://github.com/EmmanuelKiriinya/Phase_one_SQL_Assignment/blob/main/images/q7.png)  
