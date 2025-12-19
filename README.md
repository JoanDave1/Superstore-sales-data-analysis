# Superstore-sales-data-analysis

## 1. Introduction

This project explores retail sales performance using the Superstore dataset, focusing on identifying the key factors that drive sales across different regions, customer segments, and product categories. By analyzing four years of sales data (2015–2018), the study aims to uncover patterns in customer purchasing behavior, regional market differences, and category-specific preferences. Understanding these variations is essential for developing data-driven strategies that can improve revenue, optimize product offerings, and strengthen decision-making. 

In addition to using Python and Excel to conduct exploratory and descriptive analysis, this project also includes a time series forecasting component, where historical sales revenue patterns are used to estimate sales revenue under historical conditions for the next 24 months (2019–2020). The forecasting analysis aims to provide insights into expected future sales trends and support data-driven planning and decision-making.

### 1.1 Objectives
The primary objective of this project is to analyze sales performance across regions, customer segments, product categories, and sub-categories to understand:

* Why certain regions generate more revenue than others

* Which customer segments contribute the most to overall sales

* Which product categories and sub-categories perform best

* Why specific categories are preferred in certain regions or segments

Ultimately, the goal is to identify the key factors influencing purchasing behavior and provide actionable recommendations that can improve revenue, optimize product distribution, and support strategic business decisions.

## 2. Data Overview and Description
The dataset contains transactional sales records from 2015 to 2018, covering multiple dimensions of retail operations. Each row in the dataset represents an individual order with details such as:

* Order Date – When the transaction occurred

* Customer ID – Unique identifier for each customer

* Customer Segment – Consumer, Corporate, or Home Office

* Region – Geographic region where the order was fulfilled

* Product Category – Classification of products purchased

* Sales Revenue – Total sales value generated per order

These fields provide a comprehensive view of customer behavior, product performance, and geographic market differences. The dataset is clean, structured, and suitable for time-series, categorical, and segmentation analysis.

## 3. Data Cleaning and Preparation
Before analysis, the dataset was reviewed to ensure data quality and consistency. Although the Superstore dataset was largely clean and well-structured, several standard data validation and preparation steps were performed to confirm its suitability for analysis.

### 3.1. Data Quality Checks

#### Null value checks: 
All relevant columns (order date, customer ID, region, customer segment, product category, sub-category, and sales revenue) were examined for missing values using Excel filters and Python (Pandas). No significant null values were found that would impact the analysis. Null values in postal code column were identified and corrected. 

<img width="304" height="648" alt="image" src="https://github.com/user-attachments/assets/7f0decb4-8e76-4928-9113-f8ceff3c5db3" />

#### Duplicate records: 
The dataset was checked for duplicate rows in both Excel and Python to ensure that each transaction was recorded only once. No duplicate entries were detected.

Overall, the dataset required minimal cleaning, allowing the analysis to focus primarily on uncovering sales patterns and performance drivers rather than data quality issues.

## 4. Exploratory Data Analysis
### 4.1 Regional Sales Performance
The regional sales analysis reveals clear differences in revenue distribution across the Central, East, South, and West regions between 2015 and 2018. It also discloses regional sales across various product categories and customer segments. 

Overall, the West region consistently outperforms all other regions, generating the highest total revenue of $710,219.68, followed by the East region, generating $669,518.73, both surpassing the average sales revenue across the four periods ($565,384). The Central and South regions lag behind, contributing about $400,000 and $300,000 respectively.

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/02470e46-8873-4a9e-ab49-25a3cc6a6f54" />

A year-by-year breakdown shows that this pattern remains stable over time:

2015: West and East regions lead with $145,907.96 and $127,652.82. 

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/b911c1d7-e21c-40e2-a334-a239365c7028" />

2016: East surpasses the West slightly, while South experiences a significant decrease.

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/aa649e06-3d73-41aa-87eb-fd4e9cf76093" />

2017: Both West and East show strong growth, with the West returning as the top performing region.

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/9a3dec31-4511-4d2b-8957-85633ece74cf" />

2018: West records its highest annual sales ($248,130.93), widening the gap between regions.

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/33c30fd8-1e52-4748-b34b-af982c40ea65" />

Across all four years, the West consistently maintains the strongest upward trend, while the South remains the weakest performer despite minor improvements in 2017 and 2018. These trends suggest that regional market size and customer demand may be influencing revenue variations.

Furthermore, results show that overall, Technology generates the highest sales revenue across all regions. A breakdown of the performance of each product category across the various regions is given as follows:

* Furniture: This category generates over $200,000 as revenue in the West and the East regions. The South region remains the lowest sales generating region.

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/9a1cc2e8-5a18-450e-b0e4-966172af138c" />

* Office Supplies: This category generates the highest sales revenue in the West region with $217,466.51. The other regions generate revenue below $200,000, with South, once again, being the lowest performing region. 

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/5aed674b-a244-419a-a449-7a86196aca5c" />

* Technology: As stated above, this product category generates the highest sales value with a total of $827,455.87. However, East becomes the top performing region, followed by West, both surpassing the $200,000 bracket.

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/8b396128-1524-4dff-a503-a83e09ce658b" />

