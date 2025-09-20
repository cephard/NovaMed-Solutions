# NovaMed-Solutions
![Power BI](https://img.shields.io/badge/Tool-Power%20BI-yellow?logo=powerbi)
![Power Query](https://img.shields.io/badge/Tool-Power%20Query-brightgreen)
![Power BI Service](https://img.shields.io/badge/Platform-Power%20BI%20Service-blue?logo=powerbi)
![GitHub last commit](https://img.shields.io/github/last-commit/cephard/NovaMed-Solutions)

---
## Project Background
NovaMed Solutions is a leading pharmaceutical distributor established in 2022. The company sells prescription medicines through its online store as well as through end-of-the-line chemists and pharmacies. NovaMed serves a diverse healthcare sector, ensuring the availability of essential medications. However, inefficiencies in demand forecasting, stock management, and customer engagement strategies have impacted operational effectiveness.

The company has large data silos containing sales records, customer information, and drug data. Currently, NovaMed is facing challenges in consolidating and optimising sales performance, managing inventory efficiently, and identifying key market opportunities from its multiple data sources.

Since its inception in 2022, the company has gathered comprehensive sales data, including revenue, profit margins, drug performance, and customer demographics. To enhance business strategies and streamline operations through data-driven decision-making, an in-depth analysis was conducted to identify trends and key performance indicators (KPIs).

---
## Key Insights & Recommendations  
Insights and recommendations are provided on the following key areas:
- ✅ **Top/Bottom Analysis:** This involves tracking overall sales metrics, including revenue, profit, and cost of goods sold (COGS).
- ✅ **Month-over-Month Comparison:** An analysis comparing the performance of drugs in terms of revenue and profit with the previous month.
- ✅ **Customer Analysis:** An assessment of how customer segments, such as age group, purchasing category, and gender, influence revenue, profit, and sales.
- ✅ **Geographical Analysis:** An examination of the key revenue sources based on customers' geographical locations, including countries.

📊 **Interactive Dashboard**  
👉 [Download NovaMed Solutions.pbix](https://github.com/cephard/NovaMed-Solutions/raw/main/NovaMed%20Solutions.pbix)

---

# Data Structure & Initial Checks  

NovaMed-Solutions main database structure as seen below consists of four tables: `Sales Fact Table`, `Customer Dim`, `Drug Lookup Dim`, and `Calendar Dim`, with the fact table housing a total row count of **1,826 records**.  

A description of each table is as follows:  

- **Sales Fact Table`** - 
- **Customer Dim** -
- `Drug Lookup Dim** -
- **Calendar Dim**, -
  
## Entity Relationship Diagram  

![Entity Relationship Diagram](https://github.com/cephard/NovaMed-Solutions/blob/main/Entity%20Reletion%20Diagram.png)

---

## Data Cleaning & Transformation  

Before commencing the analysis, the following initial steps were conducted:  
- 📥 **Gathering datasets** from different online locations.  
- 🔄 **Transforming the data** from `CSV` format into `Power Query` for further transformation.  

The data cleaning and transformation process included:  
- 🗑️ **Removing duplicate IDs** and replacing errors with placeholder values or removing them to avoid outliers.  
- 🔧 **Converting column types** into the correct data type, such as changing the `MM-DD-YYYY` format that caused errors into short date conversion by using `Locale`.  
- 👥 **Grouping customer ages** from raw numeric values into age segments such as `Senior`, `Gen X`, `Millennials`, and `Gen Z`.  
- 🔗 **Creating relationships** by establishing 1-to-many links between the dimension tables and the fact table.  
- 📅 **Improving time intelligence** by using both month name and month number to ensure correct month categorisation on the X-axis for line charts.  

---

# Executive Summary

### Overview of Findings

Explain the overarching findings, trends, and themes in 2-3 sentences here. This section should address the question: "If a stakeholder were to take away 3 main insights from your project, what are the most important things they should know?" You can put yourself in the shoes of a specific stakeholder - for example, a marketing manager or finance director - to think creatively about this section.

[Visualization, including a graph of overall trends or snapshot of a dashboard]

# Insights Deep Dive

### Category 1

- **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 1]

### Category 2

- **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 2]

### Category 3

- **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 3]

### Category 4

- **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
- **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 4]

# Recommendations

Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:

- Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
- Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
- Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
- Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
- Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
# Assumptions and Caveats

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

- Assumption 1 (ex: missing country records were for customers based in the US, and were re-coded to be US citizens)
  
- Assumption 1 (ex: data for December 2021 was missing - this was imputed using a combination of historical trends and December 2020 data)
  
- Assumption 1 (ex: because 3% of the refund date column contained non-sensical dates, these were excluded from the analysis)
