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