As regards the customer segments, the Consumer segment generates the highest sales revenue across the various regions. The West and East regions surpass the $300,000 bracket being the top performers for this particular segment. Corporate, which is the next-top performing segment generates more sales in the West ($220,018.28), all other regions generating sales below $200,000. Home Office, which happens to be the least performing segment also generates the most sales from the West region. All visualizations for the segments are provided below. 

Consumer: 

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/6a451e79-a77e-4b5b-8e37-332f5d1b55ad" />

Corporate:

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/21c44d07-5edb-4e06-8969-7a2b06d13ea8" />

Home Office: 

<img width="327" height="175" alt="image" src="https://github.com/user-attachments/assets/6d089ef8-b1e0-442d-b6d5-03e8f29fbdcd" />


### 4.2 Product Category Performance
The analysis of product categories shows clear differences in revenue contribution across the three main categories: Technology, Office Supplies, and Furniture. Technology products generate the highest revenue overall with a whooping $827,455.87. Furniture follows closely with $728,658.58. Office Supplies contributes the least revenue with a sum of $705,422.83. All of these are specified below.

<img width="310" height="173" alt="image" src="https://github.com/user-attachments/assets/3424b886-5416-42a4-9a27-c589e10b9e72" />

A year-by-year analysis shows that ths pattern continues in 2015, 2017 and 2018. 2016 and 2018 shows a slightly different result with Furniture exceeding Technology by almost $2,000 in 2016 and Office Supplies outperforming Furniture in 2018. 

2015:

<img width="310" height="173" alt="image" src="https://github.com/user-attachments/assets/b5e0435a-080b-46fc-8bb3-4351bdab15d6" />

2016:

<img width="310" height="173" alt="image" src="https://github.com/user-attachments/assets/d2bc8d93-a5b5-4597-9d02-00f856bd9bf7" />

2017:

<img width="310" height="173" alt="image" src="https://github.com/user-attachments/assets/b35f33df-b8f7-46ed-aabb-09a799ff04b0" />

2018:

<img width="310" height="173" alt="image" src="https://github.com/user-attachments/assets/2a60b25f-f2b3-4df5-ab5f-33ce7f7ded8d" />

Despite Technology being the best performing category, the office supplies category seems to be the most preferred by customers or most popular as more than 50% of the total percentage of customers lean toward this category. In contrast to revenue performance, Technology happens to be the least popular product category. 

<img width="322" height="247" alt="image" src="https://github.com/user-attachments/assets/fb3ff6b5-e061-4e84-8dc0-ffa1a4cf7919" />

### 4.3 Customer Segment Performance
Customer segment analysis shows that the Consumer segment contributes the highest share of total revenue, followed by Corporate and Home Office customers.

<img width="308" height="246" alt="image" src="https://github.com/user-attachments/assets/b383c3b1-94a8-45cf-b09e-b676f715e92e" />

A year-by-year breakdown shows that the Consumer segment generates the highest revenue and also shows that the Consumer segment possesses the highest number of customers between 2015 and 2018. All are shown below. 

2015:

<img width="308" height="246" alt="image" src="https://github.com/user-attachments/assets/97370437-e93c-4982-a4f5-cd64f7f47af9" />

<img width="192" height="81" alt="image" src="https://github.com/user-attachments/assets/3aac24ed-530e-467c-a15f-c7df3f7e29f1" />

2016:

<img width="308" height="246" alt="image" src="https://github.com/user-attachments/assets/9a17a1d7-c9a4-416e-98a1-d73c89cb2c9d" />

<img width="192" height="81" alt="image" src="https://github.com/user-attachments/assets/e3735891-15b9-4782-868b-f8c21711c17b" />

2017:

<img width="308" height="246" alt="image" src="https://github.com/user-attachments/assets/df42e641-5360-492f-8c3d-7b17d794c52d" />

<img width="192" height="81" alt="image" src="https://github.com/user-attachments/assets/761e0aea-6353-49d5-8643-1da5dab18a4c" />

2018:

<img width="308" height="246" alt="image" src="https://github.com/user-attachments/assets/2a759e12-9dff-4ade-be67-83906493d9ba" />

<img width="192" height="81" alt="image" src="https://github.com/user-attachments/assets/db077568-cf1f-4454-b046-b0b057b48ac4" />


## 5. Findings & Recommendations
### 5.1. Regional Sales Performance:
According to the analyses and visualizations above, between 2015 and 2018, the West region surpasses all other regions in terms of sales revenue. This could be due to a greater number of customers in the West compared to other regions. This is also evident in the year 2016 when East has a slightly higher population compared to West. 

Across all regions, Technology also happens to be the most successful product category in terms of revenue, even generating greater revenue from the West region. Despite having the lowest number of customers compared to other product categories, Technology generates the most revenue and this could be linked to a significantly higher unit price for Technology, combined with the greater number of customers in the West. The West and East could also be urban areas where high-value products like Technology are greatly demanded. 

The West region also emerges as the top performing region in the customer segment. Reasons for this could be identical to the reasons stated above. 

