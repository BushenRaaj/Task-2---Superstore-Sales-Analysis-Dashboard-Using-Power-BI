# Superstore Sales Analysis – Power BI Dashboard

## 📌 Project Overview
This project is part of **Task 2: Data Visualization & Storytelling**.  
Using the **Superstore dataset**, I created an interactive dashboard in **Microsoft Power BI** to analyze sales, orders, profit, and customer behavior.  
The dashboard provides insights into **overall sales performance, product sub-categories, customer segmentation, and regional trends**.

---

## 📂 Repository Structure

- [SuperStore Sales Analysis.pbix](SuperStore%20Sales%20Analysis.pbix) → Power BI dashboard file  
- [data/superstore.xls](data/superstore.xls) → Raw dataset  
- [images/Final Dashboard Preview.png](images/Final%20Dashboard%20Preview.png) → Dashboard screenshot  
- [README.md](README.md) → Documentation  

---

## ⚙️ Steps Followed to Build the Dashboard

### 1. Data Loading
- Loaded the **Superstore dataset** into **Power BI Desktop**.  
- Verified column data types (Sales, Quantity, Profit, Discount, etc.).

---

### 2. Data Transformation
- Created a **calculated column**:
  ```DAX
  Final Sp = Orders[Quantity] * Orders[Sales] * (1 - Orders[Discount])
  ```
- Renamed it as **Total SP** for clarity.

---

### 3. Measures Created
Defined new **DAX measures** to calculate key KPIs:
```DAX
Total Sales = SUM(Orders[Sales])
Total Orders = COUNT(Orders[Order ID])
Total Quantity = SUM(Orders[Quantity])
Overall Sales = SUM(Orders[Final Sp])
Total Profit = SUM(Orders[Profit])
```

---

### 4. Dashboard Layout
- **Title**: *Superstore Sales Analysis*  
- **KPI Cards**: Displayed `Total Sales`, `Total Orders`, `Total Quantity`, and `Overall Sales`.  

#### Visuals Added:
1. **Stacked Column Chart**  
   - X-axis: Sub-Category  
   - Y-axis: Overall Sales  

2. **Pie Chart**  
   - Legend: Ship Mode  
   - Values: Total Profit  

3. **Stacked Bar Chart**
   - X-axis: Segment
   - Y-axis: Total Quantity   

5. **Map Visualization**  
   - Location: State  
   - Bubble Size: Total Profit  

6. **Line Chart**  
   - X-axis: Order date ( Year ) 
   - Y-axis: Overall Sales  

7. **Matrix Table**  
   - Rows: Customer Name  
   - Values: Total Orders, Total Quantity, Overall Sales, Total Profit  

8. **Slicers (Filters)**  
   - Category  
   - Product Name  
   - Segment  

---

### 5. Insights Captured
- Sales contribution across product **sub-categories**.  
- Profit distribution by **shipping mode**.  
- Customer order behavior by **segment**.  
- Regional profitability using **map analysis**.  
- Yearly trend of overall sales.  
- Customer-level breakdown with interactive filtering.  

---

## 📊 Final Dashboard Preview

- [images/Final Dashboard Preview.png](images/Final%20Dashboard%20Preview.png)

---

## 📝 Key Learnings
- Creating **calculated columns** and **DAX measures** for KPIs.  
- Designing effective **visual layouts** in Power BI.  
- Applying **filters and slicers** for interactive storytelling.  
- Turning raw sales data into **business insights**.  
