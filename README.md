[Palmoria Group emp-data (2).csv](https://github.com/user-attachments/files/21036053/Palmoria.Group.emp-data.2.csv)# My Project
## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools used](#tools-used)
- [Data Cleaning Preparation](#data-cleaning-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [My Analysis](#my-analysis)
- [Results](#results)
- [Conclusion](#conclusion)
- [Palmora Case Study Three](#palmora-case-study-three)
- [Data Cleanng Preparation Two](#data-cleaning-preparation-two)
- [Exploratory Data Analysis Two](#exploratory-data-analysis-two)
- [My Data Analysis Two](#my-data-analysis-two)
- [Results two](#results-two)
- [Recommendation](#recommendation)
- [Conclusion](#conclusion)


# DSA-Data Analysis Capstone Project

### This is how i started my portfolio building while taking my Data Analysis class with the incubator hub

### At the incubators hub, i had the opportunity of learning a number of things ranging from Ms Excel to SQl to my portfolio building to my power Bi and now to my project.

 ## PROJECT TOPICS - Case study 1 Amazon Product Review Analysis, and Case study 3 Palmora Group HR Analysis
 ##  Project Overview
 ### the Data Analysis project on Amazone aims to generate insight into the product pricing, discounts, ratings and customer review using Excel Pivot Tables, marketing strategies. And the Palmora Group HR Analysis aims to generate insight on issues bothering on gender ineqaulity and pay gap in its three regions. By analysing the various parameters in the data received we seek to gather enough insight to make reasonable decisions which then enables us to tell compelling stories around our data from the insight gotten and to know the best performance from our data, and offer recommendation based on outcome of the analysis.
 
### Data Sources
The primary sources of Data used here is Data Amazon case study.xlsx file and Data Palmora group emp-data.csv file this is downloaded from my dashboard on Canvas LMS

### Tools used
- Ms Excel for Data Cleaning  [Download Here](https://www.microsoft.com)
    - For Data Collection
    - For Data Cleaning
       1. Data Manipulation
         
- Power Bi [Download]([For creating a report](https://www.microsoft.com/en-us/download/details.aspx?id=58494))
  
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




[Amazon.case.study.VICTORIA.PROJECT.1 (1).xlsx](https://github.com/user-attachments/files/21013585/Amazon.case.study.VICTORIA.PROJECT.1.1.xlsx)

Based on the analysis of Amazon product  review analysis, Electronics have the highest average discount and the largest product count, making them a great category for volume -based promotions


### Limitation

1.Lack of Unique Identifiers: Product names were not fully visible, which may cause grouping issues in pivot table.
2.No Date/Time Stamp: Cannot analyze seasonal or time-based trends without  a time stamp column.

##  CASE Study 3, Palmora Group HR Analysis

### Data Cleaning Preparation 2
At the initial phase of the data cleaning and preparation, we perform the following action.
1. Data Loading and inspection
2. Handling Missing Variables
3. Data Cleaning and formating
 Steps followed to clean Palmora Group HR data are:
the data was loaded into the power bi, where it was transformed to the power query editor for cleaning.
At first, i assigned a generic name NOT DISCLOSED that means to replace values, and i also went on to take out rows where employee has no salary. I also took out rows where department indicated NULL. I renamed the column for Location and changed it to Region, and i added a custom coulmn where i got the department_rating. I aslo loaded the bonus table and transformed it to get my bonus mapping and then i went on to select all the bonus and unpivote it and added a custom column to give me the department rating so
it can be easy for me to merge the palmora data with the bonus data into a new merged data, to continue with the addition of columns, i expanded the bonus mapping to reveal the values and and added a custom column to get the Annual bonus, thereafter i rename the column to change it to Bonus rate and i also added another custom  column called the total salary and i added conditional column to get the salary band. i also assigned value 0 to columns that were blank. After that, i proceeded to my analysis.

### Exploratory Data Analysis

1.	What is the gender distribution in the organization? Distil to regions and departments 
2.	Show insights on ratings based on gender 
3.	Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management 
4.	A recent regulation was adopted which requires manufacturing companies to pay employees a minimum of $90,000 
●	Does Palmoria meet this requirement? 
●	Show the pay distribution of employees grouped by a band of $10,000. For example: 
●	How many employees fall into a band of $10,000 – $20,000, $20,000 – $30,000, etc.? 
●	Also visualize this by regions 
  
Case Questions 
5. Mr Gamma thought to himself that since you were already working on the employee data, you could help out with allocating the annual bonus pay to employees based on the performance rating. He handed you another data set that contains rules for making bonus payments and asked you to: 
●	Calculate the amount to be paid as a bonus to individual employees 
●	Calculate the total amount to be paid to individual employees (salary inclusive of bonus) 
●	Total amount to be paid out per region and company-wide 
  
  
 
My Analysis Two

I Import the employee data into Power BI and 
did a proper cleaning by

1. Assign a generic gender status to employees who refused to disclose their gender.
2. Remove employees without salaries and departments indicate as "NULL".

first of all i got the employee count using cards on the visual and then
i went on to get the total salary by copying and pasting the employee and and
summerizing by count and then i got the average salary Max salary and Min salary using the same approach.

1. For Gender Distribution Analysis
1. I used a bar chart:
    - Axis: Region/Department
    - Value: Count of Employees by Gender
2.And then i Used a slicer to filter by region/department.
3.  I Visualize the overall gender distribution using a pie chart.

Visualization: 
- Bar chart: "Gender Distribution by Region"
- Pie chart: "Overall Gender Distribution"

Measures
- `Gender Count = COUNT('Employee'[Gender])`
-  Gender Percentage = DIVIDE(CALCULATE(COUNT('Employee'[Gender])), CALCULATE(COUNT('Employee'[Gender]), ALL('Employee'[Gender])))`
 2: Ratings Insights Based on Gender
1. I Created a histogram and a matrix box plot:
    - Axis: Rating
    - Value: Count of Employees by Gender
   2. And i used slicer to filter by Gender
   3.I Calculated the average rating by gender using a measure.

Visualization:
- Histogram: "Ratings Distribution by Gender"
- Box plot: "Ratings Comparison by Gender"

Measures
- Average Rating by Gender = AVERAGE('Employee'[Rating])`
- Rating Count by Gender = COUNT('Employee'[Rating])`
 3: Salary Structure and Gender Pay Gap Analysis
1. Create a scatter plot:
    - X-axis: Salary
    - Y-axis: Gender
2. Calculate the average salary by gender using a measure.
3. Identify departments and regions with significant pay gaps.

Visualization:
- Scatter plot: "Salary vs. Gender"
- Bar chart: "Average Salary by Department and Region"

Measures 
- `Average Salary by Gender = AVERAGE('Employee'[Salary])`
- `Salary Count by Department and Region = COUNT('Employee'[Salary])`
 4: Minimum Salary Requirement Analysis
1. Create a histogram:
    - Axis: Salary Band ($10,000 increments)
    - Value: Count of Employees
2. Use a slicer to filter by region.
3. Calculate the number of employees below the minimum salary threshold.

Visualization:
- Histogram: "Salary Distribution by $10,000 Band"
- Bar chart: "Employees Below Minimum Salary Threshold by Region"

Measures
- `Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])`
-  5: Bonus Payment Calculation
1. Create a measure to calculate the bonus amount based on performance ratings.
2. Calculate the total amount to be paid to individual employees (salary + bonus).
3. Create a bar chart to visualize the total amount to be paid out per region.

Visualization:
Bonus Payments
- Bar chart: "Total Bonus Payout by Region"
- Table: "Individual Employee Bonus Payments"

Measures
- `Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)`
- `Total Amount to be Paid = 'Employee'[Salary] + 'Bonus Amount'`

  ## Results two
  SNAP SHOTS OF POWER BI PROJECT
![Project Case 3_1](https://github.com/user-attachments/assets/60fa9909-cbd0-42a4-8a58-73080f28552f)
![Project Case 3_2](https://github.com/user-attachments/assets/d094a43d-6966-43ce-b2e0-f344ef18b0d1)
![Project Case 3_3](https://github.com/user-attachments/assets/481cae84-2b2d-43eb-9a17-d36c5d35eb9b)
![Project Case 3_4](https://github.com/user-attachments/assets/b33ea4a5-195c-475d-a2d5-576d9da10a27)






