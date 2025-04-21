# Hospital Patients Record Analysis

![Hospital Dashboard Cover](https://github.com/user-attachments/assets/047f5e6c-6fcf-4590-801b-a0c4792be128)

---

## Aim

The aim of this analysis is to assess hospital performance metrics—particularly** **encounter costs**, **procedure duration**, **readmissions**, and **insurance influence** to identify trends and provide actionable recommendations that support strategic decision-making, cost containment, and improved patient care outcomes.

📌 Key recommendations include cost control, readmission management, and procedural efficiency.

---

## Data Preparation & Modeling

### Data Connection and Transformation

Using Power BI Desktop, I imported and cleaned datasets related to encounters, patients, procedures, payers (insurance), and organizations. Key transformations included:

- Standardized data types (e.g., admission/discharge dates, cost fields like `payer_coverage`, `total_claim_cost`)
- Removed null and duplicate records, especially in patient and procedure entries
- Created new calculated columns using Power Query and DAX
- Extracted Month, Year, Quarter from encounter start dates for time-based analysis
- Ensured consistent formatting for fields like Gender, Encounter Class, and Procedure Reason

### Relational Data Model

The data model follows a **star schema** structure, with a central **Encounter Fact Table** and linked dimension tables:

- `patients`: Demographics including gender, birth date, and age group  
- `procedures`: Procedure details, encounter IDs, and reason codes  
- `payer`: Insurance provider data  
- `organization`: Healthcare facility information  
- `date`: Custom date table to support accurate time-based filtering  

![Data Model](https://github.com/user-attachments/assets/d6a80f37-d0cd-46bd-acf1-0698f464a0b2)

---

## Visualizations

### Encounter Cost Analysis

- Average Encounter Cost increased **12.74%** from 2011 to 2022  
- Notable rise began in 2020, with a **4.42% ($5.0)** increase in 2 years  
- Sharpest annual spike occurred between 2011 and 2012: from **$105.8 → $112.5**

#### Payer Insights

- **Medicare** had the highest total encounter cost: **$1.32M**  
- This was **1,522.55%** higher than **Anthem** ($81K)  
- **Ambulatory encounters** had the highest cost and utilization  
- **Wellness** and **Urgent Care** were lower-cost but had significant volume  

![Encounter Cost Chart](https://github.com/user-attachments/assets/77f7e6b6-78ce-4848-b5ac-e42af5f3a2c5)

---

### Procedure Utilization and Duration

- Total procedure volume: **11,000 cases**  
- Average procedure duration: **7.25 hours**

#### 🧾 High-Cost Procedures

- **Electrical Cardioversion**: Most expensive and frequent ($35.8M / 1,383 cases)  
- Others: Fetal heart auscultation, chemotherapy, catheter ablation  

---

### Admissions and Readmissions Trends

#### Admissions Over Time

- Decreased **26.91%** from Jan 2011 to Jan 2022  
- Most significant drop: **Oct 2014–2020** (−189 admissions / −26.73%)  
- Earlier spike: **301 → 640 admissions** from Jan 2011 to Jul 2014  

#### Readmission Insights

- **"Encounter for problem (procedure)"**: Top reason for readmissions  
  - **4,239 cases** (30.45% of total)  
  - **155.36%** higher than the lowest (1,660 for "Encounter for symptom")

![Readmission Trends](https://github.com/user-attachments/assets/b9734d2a-3d10-478e-b9ed-83a4d639ba5e)

---

## Recommendations

1. **Address Rising Encounter Costs**  
   Review post-2020 clinical and admin workflows to identify cost drivers.

2. **Implement Chronic Care Management**  
   Frequent patients may have chronic conditions—introduce personalized care plans.

3. **Evaluate High-Cost Procedures**  
   Procedures like **electrical cardioversion** require scrutiny; explore preventive alternatives and education.

4. **Reduce Readmissions**  
   Focus on "Encounter for problem (procedure)" via better discharge planning and chronic disease management.

5. **Analyze Procedure Duration Spikes**  
   Investigate spikes from 2014 and 2017 for clinical/operational issues; improve real-time anomaly detection.

---

🛠 Built with **Power BI**, **Power Query**, **DAX**, and advanced **Data Modeling** techniques.
