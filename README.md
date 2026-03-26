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

**Optimized Data Model Design**  
A high-performance star schema was implemented to ensure efficient query performance and scalability. The model is structured with clearly defined fact and dimension tables, enabling consistent filtering and reliable DAX calculations across all business metrics.

**Dual Fact Table Architecture**  
The model leverages two primary fact tables, OrderHeader and OrderLine, to capture both order-level attributes and item-level transactional details. This structure enables flexible analysis across aggregated and granular views of sales performance.

**Centralized Time Intelligence**  
A dedicated Calendar table serves as the central date dimension. Inactive relationships with ReturnDate and DeliveryDate allow for multi-perspective time analysis using USERELATIONSHIP, supporting accurate reporting across sales, returns, and fulfillment timelines.

## Data Transformation

**Data Quality and Validation**  
A structured data validation process was applied to identify and resolve duplicate records and inconsistencies, ensuring accuracy in revenue, cost, and quantity reporting.

**Operational Risk Metrics**  
Custom metrics were developed to evaluate fulfillment reliability, including High Risk shipment identification and Delay Severity classification. These enable clear visibility into delivery performance and operational exceptions.

**End to End Data Integration**  
Sales, returns, and fulfillment datasets were integrated to create a unified view of the order lifecycle. This allows stakeholders to move from high-level performance trends to detailed drivers of cost and inefficiency.

**Net Performance Calculation**  
All KPIs were modeled to reflect net business performance by incorporating returns, refunds, shipping costs, and restocking fees. This ensures that reported revenue and profitability metrics align with real business outcomes.
