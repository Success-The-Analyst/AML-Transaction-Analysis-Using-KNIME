# AML Transaction Analysis Using KNIME

## 📌 Project Overview
This project uses **KNIME Analytics Platform** to analyze **anti-money laundering (AML) transactions** based on a dataset of financial transactions from Canadian provinces. The goal is to **identify suspicious transactions, detect high-risk customers, and generate automated reports** for compliance and regulatory monitoring.

## 📂 Dataset
- **File:** `aml_canadian_transactions.csv`
- **Columns:**
  - `Transaction_ID`: Unique identifier for each transaction
  - `Customer_Name`: Name of the customer
  - `Province`: Canadian province of transaction
  - `Transaction_Amount`: Amount in CAD
  - `Transaction_Type`: Type of transaction (Wire Transfer, Crypto, etc.)
  - `Risk_Level`: Risk rating (Low, Medium, High)
  - `AML_Flag`: 1 = Suspicious, 0 = Normal

## 🛠 Tools & Technologies
- **KNIME Analytics Platform** (Data processing & analysis)
- **Excel Writer** (Saving flagged transactions)
- **Rule Engine & Filters** (Identifying suspicious transactions)
- **Bar Chart Node** (Data visualization)
- **Send Email Node** (Automated alerts)
- **KNIME WebPortal** (Dashboard deployment)

## 🚀 Steps to Run the Workflow

### **1. Import Data**
1. Open **KNIME Analytics Platform**.
2. Drag & drop a **CSV Reader** node.
3. Select `aml_canadian_transactions.csv` and execute the node.

### **2. Data Cleaning & Preparation**
1. Use **Missing Value** node to fill missing values.
2. Use **String to Number** node to convert `Transaction_Amount` to numeric.
3. Normalize province names using **String Manipulation** node.

### **3. Identifying High-Risk Transactions**
1. Apply **Row Filter** node to keep transactions above $10,000.
2. Use **Rule-Based Row Filter** node to filter high-risk customers.
3. Implement **Rule Engine** node to flag transactions involving `Crypto` and large `Cash Deposits`.

### **4. Reporting & Visualization**
1. Use **GroupBy** node to summarize transactions by province & risk level.
2. Save flagged transactions using **Excel Writer**.
3. Generate a **Bar Chart** for high-risk transactions per province.

### **5. Automate & Deploy**
1. **Schedule Execution** using KNIME Server.
2. **Send Email Alerts** for flagged transactions using **Send Email** node.
3. **Deploy Dashboard** using **KNIME WebPortal Output** node.

## 📊 Expected Outputs
- **Filtered High-Risk Transactions List**
- **Excel Report of Suspicious Transactions**
- **Visual Dashboard for AML Monitoring**
- **Automated Email Alerts for Compliance Teams**

## 📌 Future Enhancements
- **Integrate real-time data sources (SQL, APIs).**
- **Implement machine learning models for fraud detection.**
- **Enhance risk scoring algorithms using AI.**

---
✅ **Follow these steps and run your first KNIME AML analysis today!** 🚀

