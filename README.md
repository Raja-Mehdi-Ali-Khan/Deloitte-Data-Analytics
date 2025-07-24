# Deloitte Data Analytics Virtual Internship – Daikibo Industrials

This repository contains submissions for the Deloitte Australia Data Analytics Virtual Internship hosted on Forage. The internship simulated real-world business problems faced by Daikibo Industrials — a multinational manufacturing company — focusing on two major analytics domains:

1. Machine Telemetry Data Analysis (Task 1)
2. Gender Pay Equity Investigation (Task 2)

---

## Task 1: Telemetry Data Analysis with Tableau

### Objective:
To determine:
- Which Daikibo factory experienced the highest machine downtime.
- Which machine types contributed most to the downtime in that factory.

### Context: 
Daikibo operates four factories in:
- Meiyo (Tokyo, Japan)
- Seiko (Osaka, Japan)
- Berlin (Germany)
- Shenzhen (China)

Each factory has 9 machine types, reporting status every 10 minutes. All telemetry data for May 2021 was unified into a single JSON file by the client’s tech team.

### Tools Used:
- Tableau (free trial version)
- JSON-formatted telemetry data

### Approach:
1. Imported the unified JSON dataset into Tableau.
2. Created a calculated field named `Unhealthy` using the formula:

       IF [status] = 'Unhealthy' THEN 10 ELSE 0

(Assigning 10 minutes of potential downtime per 'Unhealthy' record.)

### 📊 Developed the Following Visualizations:

- **Down Time per Factory** (bar chart)
- **Down Time per Device Type** (bar chart)

### 🧩 Built an Interactive Dashboard Combining Both Charts:

- Enabled **filter action** on the first chart to dynamically update the second based on the selected factory.

### 📈 Created Additional Insights:

- **Unhealthy Events Over Time** (line chart)
- **Heatmap of Device Type vs Factory**
- **Failure Rate by Device Type**
- **Factory Performance Summary Table**

---

### ✅ Outcome

- Identified the factory with the **highest total downtime**.
- Determined which **machine types** were most responsible for downtime in that factory.
- Submitted a **screenshot of the Tableau dashboard** as required.

---

## 🕵️‍♂️ Task 2: Forensic Technology – Gender Pay Equity Analysis in Excel

### 🎯 Objective
Assist Daikibo’s forensic team by classifying the level of **gender pay equality** across job roles and factories using **Equality Scores**.

### 🏢 Context
Internal concerns about salary-based gender discrimination led to a forensic audit. The forensic analysts calculated an **Equality Score** (ranging from -100 to +100) for each job role at each factory:

- `0` indicates perfect equality.  
- Negative or positive values imply bias.

### 🛠️ Tools Used
- Microsoft Excel

### 🧠 Dataset Overview

**Columns:**
- `Factory`
- `Job Role`
- `Equality Score`

### 📋 Task

Add a 4th column named `Equality Class`, classifying the score as:

| Score Range             | Equality Class           |
|-------------------------|--------------------------|
| -10 to 10 (inclusive)   | Fair                     |
| -20 to -11 or 11 to 20  | Unfair                   |
| < -20 or > 20           | Highly Discriminative    |

### 💡 Implementation

Used a nested `IF` formula in Excel:

```excel
=IF(ABS([@Equality_Score]) <= 10, "Fair",
    IF(ABS([@Equality_Score]) <= 20, "Unfair", "Highly Discriminative"))
```
### ✅ Outcome

- Accurately classified all roles based on **Equality Score**.  
- Submitted the completed Excel file as the final output.

---

### 🧠 Skills Gained

- 📈 Data Visualization using Tableau  
- ⚙️ Data modeling with calculated fields  
- 🧩 Interactive dashboards with filters  
- 📊 Data classification using Excel formulas  
- 🕵️ Real-world business and forensic analytics  
- 📚 Analytical storytelling and insight reporting  

---

### 👤 Author

**Raja Mehdi Ali Khan**  
*National Institute of Technology, Andhra Pradesh*  
Completed as part of the **Deloitte Data Analytics Virtual Internship (2025)**
