# Healthcare-Performance-Dashboard

### Project Overview
Is this healthcare centre financially healthy?

What drives revenue and cost at this clinic — procedures, providers, or patient mix?

This project analyzes the financial health of a healthcare center — exploring revenue sources, cost drivers, and provider efficiency. Using Power Query, DAX, and interactive Power BI visuals, it presents clear insights on billing trends, medication and treatment costs, and provider ratings. Designed to help health administrators and analysts make data-driven decisions that improve care delivery and operational performance.

### Goal
The goal of this project is to analyze the financial health and provider performance of a healthcare centre using Power BI. The dashboard helps stakeholders answer:
- Where is the revenue coming from (procedure, department, diagnosis)?
- What are the largest cost drivers (medication, treatment, room charges)?
- Which providers deliver the best outcomes vs cost?
- How do visits and revenue trend over time (monthly/quarterly/yearly)?

## What I did
1. Data cleaning & shaping (Power Query)   
   - Created calendar fields: `Weekday`, `IsWeekend`, `Quarter`, `Month`, `Year`.  
   - Split/normalized tables: Visits, Providers, Departments, Procedures, Diagnoses, Billing components (Insurance, Out-of-Pocket).  
2. Data model  
   - Star schema: central `Visits` table + dimension tables for `Provider`, `Procedure`, `Department`, `Diagnosis`, `Calendar`.  
3. Measures (DAX) — KPI, growth and ratio measures for financial and operational insights.  
4. Dashboard design (Power BI)
   - Page 1 — Financial Overview: KPI cards, trend charts (monthly revenue), revenue by procedure/department, map of patient locations, cost breakdown.  
   - Page 2 — Provider Insights: provider ranking by revenue, avg rating, visits, avg treatment cost, length-of-stay distribution and provider detail drillthrough.  

 ### Key insights (examples from analysis)
- Procedures like X-Ray and CT contribute a large share of billing (top 2–3 procedures). 
- Medication contributes significantly to per-visit cost — useful target for cost-management. 
- Provider-level variation: some high-revenue providers also have high ratings

### Dashboard
[Healthcare Dashboard.pdf](https://github.com/user-attachments/files/22762279/Healthcare.Dashboard.pdf)

### Conclusion
This Power BI project demonstrates how data visualization can uncover meaningful insights in healthcare management. By analyzing financial records and provider performance, the dashboard provides a clear view of the clinic’s operational health — from revenue streams and treatment costs to provider efficiency and patient trends.

The findings show that while the healthcare center maintains steady financial growth, medication and treatment costs represent a significant portion of total expenditure. This insight highlights the need for cost control and resource optimization without compromising care quality.

Additionally, provider-level analysis revealed distinct patterns in revenue generation and ratings. These differences suggest that recognizing and learning from top-performing providers can help the organization improve both financial outcomes and service delivery.

By turning raw data into interactive visuals, this project illustrates the impact of data-driven storytelling — where complex healthcare data becomes a tool for informed decisions, improved patient outcomes, and long-term sustainability.
  
