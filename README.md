# ETL-Sales-Dataset
### Objective:
> Develop an ETL pipeline to efficiently extract, transform, and load sales data, ensuring clean, structured datasets for streamlined business operations.  

### EXTRACT CSV File
- Download the CSV file from Kaggle: [Download the File Here](https://www.kaggle.com/datasets/shantanugarg274/sales-dataset)
- Anaconda Navigator GUI  Anaconda Navigator is a graphical user interface
> making it easier to manage Python environments and packages without using the command line.
- Jupyter Notebook (Not a full-fledged IDE - Integrated Development Environment)
> IDE is a software application that provides a comprehensive set of tools for coding, debugging, and testing programs.
- Use Python's pandas library to read the data.
![Read CSV](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/Read%20CSV.png)
- Full DataFrame (Cost Column included)
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
### LOAD
- Create a Connection to MySQL
> Use SQLAlchemy to connect to MySQL database.
![Create Connection](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/create%20connection.JPG)
- Load DataFrame into MySQL
> Use .to_sql() to insert your DataFrame into MySQL:
![Load to MySQL](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/load%20record.JPG)
> sales_table → Name of the table in MySQL  
> if_exists= 'replace' → Replaces the table if it already exists  
> index=False → Prevents Pandas from adding an extra index column
- Verify Data in MySQ
> Run this SQL query in MySQL Workbench to check.  
 > SELECT * FROM etl (table name).
![Check MySQL](https://github.com/EricDataAnalyst/ETL-Sales-Dataset/blob/main/check%20dataframe.JPG)

##### This ETL pipeline streamlines data processing, unlocking valuable insights to drive business growth and smarter decision-making.

---

<p align="left">
  © 2025 Eric | All Rights Reserved
  
  ### Let's connect! Contact me here.

  <a href="https://www.linkedin.com/in/eric-va/">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" width="20" height="20">
  </a>
  <br>
  <a href="mailto:erdejesus1994@gmail.com">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/google/google-original.svg" width="20" height="20">
  </a>
</p>
