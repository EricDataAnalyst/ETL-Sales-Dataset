# ETL-Sales-Dataset
### Problem Statement for the ETL Project:
> How can a business use raw sales transaction data to gain actionable insights that improve decision-making?
### Objective:
> Build an ETL pipeline to collect, clean, and organize sales data, then use it to analyze performance trends, customer behavior, and product performance. The goal is to help the business make data-driven decisions.
### Business Problems We're Solving:
#### Sales Performance Analysis
- Which months or days are high-performing?
- Are sales improving over time?
#### Top & Poor Performing Products
- Which products bring the most revenue?
- Which products have high return or low sales?
#### Customer Insights
- Who are the top customers?
- What products do they frequently buy?
#### Purchase Patterns
- Are there seasonal trends?
- Do discounts increase sales volume?
#### Inventory & Category Demand
- Which product categories need restocking more often?
- Which items have low or no movement?
####Revenue Optimization
- How do discounts affect total revenue?
- Is there a correlation between quantity and total sales?
### EXTRACT CSV File
- Download the CSV file from Kaggle: [Download the File Here](https://www.kaggle.com/datasets/shantanugarg274/sales-dataset)
- Anaconda Navigator GUI  Anaconda Navigator is a graphical user interface
> making it easier to manage Python environments and packages without using the command line.
- Jupyter Notebook (Not a full-fledged IDE - Integrated Development Environment)
> IDE is a software application that provides a comprehensive set of tools for coding, debugging, and testing programs.
- Use Python's pandas library to read the data.
![Read CSV](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/Read%20CSV.png)
- Full DataFrame (COst Column included)
![DataFrame](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/Full%20Dataset.png)

### TRANSFORM Dataset
- Added a Cost column for clarity, showing the origin of Profit.
> This will give us the total cost for that row (not per item).
![Cost Column](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/Cost.png)
> Move the Cost column so that it appears directly after the Profit column.
![Move Column](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/Move%20cost%20next%20to%20profit.JPG)
- Drop Year-Month Column
> Since the **OrderDate** column already contains the **Year-Month** information, keeping both would be redundant. Removing the **Year-Month** column helps optimize storage when uploading the dataset to the database.
![Drop Y-M col](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/Drop%20Y-M%20col.JPG)
- Checking and Correcting Data Types in a Pandas DataFrame
> Convert Order ID to string<br>
> Convert Amount to float<br>
> Convert Profit to float<br>
> Convert Cost to float<br>
> Convert Quantity to float<br>
> Convert Order Date to datetime
![Convert](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/change%20data%20type.JPG)
- Change Column Name
> Order ID = OrderID<br>
> Order Date = OrderDate
![Column Name](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/column%20name.JPG)
