# Google Data Analytics Capstone: Analyzing Company Data to Provide Actionable Marketing Strategy
My capstone project for the Google Data Analytics Professional Certificate, a Cyclistic bike share case study.
 
  By: Ajoku, Chilotam
  
  Last Updated: 1st of January, 2025 (update ongoing)

  ## Introduction
As part of the [Google Data Analytics Professional Certification](https://www.coursera.org/professional-certificates/google-data-analytics), I completed the capstone case study. In this case study, I was given a real-world data analysis scenario for the fictional bike sharing company. This study presented a practical data analysis situation involving the fictional bike-sharing company, Cyclistic. Assuming the role of a junior data analyst on the Cyclistic marketing team, my responsibility was to examine historical data from the company to address a specific business question. I adhered to Google's data analysis framework, which includes the steps of 'ask, prepare, process, analyze, share, and act' to conduct my analysis.
  ## Background
In 2016, Cyclistic introduced a highly successful bike-sharing program. Since its launch, the program has expanded to include 5,824 GPS-enabled bicycles, available at 692 stations across Chicago. Riders have the flexibility to unlock bikes from one station and return them to any other station within the network at any time.

Cyclistic's marketing strategy thus far has focused on raising general awareness and catering to diverse customer groups. A key factor contributing to the program's success has been its flexible pricing options: single-ride passes, full-day passes, and annual memberships. Customers using single-ride or full-day passes are categorized as casual riders, while those opting for annual memberships are considered Cyclistic members.

The marketing director of the company is convinced that the future success of Cyclistic relies on increasing the number of annual memberships. As a result, as junior data analysts, I have been assigned to analyze the differences in how casual riders and annual members utilize Cyclistic bikes. These insights will inform the development of a new marketing strategy aimed at converting casual riders into annual members.
  
  ## Approach/Steps
  ### 1. Ask Phase

**Business Task** - Design marketing strategies aimed at converting casual riders into annual members. In this project, I will answer the business question, “how do annual members and casual riders use Cyclistic bikes differently?” I will prepare, clean, and analyze historical trip data from the January to December 2022 to understand how annual members and casual riders use Cyclistic bike-share services.

### 2. Prepare phase
**Data Source:** [divvy-tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html)
 [_Note: This dataset has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement)_]

**Tools:**
  - Data cleaning & processing- SQL Server and Excel
  - Data visualization- Power BI

### 3. Process phase (Download all 12 months and export to excel, ckecked for duplicates or mistake, created column for days of the week and ride length)
The basis for this analysis is 2022 data and the steps for processing the data are as follow:

1. Data Combining
  
2. Data Exploration

3. Data Cleaning
   
5. Data Analysis
   

Data Combining: The 12 tables from January 2022 to December 2022 were stacked and combined into a single table called "Full_year_dataset". The table consists of 5,722,001 rows.
   
```sql
SELECT * 
INTO FULL_YEAR_DATASET
FROM (
    SELECT * FROM [dbo].[January_dataset]
    UNION ALL
    SELECT * FROM [dbo].[February_dataset]
    UNION ALL
    SELECT * FROM [dbo].[March_dataset]
    UNION ALL
    SELECT * FROM [dbo].[April_dataset]
    UNION ALL
    SELECT * FROM [dbo].[May_dataset]
    UNION ALL
    SELECT * FROM [dbo].[June dataset]
    UNION ALL
    SELECT * FROM [dbo].[July_dataset]
    UNION ALL
    SELECT * FROM [dbo].[August_dataset]
    UNION ALL
    SELECT * FROM [dbo].[September_dataset]
    UNION ALL
    SELECT * FROM [dbo].[October_dataset]
    UNION ALL
    SELECT * FROM [dbo].[November_dataset]
    UNION ALL
    SELECT * FROM [dbo].[December_dataset]
);
```
The data type for the variables are

<img width="438" alt="Data_type" src="https://github.com/user-attachments/assets/f80e4247-c6f0-403d-9cb2-44662adcd235" />


### 5. Analyze phase (SQL queries, I merged all 12 months, cleaned the data, created column for month)
6. Share phase (PowerBi) then also answer the question regarding similarities and differences between casual riders and annual members.
7. Act phase (Reccomendation)
