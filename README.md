# Indian_Banking_Transaction_-2019_2024
Analysis of the Indian Banking Transactions dataset revealed several key insights

# Executive Summary
This project analyzes a comprehensive dataset of 550,000 Indian banking transactions to uncover patterns in customer behavior, evaluate the performance of various transaction channels, and identify operational bottlenecks. By leveraging Python-based data analytics, the project provides actionable insights into transaction volumes, monetary values, and success rates. Key findings indicate that while UPI dominates transaction volume, high-value transfers rely heavily on RTGS. Furthermore, an analysis of failed transactions highlights the Mobile App as a primary area needing technical optimization to improve customer experience.

# Business Problem
In the modern digital banking landscape, customer satisfaction and operational efficiency heavily depend on seamless transaction processing. The bank faces the following challenges:

Channel Optimization: Understanding which payment methods (e.g., UPI, RTGS, Net Banking) are most heavily utilized to allocate server and support resources effectively.

Reliability and User Experience: Failed transactions cause customer frustration and increase support ticket volumes. Identifying where and why these failures occur (by account type or channel) is critical for targeted technical interventions.

Risk & Liquidity Management: Tracking high-value transactions (like RTGS and Cheques) is necessary to ensure liquidity and monitor potential anomalies.

# Methodology
The analysis was conducted using Python, utilizing the following step-by-step approach:

Data Ingestion & Inspection: Loaded the 550,000-row dataset using Pandas and examined data types, columns, and overall structure using .head() and .info().

Data Cleaning: Identified missing values (specifically in the loan_type column) and handled them via zero-imputation (fillna(0)) to ensure downstream calculations did not break.

# Exploratory Data Analysis (EDA):

Filtered subsets of data based on transaction thresholds (e.g., >2,500 and >10,000) and specific payment methods (UPI, Net Banking).

Used aggregations (groupby, mean, max, min) to calculate average transaction amounts across different payment types.

Employed frequency distributions (value_counts, crosstab) to evaluate transaction statuses and usage rates.

Data Visualization: Generated graphical representations (Bar charts and Pie charts) using Matplotlib and Seaborn to intuitively display transaction averages and status distributions.

# Skills Demonstrated
Programming & Libraries: Python, Pandas, NumPy.

Data Wrangling: Handling missing data, filtering, subsetting, and cross-tabulation.

Statistical Analysis: Mean calculation, finding central tendencies, and calculating percentages.

Data Visualization: Creating categorical bar charts and pie charts using Matplotlib and Seaborn.

Business Intelligence: Translating raw data outputs into strategic business conclusions.

# Results
Transaction Volume vs. Value:

Most Used: UPI is the dominant transaction method by volume (153,986 transactions).

Least Used: Credit Cards are the least utilized method (16,426 transactions).

Highest Value: RTGS transactions handle the largest monetary values by far, averaging 269,254.41 per transaction, with the highest single transaction reaching 9,236,223.15.

System Reliability (Transaction Status):

The vast majority of operations process smoothly, with a 92.0% Success rate.

Overall, 4.0% of transactions failed, with the remaining 4% split evenly between 'Reversed' and 'Pending'.

Failure Diagnostics:

By Account Type: Failure rates are highly consistent across account types, ranging narrowly from 3.91% (Salary accounts) to 4.11% (NRI accounts). This indicates that failures are likely systemic rather than tied to specific account products.

By Channel: The Mobile App channel is the largest source of transaction failures, accounting for 8,210 of the failed transactions. This highlights a critical need for IT and development teams to investigate the app's payment gateway stability.
