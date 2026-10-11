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

---

## Key Business & Epidemiological Questions Answered

### 1. Revenue Sources (Procedures, Departments, Diagnoses)

* **By Diagnostic Procedure:**
  * **X-Ray:** £1,053,529 (31.4% of procedure billing | 1,537 visits)
  * **CT Scan:** £805,508 (24.0% | 1,233 visits)
  * **MRI Scan:** £600,739 (17.9% | 912 visits)
  * **Ultrasound:** £481,347 (14.3% | 720 visits)
  * **Blood Test:** £414,952 (12.4% | 598 visits)

* **By Clinical Department:**
  * **Cardiology:** £846,925 (25.2% of total revenue | 1,281 visits)
  * **Orthopedics:** £813,253 (24.2% | 1,179 visits)
  * **General Surgery:** £783,247 (23.3% | 1,185 visits)
  * **Neurology:** £478,200 (14.2% | 697 visits)
  * **Pediatrics:** £434,450 (12.9% | 658 visits)

* **By Clinical Diagnosis:**
  * **Hypertension:** £1,328,213 (39.6% | 2,013 visits) — primary driver of revenue and clinical patient volume.
  * **Appendicitis:** £661,518 (19.7% | 994 visits)
  * **Asthma:** £629,505 (18.8% | 918 visits)
  * **Fracture:** £411,420 (12.3% | 606 visits)
  * **Migraine:** £325,419 (9.7% | 469 visits)

---

### 2. Operational Cost Drivers & Financial Protection Dynamics

| Component | Total Billed (£) | % of Total | Average per Visit (£) | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Treatment Cost** | £2,630,406 | 78.4% | £526.08 | Direct clinical, surgical, and procedural charges |
| **Medication Cost** | £546,039 | 16.3% | £109.21 | Inpatient and outpatient pharmacotherapy regimens |
| **Room Charges** | £179,630 | 5.4% | £35.93 | Inpatient accommodations (mean LOS: 4.87 days)|

#### Financial Protection & Patient Liabilities
* **Third-Party Insurance Coverage:** £2,225,924 (66.3% aggregate reimbursement | £445.18 mean coverage/visit).
* **Patient Out-of-Pocket (OOP) Burden:** £1,059,267 (31.6% net direct patient responsibility | £211.85 mean cost/visit)
* **Key Finding:** Unreimbursed out-of-pocket costs represent nearly one-third of overall healthcare expenditure, indicating high vulnerability to catastrophic health spending among uninsured/underinsured groups.

---

### 3. Provider Quality-to-Cost Performance

Encounters were evenly distributed across attending clinicians (~1,000 visits and ~£670,000 billing per clinician):

* **Dr. Olu Abisola:** Highest overall patient satisfaction (**5.58 / 10** across 1,012 visits), generating £675,815 (£667.80 mean billing per encounter).
* **Dr. Johnson Grek:** Second-highest patient satisfaction (**5.19 / 10** across 997 visits) while maintaining the most cost-efficient treatment profile (£667.61/encounter).
* **Dr. Sade Kikiola:** Lowest patient satisfaction rating (**2.92 / 10** across 988 visits), highlighting a priority target for clinical quality improvement interventions.

---

### 4. Service Volume Trajectories & Temporal Trends

* **Care Setting Breakdown:**
  * **Outpatient:** 50.4% (2,520 visits)
  * **Inpatient:** 24.9% (1,245 admissions)
  * **Emergency:** 24.7% (1,235 encounters)

* **Seasonal Trajectory:**
  * Outpatient service demand exhibits strong seasonality, peaking in **March through June** (surpassing 90+ visits/month).
  * Volume drops significantly during the mid-year period (July–August) before undergoing a steady autumn recovery.


 ### Key insights (examples from analysis)
- Procedures like X-Ray and CT contribute a large share of billing (top 2–3 procedures). 
- Medication contributes significantly to per-visit cost — useful target for cost-management. 
- Provider-level variation: some high-revenue providers also have high ratings

### Dashboard
`<img width="584" height="323" alt="Screenshot 2026-10-09 085101" src="https://github.com/user-attachments/assets/6477a5bc-d7ff-4116-a86e-b78dc4f50489" />
<img width="581" height="323" alt="Screenshot 2026-10-09 085026" src="https://github.com/user-attachments/assets/9408d79c-4230-4d14-9403-404077593153" />

### Conclusion
This Power BI project demonstrates how data visualization can uncover meaningful insights in healthcare management. By analyzing financial records and provider performance, the dashboard provides a clear view of the clinic’s operational health — from revenue streams and treatment costs to provider efficiency and patient trends.

The findings show that while the healthcare center maintains steady financial growth, medication and treatment costs represent a significant portion of total expenditure. This insight highlights the need for cost control and resource optimization without compromising care quality.

Additionally, provider-level analysis revealed distinct patterns in revenue generation and ratings. These differences suggest that recognizing and learning from top-performing providers can help the organization improve both financial outcomes and service delivery.

By turning raw data into interactive visuals, this project illustrates the impact of data-driven storytelling — where complex healthcare data becomes a tool for informed decisions, improved patient outcomes, and long-term sustainability.
  
