
## Project 2 - Data Skills Analysis

### Introduction

The data skills analysis project was created to me visualize the most important skills I need to learn and improve in order to succeed in landing a data job. At the same time, it was created in order to show some of my skills in more advanced aspects of Excel listed in the skills section below.

The data jobs dataset used in this project has the same detailed information as the last project, such as job titles and salaries. Using this data, I wanted to answer four questions.

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

## 3. What are the top skills of data professionals?

### Skill - Power Pivot
#### Power Pivot

* I created a data model by integrating the data_jobs_all and data_jobs_skills tables into one model.
* Since I had already cleaned the data using Power Query, Power Pivot created a relationship between the two tables

#### Data Model

* Created a relationship between the two tables using the job_id column.
  <img width="606" height="467" alt="Data model relationship 1" src="https://github.com/user-attachments/assets/90043558-62c7-4084-a002-5200f6893852" />

#### Power Pivot Menu
* Used the Power Pivot menu to refine my data model so that is would be easier to create measures
  <img width="670" height="260" alt="powerpivot refined menu" src="https://github.com/user-attachments/assets/b3c9bcd5-78b2-40ba-a900-2245c086f13c" />

## Analysis

<img width="1000" height="1000" alt="skill likelihood chart" src="https://github.com/user-attachments/assets/c6bdc4ab-782f-468b-b43c-7eee9c388368" />

### Insights

* SQL and Excel, followed by Python, are the top skills for data jobs. The likelihood of a job role requiring these skills is much higher than the other skills in the top 10.
* Other important skills incude Tableau and Power BI, which are commonly used for data modeling

### Answer

The top skills of data professionals changes depending on which job title and country we are looking at. Some standouts include SQL, Excel, Tableau, and Power BI. My project file allows viewers to change the job title and country that they are being shown so they can further understand what skills are needed for which job in their country.

## 4. What is the pay for the top 10 skills?

### Skill - Advanced Charts (Pivot Chart)
#### PivotChart
* Created combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.
    * Primary Axis: Median Salary (as a Clustered Column)
    * Secondary Axis: SKill Likelihood (as a Line with Markers)
* To customize the chart, I added a title axis title, removed the line of skil likelihood, and changed the markers to diamonds

## Analysis

<img width="514" height="264" alt="Skill likelihood graph" src="https://github.com/user-attachments/assets/4548413a-7ddd-41af-a952-5b393fe494f3" />

### Insights

* Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.
* Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicating less specialization and demand in high-salary sectors.

### Answer

The pay for the top 10 skills is shown in the combo PivotChart in the project file. Skills like Python and Oracle tend to pay more than less advanced skills like Word and PowerPoint

### Conclusion

As someone looking to become an analyst (Data/Business/etc.) I created this project in order to identify the top 10 skills required for these roles. Using a dataset from real-world job postings, I analyzed the salaries, locations, and required skills. This was done with the use of more advanced Excel features like Power Query, Power Pivot, Pivot Tables/Charts, and DAX. Finally, I am able to conclude that people with a larger skill set tend to be paid higher salaries than those with smaller skill sets.

This project serves both as a way for me to showcase and practice my skills while also informing me of what I need to focus on moving forward.

