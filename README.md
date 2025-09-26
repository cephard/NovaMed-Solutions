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

---

# Data Structure & Initial Checks  

NovaMed-Solutions main database structure as seen below consists of four tables: `Sales Fact Table`, `Customer Dim`, `Drug Lookup Dim`, and `Calendar Dim`, with the fact table housing a total row count of **1,826 records**.  

A description of each table is as follows:  

- **Sales Fact Table** - Cosntitutes of the table that consistantly gets updated. The table contains a primary key `SaleID` and foreign keys for other dim tables such as `DrugID`, `CustomerID`, and `Sale Date`. Also includes other columns data `UnitsSold` and `Buyer Type`. `Revenue`, `Profit` and `Cost of Goods` Calculated columns have also been added to the table for analysiss purposes.
- **Customer Dim** - Contains the customer personal data `First Name`, `Last Name`, `Age`, and `Gender`. `Age group` calculated column has been added to best categorize cusromer dimention for analysis.
- Drug Lookup Dim** - Drug details like `RegulatoryComplianceID`,`DrugName`,`UnitSalesPrice`,`CostOfProduction`,`Treats`. The numerical columns of this table contribute to the creation of the calculated columns in thhe FactTable using **RELATED** keyword.
- **Calendar Dim** - Contains a calender custom made to comform with the periods novamed has been in business, includes `Year`, `Month Name`, `Date Month Number` which is essential for the line chart month over month analysis.
  
## Entity Relationship Diagram  

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

### Overview of Findings

Overall, the profit margin has been very high, averaging `82.06%` from 2022 to the current year. In 2023, revenue peaked at `39.26` million dollars, while revenues in recent years, such as 2025, barely hit the 1 million mark, totaling `914.52` thousand dollars. Out of the `10,000` total goods sold, `Lisnopril` accounted for `67.96%` of the total sales. However, `Doxycycline` emerged as the top drug for profit and revenue, generating `2.2` million dollars in profit and `2.3` million dollars in revenue, with `Lisnopril` as the runner-up at 2.1 million dollars in revenue and 1.9 million dollars in profit. Underperforming drugs, including amoxicillin, fluticasone, warfarin, hydrochlorothiazide, and montelukast, ranged between 18.77 thousand dollars for the lowest and 82.59 thousand dollars.

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

### Download the Interactive Dashboard  
🡇 **[Download NovaMed Solutions.pbix](https://github.com/cephard/NovaMed-Solutions/raw/main/NovaMed%20Solutions.pbix)**


### Methodology
**NovaMed Solutions: Sales Performance Analysis & Reporting**

The SWOT framework (Strengths, Weaknesses, Opportunities, and Threats) has been utilized to evaluate the sales performance of NovaMed Solutions. By integrating SWOT analysis with sales metrics and Power BI dashboards, we identify trends, highlight areas for improvement, and anticipate potential challenges that may impact operations. 

This structured approach provides strategic insights beyond mere data, supporting informed decision-making to enhance business strategies and optimize overall performance.

**SWOT Breakdown**
- **Strengths**: Products such as `Doxycycline` and `Lisnopril`, which have the highest profit margins or largest sales volumes, serve as core revenue drivers and contribute significantly to the company's profitability.
  
- **Weaknesses**: Underperforming products, such as `Amoxicillin` and `Fluticasone`, with low `revenue` or `profit margins`, reduce efficiency and highlight areas that need reassessment.
  
- **Opportunities**: Untapped markets and customer segments present potential for revenue growth at relatively low costs. For example, expansion into Australia and targeted campaigns for Generation X frequent buyers could be beneficial.
  
- **Threats**: External risks include rising costs of raw materials (COGS), declining selling prices, and a significant decrease in annual revenue, which plummeted from $39.26 million in 2023 to $914,000 in 2025. These factors may exert pressure on profit margins and overall competitiveness.

# Insights Deep Dive

### Month-over-month comparison
On average, February consistently records the lowest profit and revenue, experiencing a steep -93.33% decline from January. Sales generally recover gradually from March, peaking around May, and remain relatively stable throughout the rest of the year, with only a slight dip in August.

<p align="center">
<img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/month-on-month.png" 
     alt="Month-over-Month Revenue and Profit Trends" 
     style="width:800px; display:block; margin:auto;"/>
</p>
  
####   2022
- Revenue fell sharply from January to March: first by -43.21%, then by -21.30%.
- Recovery followed in subsequent months, but a drastic decline of -81.26% occurred in June.
- July saw a rebound, though the year closed weakly with a -65.29% drop in November.

####   2023
- January started stronger with a +9.18% increase compared to December 2022.
- However, February quickly reversed this with a -26.38% decline.
- Revenue and profit showed steady growth throughout the year, with only minor dips—August being the worst (-15.61% revenue, -15.83% profit).
- Despite the strong start, the year closed slightly down in December (-5.67% revenue, -5.74% profit).

####   2024
- 2023 ended at 3.39M revenue, but January 2024 plummeted to 56.65K, a shocking -98.33% drop.
- This is especially notable given December 2022 closed at 89.76K, and January 2023 surged to 3.59M (+3901.30%), suggesting 2023 may have been an outlier year.
- March 2024 marked the year’s peak revenue at 134.98K.
- Sales held steady until September, which saw a -48.02% dip from August.
- The year ended weak again, closing December at 44.81K revenue and 42.32K profit.
  
####   2025
- January began with a +12.20% increase, but February collapsed with a -91.82% decline.
- Recovery was modest through mid-year, but after April, sales consistently trended downward, reaching the year’s lowest in November (23.05K revenue, 20.64K profit, representing -69.50% and -67.37% declines from October).
- Encouragingly, December closed with a strong rebound, ending the year at 144.23K revenue (+525.82%) and profit up +444.56% compared to November.


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

### Top 5 & Bottom 5 Drugs

<table align="center">
  <tbody>
   <tr>
    <td>
      <p>2022</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/top%205%20drugs.png" alt="Customer Analysis 2022" width="400">
    </td>
    <td>
      <p>2023</p>
      <img src="https://github.com/cephard/NovaMed-Solutions/blob/main/Images/bottom%205%20drugs.png" alt="Customer Analysis 2023" width="400">
    </td>
  </tr>
  </tbody>
</table>

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
