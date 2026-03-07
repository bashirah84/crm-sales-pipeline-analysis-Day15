# crm-sales-pipeline-analysis-Day15
Analyzing CRM and sales pipeline data to understand lead conversion, revenue patterns, and sales performanc
# CRM Sales Pipeline Analysis

## Story
This project analyzes the company’s CRM and sales pipeline data to understand how leads move through different stages and how they are converted into successful deals. By examining information about organisations, industries, products, sales owners, and deal values, the project aims to reveal patterns and insights that can help improve sales performance and revenue generation.

## Problem Statement
The company generates many leads from different countries and industries, but only a small portion of these leads turn into successful deals. Management lacks clear insights into which factors affect deal success, where leads are most likely to drop off in the sales pipeline, and which products or regions contribute the most to revenue. This creates uncertainty in planning and limits potential growth.

## Business Questions
- Which stage of the sales pipeline has the highest lead drop-off?
- Which countries and industries generate the most successful deals?
- Which products bring the highest deal value?
- Which sales owners have the best performance in closing deals?
- What is the average time taken to close a deal from lead acquisition to actual close date?

## 🗂 Dataset Description

The dataset contains information about organizations, leads, sales stages, and deal outcomes within a CRM sales pipeline. Each record represents a potential sales opportunity tracked from the initial lead acquisition stage to the final deal outcome.

The dataset includes information such as:

- Organization name
- Country
- Geographic coordinates (Latitude and Longitude)
- Industry
- Organization size
- Salesperson responsible for the lead (Owner)
- Lead acquisition date
- Product offered
- Sales status and stage
- Deal value
- Probability of closing the deal
- Expected close date
- Actual close date

Below is a preview of the dataset structure.

![Dataset Preview](images/dataset-preview.png)

---

## 🧹 Data Cleaning

Before performing the analysis, the dataset was cleaned and standardized to ensure data quality and consistency.

The following steps were performed:

- Converted the dataset into a structured table format in Excel.
- Verified and standardized text columns such as **Organization, Country, Industry, Owner, Product, and Status**.
- Converted **Latitude and Longitude** from text format to numeric values using the **Text to Columns** feature.
- Ensured **Lead Acquisition Date** was stored in the correct date format.
- Converted **Deal Value** and **Probability (%)** to numeric data types.
- Replaced missing values in the **Stage** column with `"Unknown"`.
- Identified missing values in the **Stage Sequence** column.

Below is a visual representation of the cleaned dataset.

![Data Cleaning](images/data-cleaning.png)

---

## 🏗 Data Modeling

The dataset was structured using a **Star Schema design** inside Excel's **Data Model**.

This modeling approach improves analytical efficiency and enables advanced calculations such as time-based analysis and relationship-driven aggregations.

The data model consists of:

- A **Fact Table** containing sales pipeline transactions.
- A **Date Dimension Table** used for time intelligence analysis.

Below is the data model used for the analysis.

![Data Model](images/data-model.png)

---

## ⭐ Fact Table

The main table contains all transactional records related to the CRM sales pipeline.

Key information stored in this table includes:

- Organization
- Country
- Industry
- Salesperson (Owner)
- Product
- Deal Value
- Probability of closing the deal
- Lead acquisition date
- Actual close date

This table serves as the central source for calculating key performance metrics.

---

## 📅 Date Dimension Table

A separate **Calendar table** was created to support time-based analysis.

The calendar table enables analysis across different time levels such as:

- Year
- Month
- Day
- Day of week

This table is linked to the **Lead Acquisition Date** in the sales pipeline table.

---

## 🔗 Table Relationships

A **one-to-many relationship** was created between the **Calendar table** and the **Sales Pipeline table**.

## 📈 Dashboard 1  
### CRM Sales Pipeline Overview — How Efficient Is Our Sales Funnel?

![CRM Sales Dashboard](crm-dashboard1.png)

### KPIs

- **Total Revenue:** $8.28M  
- **Closed Deals Rate:** 11.80%  
- **Sales Drop-Off:** 348 Leads  
- **Average Time to Close:** 63.17 Days  

---

### Key Insights

- **Laura Thompson** is the top-performing sales agent, generating **over $2M in revenue**, followed by **Michael Brown** and **Jessica Martinez**.

- **Italy** generates the highest number of active leads (**620 leads**), followed by **France (422)** and **Germany (420)**.

- Most leads fall within the **Small (11–200 employees)** and **Medium (201–500 employees)** company segments, suggesting that mid-sized businesses form the core customer base.

- Lead acquisition shows **stable monthly performance**, with **March recording the highest number of captured leads (647)**.

- The **largest drop-off in the sales pipeline occurs at the Opportunity stage**, where **37 potential deals fail to progress**, highlighting a critical point of customer disengagement.

---

### Strategic Implication

The dashboard reveals that while lead generation remains consistent, the **sales pipeline experiences significant drop-offs at early qualification stages**. Improving **lead nurturing, qualification processes, and follow-up strategies** at the Opportunity stage could significantly increase conversion rates and overall revenue performance.



## 📈 Dashboard 2  
### Sales Pipeline Analysis — Where Do Deals Progress or Drop?

![Sales Pipeline Dashboard](Salesphone2.png)

### KPIs

