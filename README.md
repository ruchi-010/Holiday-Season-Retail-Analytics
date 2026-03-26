## Project Background and Overview

Evergreen Commerce is a retail business with a national footprint and strong seasonal dependence during the holiday period. Senior stakeholders requested a structured review of the Christmas trading period to better understand how product demand, campaign activity, returns, and fulfillment outcomes contributed to overall profitability.

## Project Scope

This project evaluates the business from both a commercial and operational perspective by combining product level sales data, campaign records, return transactions, and delivery performance into one integrated Power BI model. The analysis was designed to identify the main drivers of revenue growth, the sources of margin pressure, and the operational factors affecting service quality.

## Key Focus Areas
1. Revenue performance by product, category, and time  
2. Profitability across sales activity and cost structure  
3. Effectiveness of marketing spend and net campaign revenue  
4. Return volume, refund value, and write off exposure  
5. Shipment reliability, delivery delay, and high risk activity  
6. Trends that indicate where management attention is needed most  

## Core Objectives

The purpose of this report is to convert transactional retail data into business insight that supports planning, budgeting, and operational decision making. The final deliverable is intended to give stakeholders a clear understanding of what happened during the season, why it happened, and what actions could improve future performance.

[Download PowerBI Dashbboard here](https://github.com/ruchi-010/Holiday-Season-Retail-Analytics/blob/main/Dashboard.pbix)

## Data Structure

1. **Optimized Data Model Design:** A high performance star schema was implemented to support efficient query performance and scalable reporting. The model is structured around clearly defined fact and dimension tables, enabling consistent filtering and reliable DAX calculations across core business metrics such as `Total Revenue`, `Total Profit`, `Profit Margin`, `Total Qty`, and `Net Revenue After Returns`.

2. **Dual Fact Table Architecture:** The model leverages two primary fact tables, `OrderHeader` and `OrderLine`, to capture both order level attributes and item level transactional detail. This structure supports analysis across aggregated and granular views of performance, including `Total Revenue by Order Date`, `Total Qty by Order Date`, and `Profit Margin by Order Date`.

3. **Centralized Time Intelligence:** A dedicated `Calendar` table serves as the central date dimension for the model. Inactive relationships with `ReturnDate` and `DeliveryDate` enable multi-perspective time analysis through `USERELATIONSHIP`, supporting accurate reporting across sales, returns, and fulfillment timelines, including `Return Order Count`, `Return Rate`, `% Late Delivery`, `% Ontime Delivery`, and `Average Delivery Delay`.

![Screenshot 2026-03-26 002403](https://github.com/user-attachments/assets/2606b59a-4341-44b0-ab4b-600b9ad423e6)

## Data Transformation

1. **Data Quality and Validation:** A structured data validation process was applied to identify and resolve duplicate records and inconsistencies, ensuring accuracy across revenue, cost, and quantity reporting. This strengthens the reliability of measures such as `Total Revenue`, `Total Cost`, `Total Profit`, and `Total Qty`.

2. **Operational Risk Metrics:** Custom metrics were developed to evaluate fulfillment reliability, including `High Risk` shipment identification and `Delay Severity` classification. These measures provide visibility into operational exceptions through KPIs such as `High Risk Count`, `% High Risk`, `Total Shipment Count`, and `Avg Shipment Cost`.

3. **Net Performance Calculation:** All KPIs were modeled to reflect true business performance by incorporating returns, refunds, shipping costs, restocking fees, and write off activity. This ensures that reported metrics such as `Total Return Cost`, `Write Off Amount`, `Writeoff Rate`, and `Net Campaign Revenue` align with real commercial outcomes.

## Executive Summary 

![Screenshot 2026-03-26 164921](https://github.com/user-attachments/assets/0c89b5b4-a3f3-449c-8deb-35946068a3f8)


- The business delivered **$44.84M in revenue** at a **25.20% profit margin**, supported by **$33.54M in marketing spend**. This confirms that the season produced strong **top line growth**, but also that profitability depended on **disciplined control of campaign investment** rather than revenue growth alone.

- Campaign performance was **uneven across the portfolio**. **Holiday contributed 45.84% of revenue and 46.45% of units**, **Black Friday added 34.35% of revenue**, and **Clearance generated the strongest return on investment at 45.03%**, indicating that **scale and efficiency were not aligned across campaign**.

- Category performance was **relatively even**, with the **top category contributing about $483K** and the **lowest categories remaining near the $400K level**, indicating a **broad sales base** rather than reliance on a few dominant categories.

- Fulfillment was a **material constraint**, with **68.65% of shipments delivered late** and **6.64% classified as high risk shipments (shipped after the promised delivery date)**. This indicates a breakdown between promised and actual delivery timelines, creating **service reliability risk during peak trading** and a direct impact on **customer experience**.

- Post sale leakage was **significant**, with **21,709 return orders**, **$5.12M in refund value**, **$2.03M in write offs**, and **net revenue after returns reduced to $39.72M**. The return profile shows that **gross sales overstated true commercial performance** and that **product quality, fit, or delivery issues** likely had a measurable financial cost.

## Insights

## Acquisition Analytics
- Black Friday delivers strong revenue scale, but at $759.79 cost per order, it remains significantly less efficient than Clearance, which operates at $626.29 per order with 52.86% ROI. At the same time, the Holiday campaign absorbs over 50% of total marketing spend ($17.01M) while generating only 8.86% ROI, confirming that incremental spend at scale is driving diminishing returns and capturing lower-intent demand rather than improving acquisition quality.

- The consistent decline in cost per order from Holiday to Clearance, combined with the relatively strong performance of Cyber Monday (24.75% ROI), indicates that customer intent increases as campaigns become more targeted and time-bound. This suggests that pricing strategy and urgency-driven promotions are materially more effective than prolonged seasonal campaigns in driving efficient demand.
