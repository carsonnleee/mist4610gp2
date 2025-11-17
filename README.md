# mist4610gp2
# Medicaid: Program Overview and State Drug Utilization Trends  
**MIST 4610 - Data Management & Analytics**  
November 21  
Group Members: Hana Darley, Carson Sams, Mahith Madasu
- Carson Sams – [@carsonnleee](https://github.com/carsonnleee)  
- Hana Darley – [@hanaldarley](https://github.com/hanaldarley)  
- Mahith Madasu – [@mahithm1](https://github.com/mahithm1)

---

## Background & Context

### What is Medicaid?  
Medicaid is a joint federal–state health-insurance program designed to provide coverage to low-income individuals and families. While governed by federal law, it is administered by states, leading to variations in eligibility, services, and spending.

Key populations covered include:  
- Low-income adults and children  
- Pregnant women  
- Seniors needing long-term care  
- People with disabilities  

### How Medicaid Works  
- **Funding** is split between the federal government and states (FMAP model)  
- States must cover mandatory services and may offer optional ones (like prescription drugs)  
- Each state sets payment rates, eligibility processes, and utilization rules  

This structure creates wide variation in **costs and utilization across states**.

### Historical Background  
- Established under Title XIX of the Social Security Act in 1965  
- Expanded in the 1980s–90s to cover more children, women, and disabled individuals  
- Continues to evolve with long-term-care reforms and managed-care initiatives  

### Medicaid vs. Medicare  
| Medicaid | Medicare |
|----------|----------|
| Income-based | Age-based (65+) |
| All ages | Primarily older adults |
| Varies by state | Federal program |

### Modern Role in Healthcare  
- One of the largest coverage programs in the U.S.  
- Funds a large share of births, pediatric services, and chronic disease care  
- Prescription drug coverage is a major cost driver  
- Policy shifts significantly affect state budgets and patient access  

---

## Why Medicaid Drug Data Matters  
The **State Drug Utilization dataset** captures prescription-level data for Medicaid reimbursements across states and quarters.

This data enables:
- Cost and utilization trend analysis  
- State-to-state comparisons  
- Public health and policy insights  
- Identification of high-cost drugs and categories

---

## Dataset Overview

**Source:** CMS State Drug Utilization Data (data.medicaid.gov)  
**Rows:** 5,205,065  
**Columns:** 15  
**Key Fields Include:**
- State  
- Drug Name  
- NDC (Labeler + Product Code)  
- Total Reimbursement  
- Medicaid & Non-Medicaid Amounts  
- Units Reimbursed  
- Number of Prescriptions  
- Year + Quarter  

---
## Data Preparation

To answer these questions, we performed the following data manipulations:
- Combined data across all four quarters for 2022, 2023, and 2024  
- Grouped and aggregated total reimbursement by NDC and state  
- Created calculated fields for spending trends and growth rates  
- Filtered for top N drugs per state and by total national spend  


---
## Project Questions

### Q1: *Which drug products had the highest total Medicaid spending from 2022 to 2024?*

#### Why this matters:
- **Economic Impact:** High-cost drugs strain budgets  
- **Public Health:** Indicates treatment trends for major conditions  
- **Data Fit:** Dataset reports reimbursement totals per drug per quarter  

---

### Q2: *How has Medicaid spending trended from 2022 to 2024, and which drug products show the strongest upward or downward trends per state?*

#### Why this matters:
- **Spending Trends:** Highlights growth areas or successful cost control  
- **State Variation:** Shows how utilization differs geographically  
- **Data Fit:** Year, state, NDC, and reimbursement fields support trend analysis  

---


## Visualizations & Findings

### Visualization 1 – Top-Spending Drugs  
[Insert Tableau Screenshot or Link]  
- Drug X had the highest spending nationally in 2024  
- Chronic condition drugs dominate the top 10 list  
- Spending is concentrated in a small number of high-cost products  

### Visualization 2 – Trend by State  
[Insert Tableau Screenshot or Link]  
- Drug Y showed sharp increases in multiple states  
- Some drugs declined in usage due to generic availability or policy  
- Notable state-level differences in prescribing patterns  

---

## Implications & Takeaways

### Why this matters:
- Medicaid supports essential healthcare, especially for vulnerable populations  
- Drug utilization is a reflection of public health—not optional spending  
- Spending insights help states and federal agencies manage cost and access  
- Data like this helps reduce stigma, inform policy, and guide better decisions  

---

## Final Thoughts
This project connects public policy, health economics, and data analytics. By analyzing Medicaid drug spending, we gain a clearer understanding of the drivers behind one of the U.S.’s largest healthcare programs.

---

