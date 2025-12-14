# Superstore-sales-data-analysis

## 1. Introduction

This project explores retail sales performance using the Superstore dataset, focusing on identifying the key factors that drive sales across different regions, customer segments, and product categories. By analyzing four years of sales data (2015–2018), the study aims to uncover patterns in customer purchasing behavior, regional market differences, and category-specific preferences. Understanding these variations is essential for developing data-driven strategies that can improve revenue, optimize product offerings, and strengthen decision-making. 

In addition to using Python and Excel to conduct exploratory and descriptive analysis, this project also includes a time series forecasting component, where historical sales revenue patterns are used to predict sales revenue for the next 24 months (2019–2020). The forecasting analysis aims to provide insights into expected future sales trends and support data-driven planning and decision-making.

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
* Offer discounts on some of these high-value products that seem not be performing well in these regions.
* Increase the promotion and availability of under-performing products in these regions.
* Conduct surveys and hear directly from customers.
* Increase supply of high-value product sub-categories.
* Encourage regional partnerships to expand customer base

### 5.2. Product Category Performance: 
Analysis and visualization above disclose Technology to be the most successful product category overall despite having a lower customer base compared to other product categories. The product category "Office supplies", is revealed to have a much larger customer base compared to others. A number of reasons could cause this, some of which could include;
* A significantly higher unit sales price for Technology products in comparison to other product categories.
* Most customers might prioritize and invest more in Technology products, especially with the current need for tech in homes, offices and in day-to-day activities.
* Fewer customers for Technology could make more frequent, larger purchases, which could significantly increase sales revenue.
* Office supplies are most likely sold at cheaper prices per unit of product, hence its popularity among customers.
* Office supplies could also be purchased and used much more frequently especially if there is a presence of a working class customer base.

#### Recommendations:


## 6. Conclusion
