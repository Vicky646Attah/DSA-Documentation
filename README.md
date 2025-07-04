# My Project
## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools used](#tools-used)
- [Data Cleaning Preparation](#data-cleaning-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [My Analysis](#my-analysis)
- [Results](#results)
- [Limitation](#limitation)
- [Recommendation](#recommendation)
- [Conclusion](#conclusion)

# DSA-Data Analysis Capstone Project


 ## PROJECT TOPICS - Case study 1 Amazon Product Review Analysis, and Case study 3 Palmora Group HR Analysis
 
 ##  Project Overview
 ### the Data Analysis project on Amazone aims to generate insight into the product pricing, discounts, ratings and customer review using Excel Pivot Tables, marketing strategies. By analysing the various parameters in the data received we seek to gather enough insight to make reasonable decisions which then enables us to tell compelling stories around our data from the insight gotten and to know the best performance from our data, and offer recommendation based on outcome of the analysis.
 
### Data Sources
The primary sources of Data used here is Data Amazon case study.xlsx file, this is downloaded from my dashboard on Canvas LMS

### Tools used
- Ms Excel for Data Cleaning  [Download Here](https://www.microsoft.com)
    - For Data Collection
    - For Data Cleaning
       1. Data Manipulation
         

  
### Data Cleaning Preparation
In the initial phase of the Data cleaning and preparation, we perform the following 
action;
1. Data loading and Ispection
2. Handling missing variables
3. Data Cleaning and formating
-Steps Followed to clean Amazone Product review Data Are:
    -I Highlight all the Data and click the Data tab, and then the Data Tool group click on it ,you will see a dialogue box. Click Unselect all fisrt, then select product _id and then cick ok. you will have your unique or distinct product. The next step is to get the category which is key in all. To execute this, i had to copy and paste the category to a new worksheet to split it because it is a multi-level category and i observed that there is a common delimiter that seperated the text so i clicked on the delimiter and copy it to the clipboard. So i highlighted the category column and click text to columns to open a dialogue box and i clicked next and pasted the delimiter into the box and click finish. by doing that, you have your category now spread across 5 columns, next is to rename them.  After doing that, i returned back to the main data set and and highlight columns that will accomodate four more category headers and then clicked insert which created a space for me and so i copied the four columns from the category split sheet and pasted it on the main data set and so i deleted the category split sheet. The next thing i did was to confirm that all my columns data are reliable, so i used filter tools to validate each column, and since i wasn't so sure about deleting incomplete record, i got them fixed by assigning a value. For instance, i assigned zero where there was blank record and symbol . After doing all the cleaning, i proceeded to including calculated columns where appriopraite 

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

 1. Average discount percentage by product category
   - i calculated average discounct by using the formular
   = (Actual Price - Discounted Price) / Actual Price * 100
   =₹1000.00-₹499.00/₹1000.00*100= 50%
   Then i used a Pivot Table to summarise the data by Average

   Rows: Category= 630.72

   Values: Discount % → summarize by Average =0.47

2. How many products are listed under each category, I used 
    Pivot Table to determine the amount

    Rows: Category

    Values: Product Name → set to Count (Distinct) and it returned 1,351.00

 3. Total number of reviews per category
   I used Rating Count column to determine the out come and summarised using 

   Pivot Table:

   Rows: Category

   Values: Rating Count → Sum

4. Which products have the highest average ratings
   I Sorted my dataset by the Average Rating column (descending)

   I Pick top entries as
  -Electronics=1998.1,
  -Home&Kitchen=1806.2 and
  -Computers&Accesories=1557.7

5. Average actual price vs discounted price by category
    I used Pivot Table :

    Rows: Category

    Values: Actual Price → Average =5691.2
   Discounted Price → Average =3305

 6. Which products have the highest number of reviews
   Sort Rating Count column in descending order
   - Electronic has the highest

 7.How many products have a discount of 50% or more
  I Added calculated column and used the formular
  =IF(Discount % >= 50, "Yes", "No") 
  and then i used Filter to determine my answer
   and i arrived at 662 products have a discount of 50% or more

 8. Distribution of product rating
    - I used Pivot Table:

    Rows: Rating 

   Values: Product Name → Count. 

9. Total potential revenue by category (Actual Price × Rating Count)
   - I Added a calculated column and multiply the Actual price by Rating count as seen
   =Actual Price * Rating Count
   =₹1000*₹23 = ₹23,000

    and i used Pivot Table tosummerise the values

    Rows: Category

    Values: Potential Revenue → Sum


10. Number of unique products per price range bucket
   Create new column Price Bucket:
   Excel formular=IF(Discounted Price < 200, "<₹200",
   IF(Discounted Price <= 500, "₹200–₹500", ">₹500")) 
  - i used Pivot Table:

Rows: Price Bucket

Values: Product Name → Count
and i got this
₹200 - ₹500
<₹200
>₹500
  

 11. How does the rating relate to the level of discount

X-axis: Discount %
Y-axis: Average Rating. i used Line Chart
(Grouped by Discount Ranges)
Steps:

  I Created a new column that groups Discount % into buckets like:

  0–10%, 11–20%, ..., 91–100%

  and i used excel formular=IF([@Discount%]<=10%, "0-10%",
  IF([@Discount%]<=20, "11-20%",
  IF([@Discount%]<=30, "21-30%", ...))) to get my values

  =IF([@[discount_percentage]]<=10%,"0-10%",IF([@[discount_percentage]]<=20%,"11-20%",IF([@[discount_percentage]]<=30%,"21-30%",IF([@[discount_percentage]]<=40%,"31-40%",IF([@[discount_percentage]]<=50%,"41-50%",IF([@[discount_percentage]]<=60%,"51-60%",IF([@[discount_percentage]]<=70%,"61-70%",IF([@[discount_percentage]]<=80%,"71-  80%",IF([@[discount_percentage]]<=90%,"81-90%","91-100%")))))))))
    and i click enter to get my value and flash fill to fill in and i used a 
    Pivot Table:

    Rows: Discount Bucket

    Values: Average Rating → summarize as Average

    I Insert a line chart to show trend of average rating across discount buckets

 12. How many products have fewer than 1,000 reviews
    I used Filter to acheive my result Rating Count < 1000
    product with <1000 reviews is = 310


 13. Which categories have products with the highest discounts
     I Use the earlier Discount % column to achieve this, and also 
     Pivot Table:

    Rows: Category

      Values: Discount % → Max
      The product category with the highest discount is Electronics

 14. Top 5 products by rating + number of reviews combined
    Create calculated column:
    =Average Rating + (Rating Count / Scaling Factor)
    (Choose a factor like 1000 to balance weight)
    4.09 + 426,973/1000 = 431.06

Sort descending and pick top 5.
  1.Amazone Basic Wireless mouse 
  2.Sync Wire LTG to USB cable
  3.REDTECH USB-C to lightening cable
  4.Swiffer Instant electric water heater faucet tap
  5.Instant Pot Air fryer

 
  ### Results

[Amazon.case.study.VICTORIA.PROJECT.1 (1).xlsx](https://github.com/user-attachments/files/21040336/Amazon.case.study.VICTORIA.PROJECT.1.1.xlsx)


1. Based on the analysis of Amazon product  review, "Homes Improvement is the product that has  the highest average discount of 123.16%, followed by computer accessories 114.01% making them a great category for volume -based promotions. However, the product wit the lowest average discount is Toys and games with 0.00% discunt
  
2.Electronics has the highest product in the category 490 followed by Homes and  kitchen 448, the list products in the categories are Toys and Games, cars and motorbikes, health and personal care 1.

3.Electronics has the highest number of reviews by categories 14,208,406, followed by computers and accessories 6,335,177 making them the top rated and customers favourite. while cars and Motors have the list reviews 1118, making them the list customers favourite.

4. The product with the highest average rating is Electronics with 1998.1 ratings  followed by home and kitchen with 1806.2 while the product with least average rating is cars and motobikes that rated 3.8

5. The average actual price for electronic is higher followed by the average actual price for Home and Kitchen, while the average discounted price for Electronics is highest follwed by the average discounted price for Cars and Motor bikes, this is to say that the average discounted price of Cars and Motorbikes is more higher followed by that of Home and Kitchen.

6. Electronic has the highest number of reviews owing to the fact that it is the highest product in the category.

7. 662 products has a discount of 50% or More

8. The distribution of Product Ratings shows that product that is rated
   4.1 appears to be reviewed 225 times
   4.3 appeares to be reviewed 209 times
   4.2 appeares to be reviewed 207 times
    4  appeares to be reviewed 159 times
   4.4 appeares to be reviewed 114 times
   3.9 appeares to be reviewed 114 times

9. Electronics has the highest potential revenue of 5,104,861  followed by Homes and Kitchen with 1,864,609, hence the need for for chanelling more resources in its promotion. 


10.the number of unique product by price range bucket
 Prices >500 has 850 products
 prices <200 has 159
 prices 200-500 has 342


11. Product that are rated high, most times have high discount, except for cars and motorbikes with high discount but low rating.

12. 310 product has fewer reviews <1000

13. Electronics

14. Top 5 products in terms of rating and number of reviews

   a. Syncwire LTG to USB cable
   b. Instant Airfryer
   c.Amazone basic Wireless Mouse
   d. Office Product
   e.Musical Instrument

   
### Limitation

1.Lack of Unique Identifiers: Product names were not fully visible, which may cause grouping issues in pivot table.
2.No Date/Time Stamp: Cannot analyze seasonal or time-based trends without  a time stamp column.

## Recommendation

1. Promote Top-Rated products More Agressively: use them in marketing campeign and home page recommendations.
2. Incorperate more customers feedback and reviews: More reviews can make new customers trust the product.
3. Optimize Discount range for better conversion.

## Conclusion

This analysis provides valuable insight into product pricing, discount patterns, customer engagement, and category performance. the data reveals that
1. Electronics stands out as the most discounted and widely listed category, offering more opportunity for volume-driven promotions.
2. products with higher ratings should be leveraged as marketing assets to boost customers trust and conversion
3. customers engagement through reviews remains critical and should be encouraged across all categories.
