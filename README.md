# [PYTHON] Cohort Analysis: How to Analyze User Retention
# I. Introduction
## 1. About Cohort Analysis
- Cohort is a group of people who share a common characteristic over a certain period of time. A cohort analysis table helps you visualize data for these groups. It allows analysts to compare user behavior across different cohorts at the same points in their lifecycle. This reveals long-term relationships between user characteristics and their actions.
- By analyzing these trends and patterns, you can gain valuable insights into how customers behave over time. This knowledge empowers you to tailor product and service offerings to the specific needs of each identified cohort.
## 2. Types of Cohorts to Analyze
- There are several ways to categorize users for cohort analysis, each offering unique insights. Here's a breakdown of the most common types:
  - **Time Cohorts:** These group users based on when they signed up. Analyzing these cohorts reveals how customer behavior evolves depending on their starting point with your product or service. The timeframe used (monthly, quarterly) depends on your company's sales cycle.
  - **Segment Cohorts:** This approach segments users based on their purchases. For example, users who bought a specific product or subscribed to a particular service level. Customers who opt for basic plans likely have different needs than those who choose advanced options. Understanding these differences allows you to tailor products and services for specific segments.
  - **Size Cohorts:** Here, you group users based on their business size. Imagine categories like small startups, mid-sized businesses, and large enterprises. Each segment has its own set of challenges and needs. By understanding these variations, you can develop offerings that cater to the specific requirements of each size cohort.
## 3. Business Case Study in this project
- Using Python to analyze KPMG transaction data and create a cohort that allows stakeholders to evaluate user engagement beginning with their first transaction.
- This project focuses on performing Cohort Analysis based on Time.
- Customers will be assigned to purchase cohorts based on the month of their first purchase (cohort month).
- The cohort index gets assigned to each of the customer's purchases, showing the number of months from the first transaction.
## 4.  Dataset
Dataset KPMG.xlsx includes one table containing transaction information of customers purchasing products in the year 2017 
![image](https://github.com/lekhuong0196/Cohort-Analysis-How-to-Analyze-User-Retention/assets/138196501/b21c2291-1eaf-4326-b7f7-da12dab474a3)
There are many missing values (in online_order, brand,.. columns) but it does not affect the cohort analysis result => temporarily ignore

Values in 'transaction_id' column are unique => there are no duplicate records in the dataset

We need to filter order_status = ‘Approved’ before cohort analysis
## 5. Method: Cohort analysis
**Cohort analysis definition**
- Cohort analysis is a type of behavioral analytics in which you take a group of users, and analyze their usage patterns based on their shared traits to better track and understand their actions.
- A cohort is simply a group of people with shared characteristics
**Three major types of Cohort**
- Time cohorts: customers who signed up for a product or service during a particular time frame.
- Behavior cohorts: customers who purchased a product or subscribed to service in the past.
- Size cohorts: refer to the various sizes of customers who purchase the company’s products or services.
**Cohort type of this project**
- This project focuses on performing Cohort Analysis based on Time
- Customers will be divided into acquisition cohorts depending on the month of their first purchase (cohort month)
- The cohort index would then be assigned to each of the customer’s purchases, which will represent the number of months since the first transaction
# II. Data Visualization with Python
![image](https://github.com/lekhuong0196/Cohort-Analysis-How-to-Analyze-User-Retention/assets/138196501/5cf5967c-6fc2-4af9-aae9-4c13623f6c52)
![image](https://github.com/lekhuong0196/Cohort-Analysis-How-to-Analyze-User-Retention/assets/138196501/c550cdf1-d9ba-4443-b050-f4fb000dac17)
# III. Insights
- **Overall Stability:** KPMG demonstrates a generally stable retention rate, hovering between 31% and 45% across most months. This indicates a successful core business.
Seasonal Fluctuations: However, the number of new customers acquired each month exhibits a significant decline throughout 2017, dropping from 1347 in January to just 4 by December.
- **Mid-Year Acquisition Spike:** Interestingly, customers acquired between April and July 2017 show the highest retention rates: 48.1% in July (5th month) and 45.1% in April (4th month). This suggests a potential marketing or sales strategy shift during that timeframe that yielded higher customer engagement.
- **Acquisition Window Impact:** Retention rates for customers acquired in the first quarter (January-March) remained relatively stable (33% to 43%). In contrast, customers acquired later in the year (August-October) displayed more volatility, particularly in August (43.1% at month 3, dropping to 25.5% at month 5). This suggests the timing of acquisition may influence long-term retention.
- **Highlighting Top Performers:** Customers who signed up and made their first purchase in July 2017 stand out with an impressive 48.1% retention rate after 5 months. Similarly, those acquired in April 2017 exhibit a consistently high retention rate, reaching 45.1% (month 4), 42.1% (month 5), and 42.7% (month 7). May 2021 also shows a promising trend with a stable retention rate around 40%.
- **Seasonal Trends:** These observations suggest a potential seasonal effect on customer acquisition and retention. Customers acquired mid-year (April-July) tend to demonstrate higher and more stable retention rates compared to those acquired at the beginning or end of the year.
- **Year-to-Date Performance:** It's important to note that KPMG's year-to-date retention remains strong, with rates consistently above 30% (excluding the initial month at 25.5%). This highlights the overall success of their customer retention efforts.
- **Actionable Insights:** These findings offer valuable insights for optimizing future customer acquisition and retention strategies. Focusing marketing efforts during the mid-year period (April-July) might be fruitful. Additionally, investigating factors influencing customer behavior in the first few months after acquisition could improve long-term retention across all acquisition windows.
# IV. Recommendations
- **Investigate Declining New Customers:** While KPMG maintains stable retention, the sharp decline in new customers acquired throughout 2017 requires further investigation. To understand the root cause, consider gathering data on past marketing campaigns, promotions, seasonal trends, and any product quality changes. Analyzing this information can help identify areas for improvement and evaluate the effectiveness of marketing efforts.
- **Leveraging Mid-Year Success:** The superior retention rates observed for customers acquired between April and July suggest a winning strategy during that period. Analyze the characteristics of these cohorts to uncover the key factors driving their engagement. These insights can then be applied to design targeted marketing campaigns or special offers for other months, aiming to replicate this success throughout the year.
- **Retention Boost at Acquisition:** To improve retention rates, particularly for customers acquired in the first few months of the year (January-March), consider implementing attractive preferential programs. These targeted incentives can encourage repeat purchases and increase overall order rates over time.
Replicating Mid-Year Strategies: Unveiling the reasons behind the mid-year cohorts' higher retention is crucial. By delving deeper into this data, including relevant visualizations of other metrics, KPMG can identify successful elements that can be strategically incorporated into marketing campaigns for the remaining months, fostering long-term customer engagement across the entire year.

