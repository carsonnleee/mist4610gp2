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

**Dataset Source:**  
CMS State Drug Utilization Data (SDUD), accessed through Data.Medicaid.gov  
**Dataset Link:** https://data.medicaid.gov/dataset/61729e5a-7aa8-448c-8903-ba3e0cd0ea3c  

**Dataset Size:**  
- **Rows:** 5,205,065 observations  
- **Columns:** 15 variables  

**Description:**  
The CMS State Drug Utilization dataset contains detailed, product-level prescription drug information submitted quarterly by all U.S. state Medicaid programs. Each row represents a specific drug dispensed within a specific state and quarter, making the data highly granular and allowing for multi-dimensional analysis across **time**, **geography**, and **drug products**.

**Key Fields Include:**  
- **State:** U.S. state or territory where the claim occurred  
- **Product/Drug Name:** Commercial drug name recorded by Medicaid  
- **NDC (National Drug Code):** Unique product identifier (labeler + product + package code)  
- **Number of Prescriptions:** Total prescriptions dispensed  
- **Units Reimbursed:** Quantity of product reimbursed  
- **Medicaid Amount Reimbursed:** Total reimbursement paid by Medicaid  
- **Non-Medicaid Amount Reimbursed:** Additional reimbursement not covered by Medicaid  
- **Year + Quarter:** Time of dispensing (2022–2024 quarterly data)

**Why This Dataset Works Well for Our Questions:**  
The dataset’s combination of **high volume**, **multi-year coverage**, and **rich detail** enables meaningful analysis of both (1) high-level spending patterns and (2) drug-specific behaviors. Its inclusion of prescription counts, reimbursement amounts, and drug identifiers makes it especially well-suited for comparing cost drivers and examining whether spending is influenced more by high volume or high-cost specialty drugs.


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

Understanding which drug products account for the highest share of Medicaid spending is critically important from both an economic and social perspective. Medicaid is one of the largest publicly funded health programs in the United States, and its expenditures are supported by federal and state taxpayers. Identifying the drugs that drive the greatest financial burden allows policymakers and healthcare administrators to evaluate whether spending aligns with public health priorities and to consider opportunities for cost containment, rebate negotiation, or alternative therapies.

This question also carries social importance: many of the highest-spending drugs treat chronic, rare, or life-threatening diseases. Analyzing spending patterns can reveal unmet medical needs, patient dependency on certain therapies, and the implications for long-term disease management within low-income populations.  

This question is directly tied to our dataset because the Medicaid State Drug Utilization Data includes quarterly reimbursement amounts, prescription counts, NDC identifiers, and medicinal product names. These variables allow us to aggregate total spending per drug and identify which medications account for the greatest share of overall expenditures.


---


### Q2: *How does prescription volume relate to total Medicaid spending, and to what extent do high-cost specialty drugs drive overall expenditures?*


#### Why this matters:
This question moves beyond simple descriptive reporting and focuses on understanding *why* Medicaid spends what it does. Prescription count and total spending do not necessarily increase together: some medications cost thousands (or even millions) of dollars per prescription but are used infrequently, while others are inexpensive but heavily utilized. Analyzing this relationship helps determine whether Medicaid’s financial burden is driven primarily by high-cost specialty drugs or by high-volume medications that accumulate cost over time.

Economically, this insight informs resource allocation, budgeting, and policy decisions — such as whether states should prioritize formulary management, promote generics, or negotiate supplemental rebates. Socially and culturally, understanding these drivers reveals which conditions require the most treatment, which populations rely heavily on specific medications, and whether access to essential therapies is equitable and sustainable.

This question is tightly connected to our dataset because the Medicaid Drug Utilization Data contains both **Medicaid Amount Reimbursed** and **Number of Prescriptions** for each product. These variables enable calculations such as cost per prescription and help uncover whether overall spending results from drug price, drug utilization, or a combination of both. The dataset is uniquely structured to support this explanatory analysis.

---


## Visualizations & Findings

### Question One
<img width="775" height="363" alt="Screenshot 2025-11-19 at 1 03 21 PM" src="https://github.com/user-attachments/assets/9fd311d7-7d6a-48c4-9ca8-0d29d43156b6" />
<img width="1150" height="695" alt="Screenshot 2025-11-18 at 4 56 53 PM" src="https://github.com/user-attachments/assets/8ee239a1-23a9-4c6b-994a-6b5022f68a40" />
<img width="665" height="576" alt="Screenshot 2025-11-21 at 3 14 17 PM" src="https://github.com/user-attachments/assets/7dfe5dae-44c8-4e5d-bb57-6596e8f9c05a" />
<img width="463" height="354" alt="Screenshot 2025-11-21 at 3 17 50 PM" src="https://github.com/user-attachments/assets/a6a98304-7f93-43d6-9079-9dbeef1693d9" />



