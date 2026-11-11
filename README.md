# Bank of America Consumer Complaints Analysis | Power BI Dashboard

## Project Overview

This project analyzes consumer complaints submitted against Bank of America between May 2017 and August 2023. Using Power BI, the analysis explores complaint volumes, product-related issues, geographical distribution, company response outcomes, response timeliness, and complaint forwarding performance.

The objective is to transform raw complaint records into meaningful insights that can help identify recurring customer concerns, monitor company response patterns, and highlight areas that may require operational attention.

## Business Objectives

- Understand how consumer complaint volumes change over time.
- Identify the financial products and issues generating the most complaints.
- Examine the geographical distribution of complaints across U.S. states.
- Evaluate company response outcomes and response timeliness.
- Analyze how quickly complaints are forwarded to companies.
- Present findings through interactive Power BI dashboards.

## Dataset Overview

The dataset contains **62,516 complaint records** covering the period from May 2017 to August 2023.

Key fields include:

- Complaint ID
- Submitted via
- Date submitted
- Date received
- State
- Product and sub-product
- Issue and sub-issue
- Company public response
- Company response to consumer
- Timely response?

## Data Preparation and Cleaning

Data preparation was performed before dashboard development to improve consistency and analytical reliability.

Key activities included:

- Examining the dataset structure, column names, data types, and descriptive statistics.
- Checking for duplicate complaint IDs and duplicate records.
- Identifying and reviewing missing values.
- Standardizing data types, particularly date fields.
- Validating complaint dates to identify records where the company received a complaint before its submission date.
- Reviewing category consistency across products, response statuses, and submission channels.
- Creating a calculated `Forwarding Days` field to measure the number of days between complaint submission and receipt by the company.
- Retaining legitimate missing values instead of applying unnecessary imputation.

Missing response information associated with complaints still marked as *In progress* was retained because it represents the recorded status of those complaints rather than an ordinary data-entry omission.

## Data Modeling and DAX

A separate Calendar table was created to support time-based analysis.

The model includes a one-to-many relationship between `Calendar[Date]` and `Consumer Complaints[Date submitted]`.

Key DAX measures developed include:

- Total Complaints
- In-Progress Complaints
- Timely Responses
- Untimely Responses
- Timely Response Rate
- Monetary Relief Complaints
- Same-Day Forwarding Rate
- Average Forwarding Days
- Most Complained Product
- Most Reported Issue
- States Covered

## Dashboard Development

The Power BI report contains two interactive dashboard pages.

### 1. Consumer Complaint Overview & Trends

This page focuses on complaint volumes, product trends, recurring issues, and geographical distribution.

**Key performance indicators:**
- Total Complaints
- Most Complained Product
- Most Reported Issue
- States Covered

**Visualizations:**
- Annual Complaint Trend
- Complaints by Product
- Top 10 Complaint Issues
- Complaints by State (Shape Map)

**Interactive filters:**
- Year
- State
- Product
- Submitted Via

### 2. Company Response & Forwarding Performance

This page examines company response outcomes, response timeliness, and complaint forwarding intervals.

**Key performance indicators:**
- Timely Response Rate
- Untimely Responses
- In-Progress Complaints
- Monetary Relief Complaints
- Same-Day Forwarding Rate
- Average Forwarding Days

**Visualizations:**
- Company Response Distribution
- Timely vs. Untimely Responses
- Monthly Complaint Response Trends
- Forwarding Days Distribution

**Interactive filters:**
- Year
- Product
- State
- Timely Response

## Key Findings

- The dataset contains 62,516 complaint records.
- Checking or savings accounts represent the largest product complaint category, with 24,814 complaints.
- Managing an account is the most frequently reported issue, with 15,109 complaints.
- A total of 58,619 complaints received a timely response, while 2,403 were recorded as untimely.
- The calculated timely response rate is approximately **96.06%**, excluding complaints without a recorded timeliness classification.
- There are 1,494 complaints recorded as in progress.
- A total of 14,697 complaints were closed with monetary relief.
- Approximately **79.39%** of complaints were forwarded to companies on the same day they were submitted.
- The average complaint forwarding interval was approximately 1.22 days.

## Recommendations

Based on the analysis, the following actions are recommended:

1. **Investigate recurring product complaints:** Prioritize reviewing checking and savings account complaints to understand the common causes behind their high volume.

2. **Address frequently reported issues:** Examine account management processes to identify recurring customer difficulties and opportunities for improvement.

3. **Monitor untimely responses:** Regularly review complaints that exceed the required response timeframe and investigate the reasons for delays.

4. **Track unresolved complaints:** Monitor in-progress complaints to support timely follow-up and closure.

5. **Maintain efficient complaint forwarding:** Preserve the strong same-day forwarding performance while investigating cases with unusually long forwarding intervals.

6. **Use geographical patterns for targeted improvements:** Examine state-level complaint concentrations to identify areas that may require additional attention.

## Limitations and Considerations

- The dataset ends on August 28, 2023. Therefore, 2023 represents a partial year and should not be interpreted as a complete annual reporting period.
- Missing values were retained where they represented legitimate reporting conditions, particularly for complaints still in progress.
- The `Forwarding Days` calculation measures the interval between complaint submission and receipt by the company. It does not measure the time taken to resolve a complaint.
- A timely response does not necessarily mean that the consumer was satisfied with the outcome.
- Complaint records indicate reported consumer concerns and should not automatically be interpreted as proof of wrongdoing.
- The analysis is descriptive and does not establish causal relationships.

## Tools and Technologies

- **Power BI Desktop** – Data modeling, DAX calculations, visualizations, and interactive dashboard development.
- **Power Query** – Data inspection, transformation, cleaning, and preparation.
- **DAX** – Measures, calculated metrics, and time-based analysis.

## Project Deliverables

- Power BI dashboard file (`.pbix`).
- Two-page interactive complaint analysis report.
- Data preparation and transformation workflow.
- DAX measures and calculated fields.
- Business findings, recommendations, and limitations.

## Conclusion

This project demonstrates how consumer complaint data can be transformed into an interactive business intelligence report. By examining complaint patterns, product-related issues, company response outcomes, and forwarding performance, the dashboard provides a structured view of the customer complaint landscape.

The analysis highlights areas that deserve further investigation and demonstrates the value of data preparation, data modeling, DAX, and interactive visualization in supporting evidence-based business decisions.

---

**Project Category:** Data Analytics / Business Intelligence  
**Track:** AnalystLab Africa – Track A  
**Visualization Tool:** Microsoft Power BI
