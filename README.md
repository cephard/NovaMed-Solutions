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

# Data Structure & Initial Checks  

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
The profit margin has remained high, averaging 81.97% over the years.In 2023, revenue peaked at $61.68 million, while revenues for subsequent years, such as 2025, only reached $2.88 million.Doxycycline was the highest-selling drug, generating a revenue of $3.53 million and a profit of $3.36 million, resulting in a profit margin of 95.10%. Other top-selling drugs included Ergocalciferol, Lisinopril, Clonazepam, and Ezetimibe, each making over $3 million in revenue individually.The bottom five underperforming drugs barely reached $1 million in revenue, with Metformin having the highest at $ 607.27 thousand and Warfarin having the lowest at $229.25 thousand. The majority of the bottom five drugs exhibited low profit margins below 35%, with only Prednisone achieving a profit margin of 77.85%.

---

### Overview of Findings

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

### Methodology
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

# Insights Deep Dive

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
      <p>Top</p>
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
  
### Customer Performance

- **Top Customer** Alice Smith emerged as the top customer in terms of high profits contributing to a profit of `344.18` thousand with profit margin of `87.95%`. Although Alice is the top customer, her profits and revenue are only saturated between may and august with a sharp decline in setember having onlt $313.06 in revenue  in september whicjh is low compared tho her top month of july with 108134.08 in july. The drug that has commonly been bought by Alice is Doxycycline which wa 59.85 k of her revenue.
- 
- Bob Williams was the runner up with `329.88k ` profit wich was attribued a revenue of 416.85k as evident  by a spike in revenue in april and july at 93.39 k and 69.47k respectively.
- Carol Smith was the most underperforming customer having a profit thjat is only 0.52% of the profit, however, their profit margin remained at 82.06% implying that the profit margin is not affected by the perfomance of a customer since they prices of the drugs have already been predetmined by Novamed Solutions. 
  
**Buyer Type** 74% of the buyers where users and a 26% where sellers. However in terms of profit Sellers attributed to 87% of theprofit at 30.67m of the total 34.87 profitm. 

<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/customer-performance.png" alt="Customer Analysis" style="width:800px; display:block; margin:auto;"/>
</p>

### Customer Demographics
**Customer segment**
There are various customer segments in the ccustomer base for novamed solutions, such as customer type, Gender, Age, Location, and Customer type.

### Location
<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/rev%20by%20country.png" alt="Customer Analysis"  style="width:800px; display:block; margin:auto;"/>
</p>

- As displayed on the map, Dark Blu represents the highest, yellow as the mid and light blue as the lowest.
1. Canada:-
   - has contributed to be the strongest customer base of 44.11% of the revenue from the reggion
   - Out of the 18.74M revenue from Canada, 52.45% of the revenue was generated by male customers with majority of them being senior(55+).
       
2. Australia
   - is the second largest customer base with 21.49% of the customer base.
   - While this is the second highest revenue region, its revenue is close to the half of Canda's revenue.
   - wITH A TOTAL REVENUE OF 9.13m the majority of the sales are attributed from senior female customers who made 50.49% of the revenue

  In canada the higher chance a customer to buy a drug is if they are a customer type of `prefered customer` while australia has flourished on `frequent buyers`

## customer type
Apatrt frm the Frequesnt buyers who are evenly distribued in terms of age group, preferaed customers and new customers are mostlikely to be senior.
Only seniors have a the lowest numbers of frequent buyers being 20.04% of the seniors. 
Gen X has the majority of frequent buyers amongest them with 45.07% making that number and an even ditribution of gender.
Millenias are also likely to be a freuent buyer with 38.02% of them being repet customers.
45.07% of the Gen X Buyers are frequent buyers. 

<p align="center">
 <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/gender%20AND%20AGE.png" alt="Customer Analysis"  style="width:800px; display:block; margin:auto;"/>
</p>

