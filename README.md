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
## Key Insights
Insights and recommendations are provided on the following key areas:
- ✅ **Top/Bottom Analysis:** This involves tracking overall sales metrics, including revenue, profit, and cost of goods sold (COGS).  
- ✅ **Month-over-Month Comparison:** An analysis comparing the performance of drugs in terms of revenue and profit with the previous month.  
- ✅ **Customer Analysis:** An assessment of how customer segments, such as age group, purchasing category, and gender, influence revenue, profit, and sales.  
- ✅ **Geographical Analysis:** An examination of the key revenue sources based on customers' geographical locations, including countries.  

📊 **Interactive Dashboard**  
👉 [Download NovaMed Solutions.pbix](https://github.com/cephard/NovaMed-Solutions/raw/main/NovaMed%20Solutions.pbix)

## Data Structure & Initial Checks  

NovaMed-Solutions main database structure as seen below consists of four tables: `Sales Fact Table`, `Customer Dim`, `Drug Lookup Dim`, and `Calendar Dim`, with the fact table housing a total row count of **1,826 records**.  

A description of each table is as follows:  

- **Sales Fact Table** - Cosntitutes of the table that consistantly gets updated. The table contains a primary key `SaleID` and foreign keys for other dim tables such as `DrugID`, `CustomerID`, and `Sale Date`. Also includes other columns data `UnitsSold` and `Buyer Type`. `Revenue`, `Profit` and `Cost of Goods` Calculated columns have also been added to the table for analysiss purposes.
- **Customer Dim** - Contains the customer personal data `First Name`, `Last Name`, `Age`, and `Gender`. `Age group` calculated column has been added to best categorize cusromer dimention for analysis.
- Drug Lookup Dim** - Drug details like `RegulatoryComplianceID`,`DrugName`,`UnitSalesPrice`,`CostOfProduction`,`Treats`. The numerical columns of this table contribute to the creation of the calculated columns in thhe FactTable using **RELATED** keyword.
- **Calendar Dim** - Contains a calender custom made to comform with the periods novamed has been in business, includes `Year`, `Month Name`, `Date Month Number` which is essential for the line chart month over month analysis.
  
## Entity Relationship Diagram  
- The model is a `star model` with the fact table at the centre, with connections to the dim tables using their primary keys to create a relationship.
- All the dim tables are a `1-to-many` relationship with the fact table.

![Entity Relationship Diagram](https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Entity%20Reletion%20Diagram.png)

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

## Executive Summary
The profit margin has remained high, averaging 81.97% over the years.In 2023, revenue peaked at $61.68 million, while revenues for subsequent years, such as 2025, only reached $2.88 million.Doxycycline was the highest-selling drug, generating a revenue of $3.53 million and a profit of $3.36 million, resulting in a profit margin of 95.10%. Other top-selling drugs included Ergocalciferol, Lisinopril, Clonazepam, and Ezetimibe, each making over $3 million in revenue individually.The bottom five underperforming drugs barely reached $1 million in revenue, with Metformin having the highest at $ 607.27 thousand and Warfarin having the lowest at $229.25 thousand. The majority of the bottom five drugs exhibited low profit margins below 35%, with only Prednisone achieving a profit margin of 77.85%.

### Key Performance Indicators (KPIs)
<p align="center">
| Metric                  | Value              | Insight                              |
|--------------------------|--------------------|--------------------------------------|
| **Average Profit Margin** | **81.97%**         | Strong profitability across years    |
| **Peak Revenue (2023)**  | **$61.68M**        | Exceptional growth year              |
| **2025 Revenue**         | **$2.88M**         | Significant drop compared to 2023    |
| **Top Drug (Revenue)**   | **Doxycycline – $3.53M** | Highest-selling drug, 95.1% margin |
| **Bottom Drug (Revenue)**| **Warfarin – $229.25K** | Weakest performer, <35% margin      |
</p>
  
---

## Overview of Findings
Below is the overview page from the Power BI dashboard. More examples are included throughout the report.  

<div style="display: flex; gap: 10px; flex-wrap: wrap; justify-content: center; align="center">
  <div style="flex: 1; min-width: 400px;">
    <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Dashboard1.png" alt="Top/Bottom Analysis" style="width: 100%;"/>
    <p style="text-align:center;"><em>Top/Bottom Analysis</em></p>
  </div>

  <div style="flex: 1; min-width: 400px;">
    <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Dashboard2.png" alt="Customer Analysis" style="width: 100%;"/>
    <p style="text-align:center;"><em>Customer Analysis</em></p>
  </div>
</div>

### View the Interactive Dashboard  
🡇 **[View NovaMed Solutions.pbix](https://cephard.github.io/NovaMed-Solutions/)**

---

## Methodology
**NovaMed Solutions: Sales Performance Analysis & Reporting**

The SWOT framework (Strengths, Weaknesses, Opportunities, and Threats) has been utilized to evaluate the sales performance of NovaMed Solutions.
By integrating SWOT analysis with sales metrics and Power BI dashboards, we identify trends, highlight areas for improvement, and anticipate potential challenges that may impact operations.

This structured approach provides strategic insights beyond mere data, supporting informed decision-making to enhance business strategies and optimize overall performance.

**SWOT Breakdown**
**Strengths**
Products such as **Doxycycline** and **Lisinopril**, which have the highest profit margins and the largest sales volumes, serve as core revenue drivers and significantly contribute to the company's profitability.

**Weaknesses**
Underperforming products like **Amoxicillin** and **Fluticasone**, which generate low revenue or possess low profit margins, hinder efficiency and indicate areas that require reevaluation.

**Opportunities**
Untapped markets and customer segments offer potential for revenue growth at relatively low costs. For instance, expanding into **Australia** and implementing targeted campaigns for **Generation X frequent buyers** could be a beneficial move.

**Threats**
External risks include rising costs of raw materials (COGS), declining selling prices, and a substantial drop in annual revenue, which fell from **$5.19 million in December 2023** to a decrease of **59.18% in January 2024**. These factors may place pressure on profit margins and overall competitiveness.

---

## Insights Deep Dive

### Month-over-month comparison
On average, February consistently records the lowest profit and revenue, experiencing a steep -93.33% decline from January. Sales generally recover gradually from March, peaking around May, and remain relatively stable throughout the rest of the year, with only a slight dip in August.

<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/month-on-month.png" 
     alt="Month-over-Month Revenue and Profit Trends" 
     style="width:800px; display:block; margin:auto;"/>
</p>
  
####   2022
- Revenue experienced a sharp decline of 45.04% from January to February.
- There was a recovery in the following months, but June saw another drop of 16.65%.
- From July to September, revenue rebounded; however, the year ended on a weak note, with December recording the lowest levels of both profit and loss.
  
####   2023
- January started strong with a 3900.95% increase over December 2022, but February saw a significant decline of 22.43%.
- Overall, revenue and profit showed steady growth throughout the year, with a notable dip in August at 19.94%.
- December ended slightly negatively with an 8.30% decrease.
  
####   2024
- In January 2024, revenue fell by 59.18% from December 2023. December 2022 ended at $136.43K, while January 2023 surged to $5.46M, a 3900.95% increase, suggesting 2023 was atypical.
- Revenue in 2024 has generally declined, with a slight growth of 55.12%, and a significant drop of 40.20% in September.
- However, December 2024 rebounded strongly, reaching $372.82K, nearly doubling with a 99.99% increase.1-4b60-b5cd-3de2e5db000a" />
  
####   2025
- January started strong with a 30.89% increase; however, February experienced a significant drop of 33.98%.
- Recovery was modest until mid-year, and after April, sales began to decline steadily, hitting their lowest point in November, although September saw a notable spike of 48.96%.
- December ended the year with a remarkable 74.05% increase.

<table align="center">
  <tbody>
   <tr>
    <td>
      <p>2022</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/M-O-M%202022.png" alt="Customer Analysis 2022" width="400">
    </td>
    <td>
      <p>2023</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/M-O-M%202023.png" alt="Customer Analysis 2023" width="400">
    </td>
  </tr>
  <tr>
    <td>
      <p>2024</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/M-O-M%202024.png" alt="Customer Analysis 2024" width="400">
    </td>
    <td>
      <p>2025</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/M-O-M%202025.png" alt="Customer Analysis 2025" width="400">
    </td>
  </tr>
  </tbody>
</table>

---

### Top 5 & Bottom 5 Drugs
<table align="center">
  <tbody>
   <tr>
    <td>
      <p>Top 5 </p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/top%205%20drugs.png" alt="Customer Analysis 2022" width="400">
    </td>
    <td>
      <p>Bottom 5</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/bottom%205%20drugs.png" alt="Customer Analysis 2023" width="400">
    </td>
  </tr>
  </tbody>
</table>

- The top five selling drugs each generate over $3 million in revenue.
- The combined revenue of the bottom five drugs is only $2.36 million, which is less than the revenue of any individual drug on the top five list.
- All of the top five drugs have a high profit margin, exceeding 80%. Conversely, the bottom five drugs exhibit low profit margins, with Montelukast having the lowest at 8.34%. Notably, Prednisone has a profit margin of 77.85%.

---
  
## Customer Performance & Demographics
### Top 5 Customers
<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/customer-performance.png" alt="Customer Analysis" style="width:400px; display:block; margin:auto;"/>
</p>

- **Top Customer** Alice Smith emerged as the top customer in terms of high profits contributing to a profit of `344.18` thousand with profit margin of `87.95%`. Although Alice is the top customer, her profits and revenue are only saturated between may and august with a sharp decline in setember having onlt $313.06 in revenue  in september whicjh is low compared tho her top month of july with 108134.08 in july. The drug that has commonly been bought by Alice is Doxycycline which wa 59.85 k of her revenue.
- 
- Bob Williams was the runner up with `329.88k ` profit wich was attribued a revenue of 416.85k as evident  by a spike in revenue in april and july at 93.39 k and 69.47k respectively.
- Carol Smith was the most underperforming customer having a profit thjat is only 0.52% of the profit, however, their profit margin remained at 82.06% implying that the profit margin is not affected by the perfomance of a customer since they prices of the drugs have already been predetmined by Novamed Solutions. 
  
### Customer Type
<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Quanityt%20by%20Buyer%20Type.png" alt="Customer Analysis" style="width:400px; display:block; margin:auto;"/>
</p>

- The majority of customers, in terms of quantity sold, were direct end users.
- However, the customers who purchased the drugs for resale generated significantly higher revenue, totalling $62.86 million, compared to just $8.45 million from end users. 
- This indicates that while third-party sellers bought fewer drugs, their prices were considerably higher than those sold to end users.

### Location
<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Revenue%20by%20country.png" alt="Customer Analysis"  style="width:400px; display:block; margin:auto;"/>
</p>

On the map, dark blue represents the highest value, yellow mid-value, and light blue the lowest value. 
1. Canada:-has become the strongest customer base, accounting for 44.41% of revenue from the region. Out of the $31.67 million in revenue from Canada, 51.12% was generated by male customers, with the majority being seniors.
2. Australia :- Australia has the second-largest customer base, accounting for 21.39% of the total customer base. Although this region generates the second-highest revenue, its earnings are nearly half of Canada’s revenue. Additionally, 56.37% of the revenue comes from senior female customers.

In canada the higher chance a customer to buy a drug is if they are a customer type of `prefered customer` while australia has flourished on `frequent buyers`

### Age Group
<table align="center">
  <tbody>
   <tr>
    <td>
      <p>Top</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Revenue%20by%20cust%20type.png" alt="Customer Analysis 2022" width="400">
    </td>
    <td>
      <p>Bottom 5</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Revenue%20by%20age%20group.png" alt="Customer Analysis 2023" width="400">
    </td>
  </tr>
  </tbody>
</table>

- The buying habits of different age groups show distinct patterns. While frequent buyers are consistently represented across all age groups, preferred customers and new customers tend to skew toward seniors. 
- Notably, only 19.76% of seniors are classified as frequent buyers, which contrasts with other age groups. 
- Generation X has the highest percentage of frequent buyers at 42.28%, and this group exhibits an even distribution of genders.
 - Millennials also show a strong tendency to make repeat purchases, with 38.02% being frequent buyers. In comparison, 34.92% of Generation Z buyers are frequent purchasers.

### Gender
<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Revenue%20by%20gender.png" alt="Customer Analysis"  style="width:400px; display:block; margin:auto;"/>
</p>

- The data encompasses three gender categories: Male, Female, and Other. Among individuals in the "Other" category, 48.22% are new customers, with a significant number located in Canada.
- Male customers generate the largest portion of revenue, accounting for 46.6% of total revenue. Within this group, 37.24% are preferred customers, with the majority residing in Canada and Australia.
- Female customers primarily consist of frequent and preferred buyers. They are evenly distributed across various locations, with a substantial presence in Australia, followed by Canada and several European countries, including Germany, France, and the United Kingdom.

### Gender and Country
<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/Revenue%20by%20country%20and%20gender.png"  style="width:800px; display:block; margin:auto;"/>
</p>

---

## Strategic Recommendations for NovaMed Solutions  

Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:

### 1. Revenue & Profit Optimization  
- Introduce seasonal promotions or discount campaigns to stabilise sales throughout the year.
- Bundle underperforming drugs like Amoxicillin  with top performers like Doxycycline
- Monitor turnover of low-demand drugs to minimise overstocking and reduce holding costs.
 
### 2. Top Drug Strategy  
- Secure long-term supplier agreements to ensure steady availability for top-selling drugs.
- Invest in campaigns to enhance the market share of top-selling drugs.
- Explore new drug categories aligned with top performer trends.

### 3. Customer Relationship Management  
- Reward top customers like Bob Williams with exclusive loyalty discounts.
- Target underperforming customers (Carol Smith) with personalised offers.
- Tailor campaigns by customer type and age group (e.g., incentives for Gen X frequent buyers).

### 4. Geographical Expansion  
- Strengthen presence by focusing on preferred senior male customers in Canada.
- Expand campaigns targeting frequent senior female buyers in Australia.
- Explore opportunities in regions with smaller but growing revenue streams in Europe.

### 5. Operational Efficiency  
- Leverage Power BI predictive models to align stock with seasonal demand.
- Deploy real-time Power BI Service dashboards to track revenue, margins, and stock levels.
- Set automated notifications to track low inventory of high-demand products.

### 6. Future Growth Opportunities  
- Utilize predictive analytics to forecast sales performance by drug and region.  
- Implement customer engagement tools, such as developing a mobile app or creating email campaigns informed by demographic insights.
- Enhance e-commerce personalization by recommending products based on customers' purchase history, following best practices from leading retail platforms.
  
## Assumptions and Caveats

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

### Assumptions
This analysis accepted an assumption that: 
- The extremely high sales in 2023 are likely due to a partnership with another supplier, boosting revenue.
- The conflicting relationship between CustomerID and Buyer Type (User or Seller) in the Fact table indicates how customers acquired the medicine. This is to maintain normalisation and prevent any ambiguity regarding transitive dependency, as it is essential to store Buyer Type as an attribute in the Customer table, as it is an inherent characteristic of the customer.
- Duplicate SalesID entries had unique values in other columns, indicating a possible data entry error. An indexed SalesID column was created as a primary key for the Fact table.

### Caveats
-  The Buyer Type in the Fact table may not fully represent customer behaviour due to normalisation issues. Therefore, insights derived from this field should be interpreted with caution.
-  The dataset does not account for market dynamics, supply chain disruptions, competitor actions, or regulatory changes, all of which could impact actual sales and profitability trends.

