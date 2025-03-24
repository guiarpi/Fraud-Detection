# Fraud-Detection
In this project, there are 3 pieces of code related to Fraud Detection:

1) Stored Procedure for Fraud Detection in PostgreSQL 
2) Machine Learning-Based Fraud Detection PostgreSQL + Python
3) Automate Fraud Reports sending email alerts automatically

## 1. Creating a Stored Procedure for Fraud Detection in PostgreSQL (running in Python)
### Step 1: Connecting to PostgreSQL in Jupter notebook
    Installing ipython-sql package,
    Connecting to the default database,
    Connecting to the PostgreSQL server,
    Creating the new database,
    Connecting to the new database using ipython-sql.
    
### Step 2: Create a Fraud Detection Table
    Creating the schema and table,
    Inserting Sample Transactions.

### Step 3: Identify Suspicious Transactions
    Rule-Based Fraud Detection Look for high-value transactions,
    Multiple Transactions in a Short Time (Velocity Check),
    Location Anomaly Detection Find customers who made transactions from different locations within 1 hour.

### Step 4: Mark Fraudulent Transactions
    Updating the table to flag suspicious transactions.

### Step 5: Automate Fraud Detection with a Stored Procedure
    Creating a Stored Procedure to automate fraud detection


## 2. Machine Learning-Based Fraud Detection
### Step 1: Connecting to PostgreSQL
    Importing create_engine and pandas libraries
    Using connect_db() to connect to PostgreSQL
    
### Step 2: Load Data from PostgreSQL
    Using load_data() and querying SQL via Python syntax instead of using %load_ext sql

### Step 3: Train Fraud Detection Model
    Setting the features
    Splitting the data into test and training sets
    Fitting the model
    Checking accurary

### Step 4: Predict Fraud for New Transactions and Store in PostgreSQL
    Creating a function to update database 
    Running the fraud detection pipeline

### Step 5: Automate Fraud Detection with a Stored Procedure
    Creating a Stored Procedure to automate fraud detection

## 2. Automating Fraud Reports
### Step 1: Loading PostgreSQL 
    Installing ipython-sql package,
    Connecting to the default database,
    Connecting to the PostgreSQL server,
    Creating the new database,
    Connecting to the new database using ipython-sql.
    
### Step 2: Create a Transactions Table 
    Using CREATE TABLE IF NOT EXIST clause

### Step 3: Self-Join Query to Detect Suspicious Transactions
    Using self-joins the transactions table to find cases where a customer made transactions in different locations within a short time (1 hour)

### Step 4: Create Fraud Features Table
    Using subquery 

### Step 5: Create Fraud Reports Table
    Using CREATE TABLE IF NOT EXIST clause

### Step 6: Create a Stored Procedure to Generate Fraud Reports
    Using CREATE OR REPLACE FUNCTION clause
    Getting total transactions
    Getting total fraudulent transactions
    Calculating fraud percentage using IF ELSE clause

### Step 7: Automate Fraud Report Generation with Cron Job
    This step to be followed on Terminal (on Mac)

### Step 8: Create Fraud Alerts Table
    Using CREATE TABLE IF NOT EXISTS clause 

### Step 9: Create a Stored Procedure to Generate Fraud Alerts
    Using CREATE OR REPLACE FUNCTION clause
    Getting latest fraud percentage
    Inserting an alert if fraud exceeds 10% using IF clause

### Step 10: Automate Fraud Alerts with Cron Job
    This step to be followed on Terminal (on Mac)
