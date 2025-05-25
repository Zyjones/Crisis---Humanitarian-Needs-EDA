# 🧭 Humanitarian Needs and Funding Analysis (2010–2024)

## 📌 Project Overview

This project analyzes global humanitarian needs and funding trends from 2010 to 2024, leveraging datasets from the Humanitarian Action website. The primary goal is to uncover patterns in funding gaps, regional disparities, population needs, and types of humanitarian appeals.
## 📂 Data Sources
We use the following datasets provided by Humanitarian Action:
* **Raw Data** — Country-level humanitarian indicators across metrics and years


* **Funding Requirements** — Annual financial requirements for humanitarian response


* **Funding Received** — Contributions received per country per year


* **Data by Year** — Aggregated yearly statistics


* **Data by Plan** — Metadata on humanitarian plans and appeal types


## 📊 Column Definitions
Key variables used in our analysis include:

* year - Calendar year of the appeal or report
* country - Country or territory targeted by the humanitarian response
* people_in_need - Estimated number of individuals requiring humanitarian aid
* people_targeted - Number of individuals targeted by aid interventions
* funding_requirements - Total funding requested to address humanitarian needs
* funding_received - Actual funding received
* funding_gap - Difference between required and received funding
* coverage_percentage - Percentage of funding needs that were met
* appeal_type - Type of humanitarian plan (e.g., HRP, Flash Appeal)



## **🔬 Methodology**
* All data processing and analysis were conducted using Python with pandas, numpy, matplotlib, and seaborn.
* This was a collaborative project in which each group member took on a specific research question so that we can have a comprehensive understanding of humanitarian needs and funding. 

**🧼 Data Preparation**
* Cleaned and standardized column names and formats
* Converted financial and population metrics from string to numeric
* Mapped country codes to regions through the creation of a dictionary


**📈 Analytical Techniques**
* Time Series Analysis: Funding trends and people in need over time
* Aggregation & Grouping: Summarized data by year, country, region, and appeal types. 
* Correlation & Regression: Assessed relationships between variables
* Outlier Detection: Identified anomalies in funding and population metrics
* Distribution Analysis: Evaluated normality of funding requirements,, funding received, and funding coverage using distribution curves (histograms with KDE).
* Cumulative Metrics: Tracked cumulative funding by region and year


**📊 Visualization**
* Line plots for temporal trends
* Bar charts and heatmaps for cross-sectional comparisons
* Scatterplots for correlation exploration


## **🧠 Research Questions and Findings**

### **Trends in Global Funding and Coverage (Corry)**
1. **What are the trends in the funding gap (difference between requirements and funding) and the average annual funding coverage (percentage of requirements met)?  What is the distribution of funding requirements, funding received, and funding coverage across all country-year instances?**

**Global Evolution of Humanitarian Funding (2010-2024):**
- **Overall Growth with Fluctuations:** Global humanitarian funding generally increased from 2010, reaching a significant peak around  2019, before experiencing a notable decline in the subsequent years. This suggests periods of increased donor response followed by contraction.
- **Widening Funding Gaps:** 
While both funding requirements and funding received have shown an upward trend over the period, the increase in requirements has outpaced the increase in received funding. This has resulted in a consistently widening funding gap, indicating a growing unmet need for humanitarian assistance globally.
- **Inconsistent Funding Coverage:** 
The global funding coverage, which represents the percentage of requirements met, has fluctuated overtime but has consistently remained below 60%. This highlights a persistent challenge in adequately funding global humanitarian operations, meaning that, on average, a substantial portion of the required aid is not secured.

**Evolution Across Countries and Distribution of Funding Coverage:**

- **Skewed Funding Distribution:** 
The total humanitarian funding received per country is highly unevenly distributed. A small number of countries receive a disproportionately large share of the overall funding, while many other countries receive significantly less. This indicates a concentration of resources in specific crises or regions.

- **Strong, but Imperfect, Correlation between Requirements and Received Funding:** 
The Pearson correlation coefficient of 0.873 between funding requirements and funding received indicates a strong positive relationship. This means that as humanitarian needs increase in a country, the funding it receives generally also increases. However, since the correlation is not 1.0, it suggests that other factors or limitations prevent funding from perfectly matching requirements, leading to varying levels of unmet needs despite high requirements.

- **Skewed Distribution of Funding Coverage:** 
The distribution of funding coverage across countries is notably skewed. This implies that while a few countries or crises might achieve relatively high funding coverage, a larger number of countries experience significantly lower coverage. This imbalance means that the effectiveness of humanitarian response, in terms of meeting needs, varies drastically from one context to another. The distribution is not balanced; it is heavily weighted towards lower coverage for many, with a few exceptions.

