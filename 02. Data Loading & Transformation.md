# Module 2: Data Loading & Transformation with Power Query — Step-by-Step Guide

---

## Step 1: Import Data from Various Sources

- Open Power BI Desktop  
- Click **Get Data**  
- Choose your data source (Excel, CSV, SQL Server, Web, etc.)  
- Browse and select your file or enter connection details  
- Click **Transform Data** to open Power Query Editor  

---

## Step 2: Data Cleansing and Shaping

- In Power Query Editor, review your data preview  
- Remove unwanted columns: Right-click column > **Remove**  
- Remove blank rows or filter out errors:  
  - Use **Remove Rows** > **Remove Blank Rows**  
  - Filter errors by clicking the dropdown on columns  
- Rename columns for clarity by double-clicking the header  

---

## Step 3: Handling Data Types and Columns

- Check column data types (ABC, 123, calendar icon) in header  
- Change data types if needed by clicking the icon > select proper type (Text, Whole Number, Date, etc.)  
- Split columns if necessary (e.g., split date/time or full name) using **Split Column**  

---

## Step 4: M Language Basics for Advanced Transformations

- Access the **Advanced Editor** to view/edit M code  
- Understand the applied steps on the right pane  
- Use M for:  
  - Creating custom formulas  
  - Conditional columns  
  - Complex data manipulations not available via GUI  

---

## Step 5: Creating Custom Columns & Conditional Logic

- In Power Query Editor, click **Add Column** > **Custom Column**  
- Write simple formulas like:  


- Use **Conditional Column** option for GUI-based logic  

---

## Step 6: Merging and Appending Queries

- To combine data from multiple tables:  
- Use **Home** > **Merge Queries** (joins two tables based on matching columns)  
- Use **Home** > **Append Queries** (stack tables vertically)  

---

## Step 7: Refreshing Data and Incremental Refresh Setup

- Click **Close & Apply** to load transformed data into Power BI model  
- To refresh data manually: Click **Refresh** in Power BI Desktop  
- For large datasets: Configure **Incremental Refresh** (requires Power BI Pro and Premium)  
- Define refresh policy on date/time column  
- Only new/changed data will refresh, improving performance  

---

# Summary

By completing Module 2 practice, you will be able to:

- Import and connect to multiple data sources  
- Cleanse and shape data for analysis  
- Handle data types and columns effectively  
- Write and understand basic M language scripts  
- Create custom and conditional columns  
- Merge and append queries for combined datasets  
- Refresh data and setup incremental refresh for efficiency  



