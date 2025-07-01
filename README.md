# My Project
## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools used](#tools-used)
- [Data Cleaning Preparation](#data-cleaning-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [My Analysis](#my-analysis)
- [Results](#results)
- [Conclusion](#conclusion)
  
# DSA-Data Analysis Capstone Project

### This is how i started my portfolio building while taking my Data Analysis class with the incubator hub

### At the incubators hub, i had the opportunity of learning a number of things ranging from Ms Excel to SQl to my portfolio building and now to my power Bi

 ##  Project Topic: Amazone Product Review Analysis

 ##  Project Overview
 ### the Data Analysis project aims to generate insight into the product performance and customer review for E-commerce analytic solutions that can guide product improvement, marketing strategies, and customer engagement. By analysing the various parameters in the data received we seek to gather enough insight to make reasonable decisions which then enables us to tell compelling stories around our data from the insight gotten and to know the best performance from our data.
 
### Data Sources
The primary sources of Data used here is Data Amazon case study.xlsx file and this is downloaded from my dashboard on Canvas LMS

### Tools used
- Ms Excel for Data Cleaning  [Download Here](https://www.microsoft.com)
    - For Data Collection
    - For Data Cleaning
       1. Data Manipulation
         
- Power Bi [Download]([For creating a report](https://www.microsoft.com/en-us/download/details.aspx?id=58494))
- Ms power point ( for presentation)
  
### Data Cleaning Preparation
In the initial phase of the Data cleaning and preparation, we perform the following 
action;
1. Data loading and Ispection
2. Handling missing variables
3. Data Cleaning and formating
-Steps Followed to clean the Data Are:
    -I Highlight all the Data and click the Data tab, and then the Data Tool group click on it ,you will see a dialogue box. Click Unselect all fisrt, then product _id and then cick ok. you will have your unique or distinct product. The next step is to get the category which is key in all. To execute this, i had to copy and paste the category to a new worksheet to split it because it is a multi-level category and i observed that there is a common delimiter that seperated the text so i clicked on the delimiter and copy it to the clipboard. So i highlighted the category column and click text to columns to open a dialogue box and i clicked next and pasted the delimiter into the other box and click finish. by doing that, you have your category now spread across 5 columns, next is to rename them.  After doing that, i returned back to the main data set and and highlight columns that will accomodate four more category headers and then clicked insert which created a space for me and so i copied the four columns from the category split sheet and pasted it on the main data set and so i deleted the category split sheet. The next thing i did was to confirm that all my columns are reliable, so i used filter tools to validate each column, and since i wasn't so sure about deleting incomplete record, i got them fixed by assigning a value. For instance, i assigned zero where there was blank record and and symbol . After doing all the cleaning, i proceeded to calculated columns.

### Exploratory Data Analysis
EDA involved in the exploring of the data to answer some questions about the Data such as;
-	What is the average discount percentage by product category? 
-	How many products are listed under each category? 
-	What is the total number of reviews per category?  
-	Which products have the highest average ratings? 
-	What is the average actual price vs the discounted price by category? 
-	Which products have the highest number of reviews? 
-	How many products have a discount of 50% or more? 
-	What is the distribution of product ratings (e.g., how many products are rated 3.0, 
4.0, etc.)? 
-	What is the total potential revenue (actual_price × rating_count) by category? 
-	What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)? 
-	How does the rating relate to the level of discount? 
-	How many products have fewer than 1,000 reviews? 
-	Which categories have products with the highest discounts? 
-	Identify the top 5 products in terms of rating and number of reviews combined. 
-	Final Task: Dashboard Creation 
Using your cleaned dataset and pivot outputs, build an Excel dashboard. Unleash your Creativity 


### My Analysis

