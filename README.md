# Excel_Project_Data_Analytics

### Quick Summary

This repository currently includes 2 Excel Projects I made to showcase some of my Data Analytics skills. Files for the finished projects are included, but I will be doing a quick summary of each project here as well. 

## Project 1 - Salary Dashboard

<img width="843" height="415" alt="Dashboard Screenshot" src="https://github.com/user-attachments/assets/100fe331-cf46-4a68-8640-ae4f79842720" />


### Introduction 

The data job salary dashboard was created to help me visualize the general state of the data job market as someone looking to get into the industry. 

The data I found on the data job market was detailed, containing information on things such as job titles, salaries, job posting locations, and job skills required or wanted by employers.

### Dashboard File

My final dashboard file is in [Salary Dashboard](https://github.com/LopezSamir/Excel_Project_Data_Analytics/tree/main/Project_1_Salary_Dashboard)

### Excel Skills Used

* Charts
* Formulas and Functions
* Data Cleaning/Formatting/Validation

### Interactive Aspects

The final dashboard file is currently set up so that all cells are protected except for 3 cells that act as drop down menus. By selecting different job titles, countries, and job-types, the data displayed will change to match those options. For example, the screenshot below is the same dashboard as the one above, but with the country changed from the United States to the United Kingdom

<img width="824" height="404" alt="Dashboard Screenshot UK" src="https://github.com/user-attachments/assets/1f0f0e08-adf0-480f-a37b-6c77c47bb729" />

### Conclusion

I created this project to better understand the data job market while also showcasing my ability to clean data and use it to create charts that model that data. The final file is intended to be as simple and easy to understand as possible. That way I could send it to someone that is not familiar with Excel, or a coworker, and they can still understand how to use the dashboard. 

## Project 2 - Data Skills Analysis

### Introduction

The data skills analysis project was created to me visualize the most important skills I need to learn and improve in order to succeed in landing a data job. At the same time, it was created in order to show some of my skills in more advanced aspects of Excel listed in the skills section below.

The data jobs dataset used in this project is from 2023. It has the same detailed information as the last project, such as job titles and salaries. Using this data, I wanted to answer four questions.

### Questions to Analyze

1. Does having more skills net you a higher salary?
2. What is the salary for data jobs in different regions?
3. What are the top skills of data professionals?
4. What is the pay for the top 10 skills?

### Data Skills Project File

My final file for this project is in [Data Skills Analysis](https://github.com/LopezSamir/Excel_Project_Data_Analytics/tree/main/Project_2_Data_Skills_Analysis)

### Excel Skills Used

* Pivot Tables
* Pivot Charts
* DAX (Data Analysis Expressions)
* Power Query
* Power Pivot

## 1. Does having more skills net you a higher salary?

### Skill - Power Query (ETL)

First I used powerquery to **extract** the original data and created two queries.
* The first one had all the data job information
* The second listed the skills for each job ID

Then I **transformed** each query by changing column types, removing unneeded columns, and other formatting such as removing specific unwanted words.

<img width="187" height="283" alt="Applied steps 1" src="https://github.com/user-attachments/assets/797a1bb1-8989-4e3d-821a-4d5305c9b5da" />

<img width="191" height="357" alt="Applied steps 2" src="https://github.com/user-attachments/assets/d24d7110-b62a-4d3e-996b-5d9bec2b7537" />

After that, I **loaded** both transformed queries into the workbook to begin my analysis.

## Analysis

<img width="451" height="298" alt="Better Pay Graph" src="https://github.com/user-attachments/assets/5d98c20a-3416-463e-a908-16636557abe7" />

### Insights

* There is a positive correlation between the number of skills requested in job postings and the median salary.
* Job roles that require less skills, such as Business Analyst, tend to offer lower salaries, which suggests that having more skills does result in a higher salary.

### Answer

Having more data skills nets you a higher salary.

## 2. What is the salary for data jobs in different regions?

### Skills - PivotTables and DAX
#### Pivot Table
* Created a PivotTable using the Data Model I created with Power Pivot
* Moved the job_title_short to the rows area and salary_year_avg into the values area.
* Added a new measure to calculate the median salary for United States jobs.
  <img width="394" height="334" alt="Measure - Median Salary US" src="https://github.com/user-attachments/assets/217cb42d-60ec-4cc8-b59e-ba244a30f757" />

#### DAX 
* Used DAX to calculate the median yearly salary
    * Median Salary := MEDIAN(data_jobs_all[salary_year_avg])

## Analysis

<img width="584" height="241" alt="Median Salaries Table" src="https://github.com/user-attachments/assets/654589ab-ca18-412d-996f-c16f6c2e213e" />

### Insights

* Higher level job roles like Senior Data Engineer and Data Scientist have higher median salaries both in the United States and internationally, showing the global demand for high level data experts.
* The United States tends to have higher salaries than other countries, most likely due to the higher demand for these roles in the United States than internationally.

### Answer

The median salary for international data jobs is less than the median salary for United States data jobs. The median salary for specific countries can be checked by opening up my project file and changing the country currently being displayed.





