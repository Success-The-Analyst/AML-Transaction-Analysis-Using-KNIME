AML Transaction Analysis Using KNIME

📌 Project Overview

This project uses KNIME Analytics Platform to analyze anti-money laundering (AML) transactions based on a dataset of financial transactions from Canadian provinces. The goal is to identify suspicious transactions, detect high-risk customers, and generate automated reports for compliance and regulatory monitoring.

📂 Dataset

File: aml_canadian_transactions.csv

Columns:

Transaction_ID: Unique identifier for each transaction

Customer_Name: Name of the customer

Province: Canadian province of transaction

Transaction_Amount: Amount in CAD

Transaction_Type: Type of transaction (Wire Transfer, Crypto, etc.)

Risk_Level: Risk rating (Low, Medium, High)

AML_Flag: 1 = Suspicious, 0 = Normal

🛠 Tools & Technologies

KNIME Analytics Platform (Data processing & analysis)

Excel Writer (Saving flagged transactions)

Rule Engine & Filters (Identifying suspicious transactions)

Bar Chart Node (Data visualization)

Send Email Node (Automated alerts)

KNIME WebPortal (Dashboard deployment)

🚀 Steps to Run the Workflow

1. Import Data

Open KNIME Analytics Platform.

Drag & drop a CSV Reader node.

Select aml_canadian_transactions.csv and execute the node.

2. Data Cleaning & Preparation

Use Missing Value node to fill missing values.

Use String to Number node to convert Transaction_Amount to numeric.

Normalize province names using String Manipulation node.

3. Identifying High-Risk Transactions

Apply Row Filter node to keep transactions above $10,000.

Use Rule-Based Row Filter node to filter high-risk customers.

Implement Rule Engine node to flag transactions involving Crypto and large Cash Deposits.

4. Reporting & Visualization

Use GroupBy node to summarize transactions by province & risk level.

Save flagged transactions using Excel Writer.

Generate a Bar Chart for high-risk transactions per province.

5. Automate & Deploy

Schedule Execution using KNIME Server.

Send Email Alerts for flagged transactions using Send Email node.

Deploy Dashboard using KNIME WebPortal Output node.

📊 Expected Outputs

Filtered High-Risk Transactions List

Excel Report of Suspicious Transactions

Visual Dashboard for AML Monitoring

Automated Email Alerts for Compliance Teams

📌 Future Enhancements

Integrate real-time data sources (SQL, APIs).

Implement machine learning models for fraud detection.

Enhance risk scoring algorithms using AI.