### **Which drug products had the highest total Medicaid spending in recent years?**

To understand which medications account for the greatest share of Medicaid drug spending, we analyzed prescription volume, reimbursement totals, and geographic spending patterns across multiple years. The following visualizations provide a comprehensive look at both utilization and cost trends across Medicaid programs nationwide.

---

### **1. Most Prescribed Drugs (2022–2024)**  
Our first visualization examined year-over-year prescription counts for the most commonly used medications covered by Medicaid.  
The results show that **Albuterol, Amoxicillin, Ibuprofen, Fluticasone, and Atorvastatin consistently remain among the most prescribed medications** during 2022, 2023, and 2024. These drugs treat common conditions—such as asthma, infections, allergies, pain management, and cholesterol control—which explains their high and stable utilization among Medicaid beneficiaries.

**Key takeaway:**  
Prescription volumes remain relatively stable over time, indicating continuous, essential demand for these medications.  
Despite their high utilization, these drugs do *not* dominate Medicaid spending, reinforcing an important insight: **high prescription volume does not necessarily translate to high total spending.**

---

### **2. Total Medicaid Reimbursed by Drug (2022–2024)**  
Next, we compared total Medicaid reimbursement amounts for these same medications to see how spending aligns with utilization.  
While all five drugs are heavily prescribed, **Fluticasone and Albuterol consistently account for the largest share of Medicaid spending** among this group. 

A notable trend is the **significant spike in Fluticasone reimbursement in 2024**, reaching over **$188 million**, making it the highest-cost drug among these common medications. Other drugs show steady spending patterns that mirror their stable prescription volumes.

**Key takeaway:**  
Even among commonly used drugs, spending varies—mainly due to therapeutic importance, dosage forms (inhalers vs. tablets), and patient need.  
However, even the highest-spending common medications fall far below the extremely high-cost specialty drugs that dominate Medicaid’s overall expenditures, which we analyze in later visualizations.

---

### **3. State-Level Medicaid Spending (Choropleth Map + Table)**  
To add geographic context, we analyzed total Medicaid drug reimbursement by state.  
**California stands out as the largest spending outlier**, with over **$41 billion** reimbursed—dramatically higher than any other state. States such as Florida, Georgia, and Arizona also show high spending totals, largely due to larger Medicaid populations.

Smaller states (e.g., Alaska, Delaware, D.C.) have substantially lower spending, which aligns with smaller beneficiary populations and program sizes.

**Key takeaway:**  
Geographic spending patterns closely track with **population size and Medicaid enrollment levels**, showing that state-level differences reflect scale rather than unusual trends in drug usage.

---

### Question 2 
<img width="570" height="374" alt="Screenshot 2025-11-20 at 2 48 33 PM" src="https://github.com/user-attachments/assets/4d6c691f-3dda-42e4-9f3d-8f59c2d109bc" />
<img width="657" height="308" alt="Screenshot 2025-11-20 at 2 49 36 PM" src="https://github.com/user-attachments/assets/bbee0730-328d-4ca6-af6f-48204daaedff" />

### **1. Relationship Between Prescription Volume and Medicaid Spending**

To explore how prescription volume relates to total Medicaid spending, we created a scatterplot comparing the **Number of Prescriptions** and the **Medicaid Amount Reimbursed** for each drug product. A trend line and R² value were added to measure the strength of the relationship.

**Key Findings:**

- **Very weak relationship:**  
  The regression line produced an **R² of approximately 0.035**, meaning prescription count explains only about **3.5%** of variation in Medicaid spending. This indicates that **drugs prescribed more often are not necessarily the drugs that cost Medicaid the most**.

- **Most drugs are low-cost, high-use generics:**  
  The scatterplot shows a dense cluster of points in the bottom-left corner, representing medications with both **low cost and high utilization**. These are typically generic drugs (e.g., antibiotics, inhalers, pain relievers) that do not significantly impact overall spending.

- **A few extremely expensive outliers dominate spending:**  
  Several drugs show **very high reimbursement amounts despite low prescription counts**, indicating that **high-cost specialty drugs**, rather than volume, are the primary drivers of Medicaid spending.

