📌 Project Objective

This project analyzes customer behavior, event performance, A/B testing results, and RFM‑based customer value using a four‑page interactive Power BI report and a dedicated dashboard published on Power BI Service.
It answers key questions such as why traffic increases without a matching rise in revenue, what drives high‑value customers into the At‑Risk segment, and which channels and payment methods influence their purchasing decisions.


📌 Tools & Skills Used

•	Power BI Desktop

•	Power BI Service

•	DAX (Measures & Time Intelligence)

•	Data Modeling (Star Schema)

•	RFM Segmentation

•	Marketing Analytics

•	Data Cleaning & Transformation

•	Dashboard Design & UX Principles


📌 Business Questions Answered

This report was designed to address practical business questions, including:

- Why does traffic increase during events without a proportional rise in revenue?
  
- Do A/B test variations actually improve customer spending behavior?
  
- Which RFM segments contribute the most to long‑term value?
  
- Why are high‑value customers becoming At‑Risk, and when does this shift occur?
  
- Which payment methods and marketing channels matter most for retaining valuable customers?
  

📌 Dataset Overview

The dataset (sourced from Kaggle) includes four tables covering marketing activity, customer demographics, branch attributes, and sales transactions.
It provides a complete view of customer behavior, event performance, and marketing effectiveness.


📌 Data Cleaning Summary

Basic data cleaning steps were applied across all tables to ensure accuracy and consistency before modeling.
Key fixes included:

•	Ad History Table: 

Filled missing EndDate values using a consistent yearly pattern (Jan 1 → Dec 31).

•	Customer Table:

- Removed ~2% missing gender values.

- Corrected extreme age outliers (–10, 150) using mean replacement.

- Converted negative TotalSpent values to positive.

- Replaced inconsistent TotalTransactions values (zeros with non‑zero spending).

- Fixed ~300 invalid country/city entries using BranchName.

•	Transactions Table: 

Removed less than 5% negative sales amounts.

•	Branches Table:

No major issues detected.
All transformations and calculated fields are available inside the PBIX file.


📌 Data Model

A clean star‑schema model was built to ensure fast performance and intuitive navigation.


Model Structure :

•	BranchID links customer data, transactions, ad strategy history, and branch attributes.

•	A Date Table supports seasonal and time intelligence analysis (Quarter, Month, Year).

•	A Measure Table stores all DAX calculations for maintainability and clarity.

This structure enables seamless analysis across events, customer behavior, and marketing performance.


📌 Report Structure (4 Pages)

1) Events & A/B Testing
Analyzes how promotional events and A/B test groups affect traffic and revenue.
Event traffic increased 3×, but revenue rose only slightly, indicating conversion issues.
A/B test groups were imbalanced, and average revenue showed no uplift from variations.

2) Customer Value (RFM Segmentation)
RFM segmentation was built from scratch to classify customers into VIP, Regular, At‑Risk, and Need Development.
Despite "At Risk" representing only 16% of customers, the At‑Risk segment generated significantly more revenue than the largest segment (Need Development 53%).
They behave like VIPs in spending and frequency but have much worse recency, indicating high churn risk.

3) At‑Risk Customer Analysis
Age is the only demographic factor that differentiates At‑Risk customers, with Retirees and Gen X forming nearly half of the segment.
Their spending peaks in May (Q2) and August (Q3), showing strong seasonal patterns.
Gender, country, and branch show no meaningful differences.

4) Payments And Channels (At Risk)
Around 70% of At‑Risk customers use Instant Payment, making it essential to keep this method fully available.
Google Ads, Instagram Ads, and Shopify generate slightly higher revenue from this segment, indicating strong reactivation potential.



📌 Key Insights

•	Event driven traffic surges generate strong engagement but do not translate into proportional revenue, indicating friction in the conversion funnel.

•	A/B test variations show no measurable uplift over the control group, suggesting issues in test design or insufficient differentiation.

•	At Risk customers represent only 16% of the customer base yet generate the highest revenue—exceeding the Need Development segment (52% of customers) by nearly 9M. This highlights a critical value imbalance and a major retention risk.

•	At Risk customers exhibit spending patterns similar to VIPs, making them a disproportionately valuable segment despite their smaller size.

•	Age is the strongest demographic predictor of churn, with Retirees and Gen X showing the highest vulnerability.

•	Instant Payment is the preferred method among high value customers and correlates with higher order frequency and basket size.

•	Google Ads, Instagram Ads, and Shopify consistently deliver stronger engagement and revenue contribution from At Risk customers compared to other channels.



📌 Recommendations

•	Improve event conversion performance by optimizing landing pages, checkout flow, and product availability to better capture the high traffic generated during events.

•	Redesign A/B test structures to ensure balanced group distribution, clearer variation differences, and more statistically reliable outcomes.

•	Prioritize retention strategies for the At Risk segment, as this group—despite being only 16% of the customer base—drives the highest revenue and outperforms the much larger Need Development segment by approximately 9M.

•	Develop age targeted engagement strategies tailored to Retirees and Gen X, addressing their unique behavioral patterns and churn drivers.

•	Launch seasonal reactivation campaigns during May and August, aligning with historically strong spending periods for At Risk customers.

•	Ensure full availability of Instant Payment across all platforms to support the preferred payment behavior of high value segments.

•	Increase investment in high performing channels such as Google Ads, Instagram Ads, and Shopify to maximize reach and revenue impact among At Risk customers.



📌 Project Files

•	.pbix — Full Power BI report

•	Dashboard published on Power BI Service

•	Dataset (Kaggle source)

•	README documentation


📌 How to Use the Report

The report is fully interactive. Users can:

•	Navigate across the four analytical pages using the top menu.

•	Use slicers to filter by event type, A/B test group, RFM segment, age group, and payment method.

•	Hover over visuals to view detailed tooltips and breakdowns.

•	Explore the dedicated dashboard for a high level summary.

The full interactive report and dashboard are published on Power BI Service for exploration.