Overall, the level of positive performance from the West region can be traced primarily to the higher number of customers in this region compared to other regions amongst other factors

#### Recommendations: 
The following can be adopted to boost the performance of the South and Central regions; 
* Increase the promotion and availability of under-performing products in these regions.
* Conduct surveys and hear directly from customers.
* Increase supply of high-value product sub-categories.
* Encourage regional partnerships to expand customer base

### 5.2. Product Category Performance: 
Analysis and visualization above disclose Technology to be the most successful product category overall despite having a lower customer base compared to other product categories. The product category "Office supplies", is revealed to have a much larger customer base compared to others but generating the least sales revenue. A number of reasons could cause this, some of which could include;
* A significantly higher unit sales price for Technology products in comparison to other product categories.
* Most customers might prioritize and invest more in Technology products, especially with the current need for tech in homes, offices and in day-to-day activities.
* Fewer customers for Technology could make more frequent, larger purchases, which could significantly increase sales revenue.
* Office supplies are most likely sold at cheaper prices per unit of product, hence its popularity among customers.
* Office supplies could also be purchased and used much more frequently especially if there is a presence of a large working class customer base.
* Office supplies could also be sold at lower unit prices, therefore, the presence of a large customer base would cause little to no significant increase in sales revenue.
* In addition to smaller unit prices, there could also be a case of customers buying exactly what they need. In most cases, customers don't need many Office Supplies especially if they're not necessities. Therfore, the average order value as well as revenue remain low. 

#### Recommendations:
The following recommendations can be adopted to maintain and boost Technology's performance as well as the performance of other product categories;
* Technology's revenue is mostly driven by high unit prices, therefore, while the idea of discounts is recommended, care should be taken, especially on high-value Technology products, so as not to affect profit margin.
* To improve Technology's revenue performance, special offers in bundles among Technology product sub-category e.g accessories and phones should be included.
* Unit sales price for Office Supplies can be increased **slighly** so as to improve revenue performance, however, if possible, quality should also be increased. 
* Bulk purchase discounts can also be introduced **strategically** in order to increase the average order value of certain office supplies.
* To retain customers, benefits and rewards could be attached to frequent purchases e.g free shipping, exclusive & early access to new products.
* Focus on retention strategies. For example, convenience, fast-delivery and budget-friendly bundles across various segments.
* Online questionnaires and surveys to hear directly from customers regarding delivery services, product quality and in order areas of concern.

### 5.3 Customer Segment Performance:
Analyses show that Consumer segment happens to be the most successful segment in terms of revenue and also contains the largest number of customers. Home Office segment is the least performing segment in revenue and in total number of customers. 
#### Findings
* Higher purchase frequency in the Consumer segment across various product categories could be a factor contributing to an increase in revenue.
* There is also less specialized purchase in the Consumer segment, meaning that that customers in this segment have the liberty of purchasing from any product category which explain the reason stated above.
* Customers in the Consumer segment are also most likely to make unplanned purchases, most of these purchases happen frequently.
* The Home Office segment probably buys product only when necessary and buys for small or perrsonal business. This causes a low average order value.
* There could also be less frequent purchases by the Customers in the Home Segment as well as more careful and strategic, specialized purchases.

#### Recommendations:
The following recommendations could be adopted to improve revenue for both Consumer and Home Office segments and to retain and increase customers for both segments respectively;
* Reward long term customers with rewards and benefits like free delivery and shipping after 5 orders from a particular category, benefits expire if inactive. This increases engagement. 
* Create Home Office-specific bundles like a home-office starter kit, at affordable prices.

### Sales Forecasting Approach and Assumptions:
Sales for 2019–2020 were forecasted using a machine-learning–based time series approach. Historical sales data (2015–2018) were aggregated at a monthly level, and lag features were created to capture temporal dependencies, trends, and seasonality. A Random Forest regression model was trained using a time-aware train–test split to prevent data leakage and evaluated using RMSE.

Forecasts were generated recursively over a 24-month horizon and represent baseline projections under the assumption that historical sales patterns and customer behavior remain consistent. As with most multi-step forecasts, short-term estimates are expected to be more reliable than long-term projections. The forecasts are intended to support planning and strategic decision-making rather than provide exact future values.

## 6. Conclusion
This project examined sales performance using the Superstore dataset to understand the factors driving revenue differences across regions, product categories, and customer segments between 2015 and 2018. Through exploratory data analysis, the study revealed that the West and East regions consistently outperform others, Technology is the leading revenue-generating category despite a smaller customer base, and the Consumer segment dominates overall sales due to higher purchase frequency and broader product engagement.

Beyond descriptive analysis, the project extended into predictive modeling by forecasting sales for 2019–2020, providing a forward-looking perspective to support planning and strategic decision-making. The findings highlight that revenue performance is influenced not only by customer volume, but also by product mix, pricing dynamics, purchasing behavior, and regional demand patterns.

Overall, this analysis demonstrates how data-driven insights can be used to move from observation to action, informing targeted strategies for revenue growth, customer retention, and operational optimization across multiple business dimensions.