- **Total Revenue:** $8.28M  
- **Closed Deals Rate:** 11.80%  
- **Pipeline Drop-Off:** 348 Leads  
- **Average Time to Close:** 63.17 Days  

---

### Key Insights

- The **Opportunity stage contains the highest number of leads (867)**, indicating strong initial interest but also highlighting the need for effective qualification processes.

- The number of leads **gradually declines as deals progress through the pipeline**, with **Qualified (567)** and **Sales Accepted (528)** representing key transition points.

- A significant number of leads **fail to progress beyond early engagement stages**, suggesting potential inefficiencies in nurturing or follow-up.

- **Laura Thompson remains the strongest performer**, reaching a peak performance score of **749**, significantly ahead of other sales agents.

- Product sales distribution shows that **Services contribute the largest share (40%)**, followed by **SaaS solutions (38%)** and **Custom solutions (22%)**, indicating that service-based offerings dominate revenue generation.

---

### Strategic Implication

The sales pipeline reveals **strong lead inflow but moderate conversion efficiency**. Improving **lead qualification, proposal follow-ups, and early-stage engagement strategies** could reduce pipeline leakage and increase deal closures.

Strengthening support for **high-performing sales agents and expanding high-demand service offerings** may further improve revenue growth and sales efficiency.


## 📈 Dashboard 3  
### Market & Customer Insight — Where Are Our Strongest Markets and Customers?

![Market & Customer Insight Dashboard](Salesphone3.png)

### KPIs

- **Total Revenue:** $8.28M  
- **Closed Deals Rate:** 11.80%  
- **Pipeline Drop-Off:** 348 Leads  
- **Average Time to Close:** 63.17 Days  

---

### Key Insights

- **Italy leads the market with 620 active opportunities**, followed by **France (422)** and **Germany (420)**, indicating that the majority of sales activity is concentrated in a few key regions.

- **Transportation & Logistics is the most active industry with 528 deals**, followed by **Banking & Finance (404)** and **IT & IT Services (387)**, highlighting strong demand from operational and technology-driven sectors.

- Larger organizations contribute significantly to revenue generation, particularly **Enterprise (1001+) and Large (501–1000) companies**, suggesting that high-value deals are concentrated among bigger clients.

- **Laura Thompson has the highest conversion rate (93%)**, significantly outperforming other sales agents, demonstrating exceptional efficiency in converting leads into customers.

- Product distribution shows that **Services and SaaS solutions dominate sales contributions**, while **Custom solutions account for a smaller portion of total deal value**, indicating a stronger demand for scalable service offerings.

---

### Strategic Implication

The analysis shows that **sales performance is strongly influenced by specific geographic markets and industries**, particularly within **European regions and logistics or finance sectors**. Focusing sales resources on these high-performing markets could significantly increase revenue potential.

 leveraging the strategies of **high-performing sales representatives** and prioritizing **enterprise-level clients and service-based offerings** may further improve conversion rates and overall sales growth.


 
---

## Executive-Level Insights

The analysis of the CRM sales pipeline reveals several important patterns related to revenue generation, sales efficiency, and market performance.

- The company generated **$8.28M in total revenue**, indicating strong overall sales activity across multiple regions and industries.

- Despite a healthy pipeline of **4,245 leads**, the **overall conversion rate is 11.8%**, suggesting that a large portion of potential customers drop off during the sales process.

- The **average sales cycle is approximately 63 days**, highlighting the time required to move prospects from initial contact to closed deals.

- Sales activity is **highly concentrated in a few European markets**, particularly **Italy, France, and Germany**, which account for a significant share of total opportunities.

- Industry analysis shows strong demand from **Transportation & Logistics, Banking & Finance, and IT Services**, indicating these sectors are key drivers of sales performance.

- Sales performance varies significantly between agents, with **top-performing representatives demonstrating substantially higher conversion rates**, suggesting that individual sales strategies and experience play a major role in closing deals.

---

## Strategic Recommendations

Based on the insights derived from the dashboards, several strategic actions could help improve sales performance and pipeline efficiency:

- **Improve lead qualification processes** to reduce the large number of leads dropping off early in the sales pipeline.

- **Replicate the strategies of top-performing sales agents** through internal training and knowledge sharing.

- **Focus sales efforts on high-performing markets**, particularly Italy, France, and Germany, where demand is strongest.

- **Strengthen engagement with industries showing the highest deal activity**, such as Transportation & Logistics and Financial Services.

- **Reduce the average sales cycle** by improving follow-up processes and streamlining proposal or negotiation stages.

- **Promote high-performing products and service offerings** that consistently contribute the most to total revenue.

---

## Technical Skills Demonstrated

This project demonstrates several core data analytics and business intelligence skills, including:

- **Data cleaning and preparation** using Excel
- **Data modeling with Power Pivot**
- **Creation of calculated measures and KPIs**
- **Sales pipeline analysis**
- **Customer and market segmentation**
- **Interactive dashboard design**
- **Business-focused data storytelling**

---

## Conclusion

This CRM Sales Analysis project demonstrates how data can be used to better understand sales performance, pipeline efficiency, and market opportunities.

By combining sales metrics, market insights, and customer segmentation, the dashboards provide actionable insights that can support **better sales strategies, improved conversion rates, and stronger market positioning**.
