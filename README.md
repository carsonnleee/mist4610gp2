# mist4610gp2
# Medicaid: Program Overview and State Drug Utilization Trends  
**MIST 4610 - GROUP PROJECT 2**  
### Group Name: 15058_Group5
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

To answer our research questions, we applied the following data manipulations:

- Combined the quarterly 2022, 2023, and 2024 State Drug Utilization tables  
- Cleaned and formatted fields to ensure consistency  
- Created a **calculated field** to measure **Cost per Prescription** using: Analysis - create new calculation
- This metric was crucial in identifying **high-cost outlier drugs** with large spending impact despite low prescription volume.



---
## Project Questions

### Q1: *Which drug products contributed the most to total Medicaid spending from 2022–2024, and how was this spending distributed across states?*

#### Why this matters:
- **High-volume drugs** reveal widespread public health needs  
- Helps uncover whether heavy utilization aligns with heavy spending  
- Identifies core medications relied upon across populations  

---


### Q2: *How does prescription volume relate to total Medicaid spending, and to what extent do high-cost specialty drugs drive overall expenditures?*


#### Why this matters:
- Spending drivers shape Medicaid budgeting and policy  
- Reveals whether cost is driven by **utilization** or **price intensity**  
- Identifies the drugs putting the greatest financial strain on Medicaid  

---


## Visualizations & Findings

### Visualization 1 – Top-Spending Drugs  
<img width="775" height="363" alt="Screenshot 2025-11-19 at 1 03 21 PM" src="https://github.com/user-attachments/assets/9fd311d7-7d6a-48c4-9ca8-0d29d43156b6" />
<img width="1150" height="695" alt="Screenshot 2025-11-18 at 4 56 53 PM" src="https://github.com/user-attachments/assets/8ee239a1-23a9-4c6b-994a-6b5022f68a40" />
<img width="1095" height="719" alt="Screenshot 2025-11-18 at 8 09 42 PM" src="https://github.com/user-attachments/assets/8b70671a-582e-4893-97d4-4cd1e6ef1def" />
<img width="180" height="171" alt="Screenshot 2025-11-19 at 1 04 07 PM" src="https://github.com/user-attachments/assets/b9c93cfe-c742-44f8-86af-68bf1cf9ed81" />

- Fluticasone and Albuterol consistently drive some of the highest Medicaid spending, reflecting the widespread need for chronic respiratory care (asthma, allergies) across the population. Their continued dominance in spending highlights sustained public health demand and the importance of access to essential respiratory medications.

- Fluticasone shows a sharp increase in spending in 2024, suggesting changes in prescribing behavior, pricing adjustments, or shifting population health needs related to cholesterol management. This rise indicates an emerging trend that may warrant deeper examination in future analyses.

- State-level variation in Medicaid drug spending reveals significant geographic disparities. Large states such as California account for a disproportionate share of total reimbursement, emphasizing how population size, Medicaid enrollment, and regional health patterns shape financial pressures within the program.

### Visualization 2 – Trend by State  
[Insert Tableau Screenshot or Link]  
- There is a **very weak correlation** between the number of prescriptions and total Medicaid spending (R² ≈ 0.035). This means **high prescription volume does not equal high cost**—most frequently used drugs are **low-cost generics**.  
- Several drugs appear as **spending outliers**, indicating that price—not volume—is the key driver of Medicaid expenditures.
- A small number of **specialty drugs** (e.g., Humira, Trikafta, Stelara, Skyrizi) have **extremely high cost per prescription**, often exceeding millions.  
- These drugs **drive a disproportionate share of total Medicaid reimbursement**, despite relatively low utilization.  
- This confirms that **Medicaid spending is driven by price intensity**, not prescription count.
---

## Implications & Takeaways

### Why this matters:
- Medicaid supports essential healthcare, especially for vulnerable populations  
- Drug utilization is a reflection of public health—not optional spending  
- Spending insights help states and federal agencies manage cost and access  
- Data like this helps reduce stigma, inform policy, and guide better decisions  

---

## Final Thoughts
- This project connects public policy, health economics, and data analytics. By analyzing Medicaid drug spending, we gain a clearer understanding of the drivers behind one of the U.S.’s largest healthcare programs. 
- High-volume drugs are not the primary drivers of Medicaid spending. Even the most frequently prescribed medications contribute only a small share to total reimbursement, indicating that broad utilization does not equate to high cost
- Medicaid spending is disproportionately driven by a small group of high-cost specialty drugs. These medications have extremely high cost per prescription often millions, creating a far greater budget impact than widely used generics, despite their lower prescription volume
- Together, the analyses show that Medicaid expenditures are shaped far more by the cost intensity of specific specialty drugs than by sheer prescription volume. Understanding this imbalance is essential for evaluating budget pressures and guiding policy decisions around drug pricing and access


---