**Conclusion:**  
Medicaid drug spending is driven far more by the **price of specific specialty medications** than by prescription volume. This insight helps explain why cutting utilization of common generics does little to reduce overall spending, while managing specialty drug pricing could create a more meaningful impact.

---

### **2. Top 20 Most Expensive Drugs by Cost per Prescription**

To identify which medications place the greatest financial burden on Medicaid, we calculated a new metric:

**Cost per Prescription = SUM(Medicaid Amount Reimbursed) / SUM(Number of Prescriptions)**

We then ranked all drug products and visualized the **Top 20 Most Expensive Drugs** as a horizontal bar chart.

**Key Findings:**

- **Specialty drugs dominate the top of the list:**  
  Medications such as **Hemlibra, Humira(CF), Trikafta, Ravicti, Novoseven, and Tepezza** exceed **$5M–$12M per prescription**, making them some of the most expensive therapies covered by Medicaid.

- **These drugs treat rare and severe conditions:**  
  Most of the top 20 drugs are used to treat **hemophilia, cystic fibrosis, immune deficiencies, cancers, or endocrine disorders**. Their high cost reflects the nature of rare-disease treatments and biologic therapies.

- **Large cost disparities exist even among specialty drugs:**  
  While all 20 drugs are expensive, there is considerable variation across products, revealing pricing inconsistencies and challenges in managing specialty drug expenditures.

**Conclusion:**  
A small group of extremely high-cost medications accounts for a disproportionate share of Medicaid spending. This concentration suggests that targeted pricing policies, expanded biosimilar adoption, and value-based contracting could significantly reduce financial pressure on Medicaid without affecting access to common generic medications.

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
## Drug List Definitions

## Drug Descriptions

**ALBUTEROL**  
A fast-acting inhaler used to open airways during asthma attacks or breathing issues.

**AMOXICILLI (Amoxicillin)**  
A common antibiotic used to treat bacterial infections like strep throat, ear infections, and sinus infections.

**ATORVASTAT (Atorvastatin)**  
A cholesterol-lowering medication that reduces the risk of heart attack and stroke.

**FLUTICASONE**  
A steroid used in inhalers and nasal sprays to treat asthma and allergies.

**IBUPROFEN**  
An over-the-counter anti-inflammatory drug used to treat pain, fever, and swelling.

**CABOMETYX**  
A targeted cancer therapy used to treat kidney cancer, liver cancer, and thyroid cancer.

**COSENTYX**  
A biologic used to treat psoriasis, psoriatic arthritis, and ankylosing spondylitis.

**CRYSVITA**  
A treatment for X-linked hypophosphatemia, a rare genetic bone disorder.

**GAMMAGARD**  
An immune globulin therapy used for people with immune deficiencies and autoimmune diseases.

**HEMLIBRA**  
A preventive treatment for hemophilia A that reduces bleeding episodes.

**HEMLIBRA-**  
Another dosing form of Hemlibra, used to prevent bleeding in hemophilia A patients.

**HUMIRA PEN**  
A biologic that treats autoimmune diseases such as rheumatoid arthritis, Crohn’s disease, and psoriasis.

**HUMIRA(CF)**  
The citrate-free version of Humira used for autoimmune inflammatory conditions.

**INVEGA TRI (Invega Trinza)**  
A long-acting injectable antipsychotic for schizophrenia.

**JAKAFI**  
A medication that treats bone marrow disorders like myelofibrosis and polycythemia vera.

**LUPRON DEP**  
A hormone-suppressing therapy used for prostate cancer, endometriosis, and fibroids.

**NOVOSEVEN**  
A clotting factor used to control bleeding episodes in patients with hemophilia.

**RAVICTI**  
A medication that treats urea cycle disorders by removing toxic ammonia from the blood.

**REVLIMID**  
An oral cancer drug used to treat multiple myeloma and certain blood cancers.

**SPRYCEL**  
A targeted leukemia medication used to treat chronic myeloid leukemia (CML).

**STELARA**  
A biologic for Crohn’s disease, ulcerative colitis, psoriasis, and psoriatic arthritis.

**TEPEZZA**  
A treatment for thyroid eye disease that reduces swelling behind the eyes.

**TRIKAFTA**  
A triple-therapy drug for cystic fibrosis that improves lung function.

**TRIKAFTA (**  
Another formulation or naming variant of Trikafta for cystic fibrosis.

**VERZENIO**  
A targeted breast cancer medication used with hormone therapy.