Gender & Age
- The data has 3 gemnder categories, Male 46.72%, Female 32.03% and Other 21.25%
- In the other gender, 49.26% of them are new customers and they are majorly located in CANADA.
- The male customers are the most customers at 46.72% of all the customers, with 36.84% being a preffered custome located majorly in Canada and Australia.
- Majority of the female customers are frequent buyers with 36.58% of them, The are evely distributed in all locations but majorly inA ustralia, then canada and some in European countries like Germnery France and United kIngdom

<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/gender%20age%20cust%20group%20distribution.png" alt="Customer Analysis"  style="width:800px; display:block; margin:auto;"/>
</p>

# Strategic Recommendations for NovaMed Solutions  

Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:

### 1. Revenue & Profit Optimization  
- 📉 **February underperformance** → Introduce seasonal promotions or discount campaigns to stabilize sales.  
- 💊 **Underperforming drugs** (*Amoxicillin, Fluticasone, Warfarin, Hydrochlorothiazide, Montelukast*) → Bundle with top performers (*Doxycycline, Lisnopril*) or offer targeted discounts.  
- 📦 **Inventory control** → Monitor turnover of low-demand drugs to minimize overstocking and reduce holding costs.  

### 2. Top Drug Strategy  
- 🚀 **Doxycycline and Lisnopril** → Secure long-term supplier agreements to ensure steady availability.  
- 📈 **Marketing focus** → Invest in campaigns to strengthen dominance of top-selling drugs.  
- 🧪 **Portfolio diversification** → Explore new drug categories aligned with top performer trends.  

### 3. Customer Relationship Management  
- 🥇 **Loyalty programs** → Reward top customers (*Alice Smith, Bob Williams*) with exclusive discounts.  
- 📉 **Customer re-engagement** → Target underperforming customers (*Carol Smith*) with personalized offers.  
- 👥 **Segmentation strategy** → Tailor campaigns by customer type and age group (e.g., incentives for **Gen X frequent buyers**).  

### 4. Geographical Expansion  
- 🌍 **Canada (44% revenue)** → Strengthen presence by focusing on preferred senior customers.  
- 🇦🇺 **Australia (21.5% revenue)** → Expand campaigns targeting frequent senior female buyers.  
- 🌐 **Europe (UK, Germany, France)** → Explore opportunities in regions with smaller but growing revenue streams.  

### 5. Operational Efficiency  
- 🏭 **Inventory forecasting** → Leverage Power BI predictive models to align stock with seasonal demand.  
- 🔄 **KPI dashboards** → Deploy real-time Power BI Service dashboards to track revenue, margins, and stock levels.  
- 🕒 **Automated alerts** → Set notifications for low inventory of high-demand products.  

### 6. Future Growth Opportunities  
- 🔮 **Predictive analytics** → Forecast sales performance by drug and region.  
- 📱 **Customer engagement tools** → Develop mobile app or email campaigns informed by demographic insights.  
- 🛒 **E-commerce personalization** → Recommend products based on purchase history, following best practices from leading retail platforms.  

  
# Assumptions and Caveats

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

##Assumptions
- It is assumed that data entry and collection were conducted correctly prior to the analysis.
- The exceptionally high sales in 2023 are likely due to a strategic partnership or collaboration with another supplier, boosting overall revenue.
- The CustomerID corresponding to the Buyer Type in the Fact table had conflicting relationships. It is assumed that the Buyer Type (User or Seller) represents how the customer acquired the medicine—either directly from NovaMed as a user or via a third-party retailer.
- This assumption is necessary because the Fact table violates the 3rd normal form due to a transitive dependency.
- If the data were fully normalized, Buyer Type would belong to the Customer table.
- Therefore, basing results on Buyer Type may slightly misrepresent customer behavior. It is treated as a pseudo key to indicate the acquisition method rather than a definitive attribute of the customer.

##Caveats
- Data Quality Limitations – Some records may contain errors, duplicates, or missing values, which could slightly affect the accuracy of revenue, profit, or customer analyses.
- Buyer Type Interpretation – Since Buyer Type in the Fact table may not fully reflect customer behavior due to normalization issues, insights based on this field should be interpreted with caution.
- External Factors Not Considered – Market dynamics, supply chain disruptions, competitor actions, or regulatory changes were not captured in the dataset but could impact actual sales and profitability trends.
