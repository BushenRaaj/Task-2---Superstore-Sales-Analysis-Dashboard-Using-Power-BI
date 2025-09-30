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

<img width="1920" height="1080" alt="Superstore Sales Analysis – Power BI Dashboard" src="https://github.com/user-attachments/assets/efc55f61-f086-4587-ae97-b252d95fec42" />


---

## 📝 Key Learnings
- Creating **calculated columns** and **DAX measures** for KPIs.  
- Designing effective **visual layouts** in Power BI.  
- Applying **filters and slicers** for interactive storytelling.  
- Turning raw sales data into **business insights**.  

## ❓ Interview Questions Related to This Task

### 1. What is the importance of data visualization?
Data visualization helps transform raw data into meaningful insights.  
- Makes complex information easier to understand.  
- Identifies patterns, trends, and outliers.  
- Supports faster and more effective decision-making.  

---

### 2. When do you use a pie chart vs bar chart?
- **Pie Chart** → Best for showing proportions or percentage contribution of categories to a whole (few categories).  
- **Bar Chart** → Better for comparing absolute values across categories, especially when there are many items or when exact differences matter.  

---

### 3. How do you make visualizations more engaging?
- Use clear titles and labels.  
- Highlight key insights with colors or annotations.  
- Keep the design simple and avoid clutter.  
- Add interactivity (filters, slicers, tooltips).  
- Ensure accessibility with consistent color schemes.  

---

### 4. What is data storytelling?
- Combination of **data, visuals, and narrative** to communicate insights effectively.  
- Goes beyond what the data says, to explain **why it matters** and **what actions to take**.  

---

### 5. How do you avoid misleading visualizations?
- Start axes at zero (where appropriate).  
- Use consistent scales and avoid distortion.  
- Choose appropriate chart types.  
- Avoid overloading charts with too many variables.  
- Provide proper context (labels, units, legends).  

---

### 6. What are best practices in dashboard design?
- Keep dashboards simple and focused on KPIs.  
- Place the most important metrics at the top.  
- Group related visuals together.  
- Use filters and slicers for interactivity.  
- Maintain consistent colors and fonts.  
- Ensure dashboards answer specific business questions.  

---

### 7. What tools have you used for visualization?
- **Power BI** → Interactive dashboards and reports.  
- **Tableau** → Advanced visual storytelling.  
- **Matplotlib / Seaborn / Plotly (Python)** → Custom analytics charts.  
- **Excel** → Quick visual summaries.  
