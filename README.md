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

**Optimized Data Model Design:** A high performance star schema was implemented to support efficient query performance and scalable reporting. The model is structured around clearly defined fact and dimension tables, enabling consistent filtering and reliable DAX calculations across core business metrics such as `Total Revenue`, `Total Profit`, `Profit Margin`, `Total Qty`, and `Net Revenue After Returns`.

**Dual Fact Table Architecture:** The model leverages two primary fact tables, `OrderHeader` and `OrderLine`, to capture both order level attributes and item level transactional detail. This structure supports analysis across aggregated and granular views of performance, including `Total Revenue by Order Date`, `Total Qty by Order Date`, and `Profit Margin by Order Date`.

**Centralized Time Intelligence:** A dedicated `Calendar` table serves as the central date dimension for the model. Inactive relationships with `ReturnDate` and `DeliveryDate` enable multi-perspective time analysis through `USERELATIONSHIP`, supporting accurate reporting across sales, returns, and fulfillment timelines, including `Return Order Count`, `Return Rate`, `% Late Delivery`, `% Ontime Delivery`, and `Average Delivery Delay`.

## Data Transformation

**Data Quality and Validation:** A structured data validation process was applied to identify and resolve duplicate records and inconsistencies, ensuring accuracy across revenue, cost, and quantity reporting. This strengthens the reliability of measures such as `Total Revenue`, `Total Cost`, `Total Profit`, and `Total Qty`.

**Operational Risk Metrics:** Custom metrics were developed to evaluate fulfillment reliability, including `High Risk` shipment identification and `Delay Severity` classification. These measures provide visibility into operational exceptions through KPIs such as `High Risk Count`, `% High Risk`, `Total Shipment Count`, and `Avg Shipment Cost`.

**Net Performance Calculation:** All KPIs were modeled to reflect true business performance by incorporating returns, refunds, shipping costs, restocking fees, and write off activity. This ensures that reported metrics such as `Total Return Cost`, `Write Off Amount`, `Writeoff Rate`, and `Net Campaign Revenue` align with real commercial outcomes.
