# Superstore-sales-data-analysis

## 1. Introduction

This project explores retail sales performance using the Superstore dataset, focusing on identifying the key factors that drive sales across different regions, customer segments, and product categories. By analyzing four years of sales data (2015–2018), the study aims to uncover patterns in customer purchasing behavior, regional market differences, and category-specific preferences. Understanding these variations is essential for developing data-driven strategies that can improve revenue, optimize product offerings, and strengthen decision-making.
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
## 4. Exploratory Data Analysis
### 4.1 Regional Sales Performance
The regional sales analysis reveals clear differences in revenue distribution across the Central, East, South, and West regions between 2015 and 2018. It also discloses regional sales across various product categories and customer segments. 

Overall, the West region consistently outperforms all other regions, generating the highest total revenue of $710,219.68, followed by the East region, generating $669,518.73, both surpassing the average sales revenue across the four periods ($565,384). The Central and South regions lag behind, contributing about $400,000 and $300,000 respectively.

<img width="152" height="94" alt="image" src="https://github.com/user-attachments/assets/dc723e04-6cae-45ba-9229-a115adcf4ea8" />

A year-by-year breakdown shows that this pattern remains stable over time:

2015: West and East regions lead with $145,907.96 and $127,652.82. 

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/faf3413f-82eb-4e79-abaf-97a69724e128" />


2016: East surpasses the West slightly, while South experiences a significant decrease.

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/d69fcce5-7388-4b81-ab2d-b8f48406d2c2" />

2017: Both West and East show strong growth, with the West returning as the top performing region.

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/f36d7b99-8785-4146-96cc-4ec06a5f8652" />

2018: West records its highest annual sales ($248,130.93), widening the gap between regions.

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/7084ba98-e444-4345-8da3-708efd364378" />

Across all four years, the West consistently maintains the strongest upward trend, while the South remains the weakest performer despite minor improvements in 2017 and 2018. These trends suggest that regional market size and customer demand may be influencing revenue variations.

Furthermore, results show that overall, Technology generates the highest sales revenue across all regions. A breakdown of the performance of each product category across the various regions is given as follows:

* Furniture: This category generates over $200,000 as revenue in the West and the East regions. The South region remains the lowest sales generating region.

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/78f98700-20d8-47a3-8c26-71c4a611242b" />

* Office Supplies: This category generates the highest sales revenue is the West region with $217,466.51. The other regions generate revenue below $200,000, with South, once again, being the lowest performing region. 

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/ac8236b2-de04-412e-b333-4ef6f7644e71" />

* Technology: As stated above, this product category generates the highest sales value with a total of $827,455.87. However, East becomes the top performing region, followed by West, both surpassing the $200,000 bracket.

<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/b3deafd9-56ee-44df-be64-0f730a68ac70" />

As regards the customer segments, the Consumer segment generates the highest sales revenue across the various regions. The West and East regions surpass the $300,000 bracket being the top performers for this particular segment. Corporate, which is the next-top performing segment generates more sales in the West ($220,018.28), all other regions generating sales below $200,000. Home Office, which happens to be the least performing segment also generates the most sales from the West region. All visualizations for the segments are provided below. 

Consumer: 
<img width="155" height="97" alt="image" src="https://github.com/user-attachments/assets/1984c0ff-0fb1-4472-8325-711f51d7e62f" />

Corporate: 
<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/953a001a-af95-450c-b8aa-c81ee2416f69" />

Home Office: 
<img width="150" height="97" alt="image" src="https://github.com/user-attachments/assets/bf467ae5-2c2b-409e-b89e-54712621a2c3" />


### 4.2 Product Category Performance

### 4.3 Customer Segment Performance

## 5. Findings & Recommendations
## 6. Conclusion
