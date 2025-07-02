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

   (This assigns 10 minutes of downtime per 'Unhealthy' report.)

3. Created two bar charts:
   - **Down Time per Factory**
   - **Down Time per Device Type**

4. Built a dashboard combining the two charts.
5. Enabled filter action on the first chart to dynamically update the second based on selected factory.
6. Identified the factory with the maximum cumulative downtime and the machines most frequently reporting failure.

### Outcome:
- The factory with the most downtime was identified.
- Machine types contributing most to the downtime were revealed.
- A screenshot of the dashboard was submitted as proof of completion.

---

## Task 2: Forensic Technology – Gender Pay Equity Analysis in Excel

### Objective:
To assist in classifying gender pay equity across roles and locations based on Deloitte's forensic audit algorithm.

### Context:
Daikibo received internal complaints about gender inequality in salaries. The forensic team generated an equality score (from -100 to +100) for each job role at each factory:
- 0 indicates perfect equality.
- Negative or positive extremes indicate bias in either direction.

### Tools Used:
- Microsoft Excel

### Dataset:
- Columns:
  - Factory
  - Job Role
  - Equality Score (integer)

### Task:
Create a fourth column named `Equality Class` and classify equality scores as:
- **Fair**: if score is between -10 and +10 (inclusive)
- **Unfair**: if score is between -20 and -11 OR 11 and 20
- **Highly Discriminative**: if score < -20 or > 20

### Implementation:
Used a nested IF formula in Excel:

       =IF(ABS([@Equality_Score]) <= 10, "Fair",
           IF(ABS([@Equality_Score]) <= 20, "Unfair", "Highly Discriminative"))

### Outcome:
- Each row in the dataset was classified correctly.
- The completed Excel sheet was submitted successfully.

---

## Skills Gained:
- Tableau dashboarding and visualization
- Data modeling using calculated fields
- Filtering and interactivity in business dashboards
- Excel logic and classification using nested formulas
- Real-world data interpretation in business and forensic contexts
- Analytical storytelling with data

---

## Author:
Raja Mehdi Ali Khan  
NIT Andhra Pradesh  
Deloitte Data Analytics Virtual Internship (2025)
