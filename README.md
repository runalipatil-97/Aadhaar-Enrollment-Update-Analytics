📖 Project Overview

This project was developed as part of UIDAI Data Hackathon 2026 to analyze Aadhaar enrollment, biometric update, and demographic update transaction patterns across India. The objective is to understand whether the Aadhaar ecosystem is enrollment-driven or maintenance-driven, identify regional deviations, and provide data-backed recommendations to improve operational efficiency, accessibility, and infrastructure planning.

National-level analysis indicates that Aadhaar has reached a mature coverage stage, with biometric updates accounting for over 70% of transactions and new enrollments contributing less than 3%. However, deeper district- and state-level analysis reveals localized anomalies that require targeted interventions.

🎯 Objectives

Identify operational patterns in enrollments and updates

Highlight regional deviations from national trends

Analyze age-group-wise transaction behavior

Assess infrastructure alignment with usage patterns

Provide actionable recommendations for optimization

📊 Datasets Used

Three Aadhaar-related datasets compiled from multiple CSV files:

Dataset	Description
Enrollment Dataset	Aadhaar enrollment counts by age group (0–5, 5–17, 18+)
Biometric Updates Dataset	Biometric update counts by age group (5–17, 18+)
Demographic Updates Dataset	Demographic update counts by age group (5–17, 18+)

Common Fields

State

District

Date (Month)

Pincode

Data Source:
Government open data portals (e.g., data.gov.in).
Due to size constraints, raw datasets are not included. Cleaned datasets are available in data/processed/.

🛠 Tools & Technologies

Python (Pandas, NumPy)

Jupyter Notebook / Google Colab

Power BI

Power Query

DAX

Microsoft Excel

🔁 Methodology
1. Data Preparation (Python – Jupyter Notebook / Google Colab)

Imported multiple CSV files for each dataset

Merged files into unified enrollment, biometric, and demographic datasets

Standardized state names and resolved spelling inconsistencies

Handled missing values and corrected data types

Performed preliminary aggregations and validation checks

2. Power Query Transformations (Power BI)

Trimmed whitespace from district names

Cleaned text and corrected spelling variations

Converted district names to uppercase

Replaced inconsistent district labels with standardized values

Converted columns to appropriate data types

~50% of district records required transformation to ensure reliable analysis.

3. Data Modeling

Star schema design:

Fact Tables

Fact_Enrollment

Fact_Biometric

Fact_Demographic

Dimension Tables

Dim_Date

Dim_State

Dim_District

Relationships were created using state, district, and date keys.

4. DAX Measures

Biometric Share (%)

Age Group Ratios

Deviation from National Average

Monthly Trend Measures

These measures power interactive visuals and dynamic filtering.

📈 Key Insights
Enrollment

Pan-India enrollments are low relative to updates, confirming maturity stage

Meghalaya shows higher adult (18+) enrollments

East Khasi Hills district dominates enrollment activity

District-level patterns are more meaningful than state-level averages

Biometric Updates

Dominated by high-population states (Uttar Pradesh, Maharashtra, Madhya Pradesh)

Balanced across age groups nationally

Certain states show above-average update frequency

Noticeable dip in October (likely festive season impact)

Demographic Updates

Concentrated in high-population states

Reflect population-scale effects rather than anomalies

Similar monthly dip patterns as biometric updates

Online and physical update channels both contribute

✅ Recommendations
Pan-India

Shift focus from enrollment expansion to maintenance optimization

Seasonal capacity planning around festive months

Use deviation metrics as early warning indicators

Enrollment

District-level monitoring

Strengthen early-age (0–5) enrollment awareness

Deploy mobile enrollment units

Biometric Updates

Expand infrastructure in high-update states

Bundle multiple updates in one visit

Standardize biometric refresh cycles

Demographic Updates

Prioritize capacity in large states

Improve validation at enrollment stage

Promote online update channels

🎯 Expected Impact

Optimized resource allocation

Reduced operational strain

Improved citizen experience

Transition toward data-driven Aadhaar governance