In conclusion, humanitarian funding has grown but struggles to keep pace with escalating global needs, leading to persistent and widening funding gaps. The distribution of this funding and its coverage is highly skewed towards a few recipients, highlighting significant disparities in how effectively humanitarian needs are met across different countries.


### Top Countries in Need and Funding (Jessica L.)
2. **Which countries have the highest needs and funding levels? Is there a correlation between population in need and funds received?**
**Which countries had the most people in need?**
*The top five countries that consistently had a high number of people in need between 2010 and 2024 are: Syria (SYR), Yemen(YEM), Democratic Republic of the Congo (CON), Afghanistan(AFG), and Ethiopia(ETH). These countries appeared in the top ranks across the chosen span of years-showing chronicly severe humanitarian demand.*

**Did they also receive the most funding?**
*According to the results in Step 5, not all of these countries received the most funding.  SYR and YEM received high funding almost proportional to their needs. ETH and COD, while having substantial needs, did not appear among the top five recipients.*


**Is there a pattern over time?**  
*In the year-to-year comparison, we see the following trend for people in need:*   
- 2010-2014: number of people in need fluctuated moderately
- 2015: number of people in need increased significantly
- 2020-2023: the peak of number of people in need


*In the year-to-year comparison, we see the following trend for funding received:*
- 2018-2019: spikes of funding received are observed
- 2022-2024: zero reported funding, possibly due to missing data  
The funding received did not increase consistently to match the need. This suggests that the needs were growing faster than the funding, especially in the later years of observance.


In conclusion, this analysis partially supports our hypothesis of more people equate to more funding provided. The correlation coefficient of 0.58 between people in need and funding received suggests a moderate positive relationship. The 0.99 correlation between funding received and funding requirements suggests the requirements are set based on funding capacity. Some higher need countries were underfunded, including a few of the top five countries in need. Thus, there is a need to observe other factors as influences on funding decisions. Recommendation for future exploration would be to investigate other potential factors in underfunded countries, including but not limited to examples- such as: location, political interests, and donor focus.


### Appeal Types and Funding (Zakiyyah)
3. **What appeal types exist and how have the frequency of appeal types changed overtime? What is the relationship between funding and appeal plans?** 

* Humanitarian appeals are requests for funding and resources to address the immediate needs of people affected by crises. There are 8 appeal type plans: 
    * Flash Appeal (FA)  
    * COVID-19 (Intersectoral)
    * COVID-19
    * Consolidated Appeal Process (CAP)
    * Non Humanitarian Response Plan
    * Humanitarian Response Plan (HRP)
    * Other
    * Regional Refugee Response Plan (RRP)


* Overall, the rate of appeal types has increased between 2010 and 2024. The year with the most appeal types shown appeared in 2022 and 2023 with 92 appeal types total. The year 2010 had the lowest number of appeal types with 32.


* The Humanitarian Response Plan HRP is the plan that has the highest frequency with the count being 484. The next highest was Consolidated Appeal Process (CAP) with the count being 185. 


* Regional Refugee Response Plan (RRP) receive the most funding on average $575,231,098 dollars which is interesting considering that the Regional Refugee Response Plan (RRP) are the third most popular appeal type. 
* The Regional Refugee Response Plan (RRP) has the highest funding requirements $1,638,478,655 out of the other appeal types on average and in total. 
* Humanitarian Response Plan (HRP) received the most funding with a total of $ 5,334,636,169.  

![alt text](Appeal_Time.png)

### Regional Disparities Over Time (Hacheming)

**5a. How do funding requirements vary across regions?** 

* Funding requirements vary significantly by region. The Middle East and Africa, particularly after 2015, consistently report the highest funding needs. These regions also have higher populations in need, contributing to their larger funding requests. Distribution analysis shows funding requirements are right-skewed, with most regions requesting lower amounts and a few—especially the Middle East and North Africa—requesting significantly more.

![alt text](Distributions_Metric.png) 


**5b. Are certain regions consistently underfunded?**
* Yes. Across all regions and years, funding received falls short of requirements. Even in high-need regions like the Middle East and Africa, the funding gap persists. For example, the correlation between people in need and funding received in these regions is relatively strong (r = 0.70), yet full funding is still not achieved. In West & Central Africa, the correlation between people in need and people targeted is also high (r = 0.74), but the missing data for people targeted limits conclusions. Overall, the persistent gap highlights a systemic shortfall in global humanitarian funding.

![alt text](Funding_Region.png) 


## 📁 Folder Structure
* Humanitarian Needs Data/
*   Data/
    * Raw Data.csv
    * Funding Requirements.csv
    * Funding Received.csv
    * Data by Year.csv
    * Data by Plan.csv
*  Notebooks/
    * EDA
* ReadME.pd 


## 🚧 Next Steps
* Conduct correlation and regression analysis
* Develop dashboard-ready visualizations
* Compile results into a final report and presentation
