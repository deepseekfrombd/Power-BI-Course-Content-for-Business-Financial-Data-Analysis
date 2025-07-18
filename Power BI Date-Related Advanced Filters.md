# 📆 Power BI Date-Related Advanced Filters (Bangla Tutorial)

---

## 🔹 1. Basic Date Filters

- **Date is** → On, Before, After  
- **Between** → Two fixed dates

⏳ **Example**:  
Filter records between `01-Jan-2023` and `31-Dec-2023`.

---

## 🔹 2. Relative Date Filtering (Dynamic)

এটি `Today`, `This week`, `Last 7 days`, `Next 30 days` ইত্যাদি দিয়ে কাজ করে।

📘 **Found in**:  
➡ Visual Filter Pane → Date field → “Relative Date”

| Filter Type     | Example                   | Meaning                                |
|-----------------|---------------------------|----------------------------------------|
| Last 7 days     | OrderDate → Last 7 days   | Today থেকে আগের ৭ দিন পর্যন্ত          |
| Next 30 days    | DueDate → Next 30 days    | আজ থেকে আগামি ৩০ দিন পর্যন্ত          |
| This Month      | InvoiceDate → This Month  | চলতি মাসের সব রেকর্ড                   |
| Last Year       | SalesDate → Last Year     | গত বছরের ডেটা                         |

✅ Dynamic → Always updates based on current day.

---

## 🔹 3. Top N Filter on Date Hierarchy

Use this to get latest/top dates.

**Steps**:
1. Drag Date to axis (or filter)
2. Go to filter pane → select **Top N**
3. Enter number (e.g., `3`), sort by measure (e.g., `Sales`), choose Top/Bottom

✅ **Example**: Top 3 months with highest sales.

---

## 🔹 4. Using DAX for Date Filtering

You can create calculated columns/measures for flexible filtering.

✅ **Last 30 Days Flag (DAX)**

```dax
IsLast30Days = 
IF(
    'Sales'[Date] >= TODAY() - 30 && 'Sales'[Date] <= TODAY(),
    "Yes", "No"
)

# 🧠 Top N Item Filter in Power BI (Bangla + English)

## 📌 Objective (উদ্দেশ্য)
Use **Top N Filter** in Power BI to show only the highest-ranked items — such as top 5 selling products or top 10 customers — in visuals like bar charts, tables, or matrices.

---

## ✅ Step 1: Create a Measure

**Example**: For Total Sales

```dax
Total Sales = SUM(Sales[Amount])


TopN Filtered Sales = 
VAR TopNValue = SELECTEDVALUE(TopNSelector[TopNSelector])
RETURN
IF(
    RANKX(ALL(Sales[Product]), [Total Sales]) <= TopNValue,
    [Total Sales]
)

