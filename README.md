Excel Salary Dashboard
![1_Salary_Dashboard_Final_Dashboard (1)](https://github.com/user-attachments/assets/52e132b8-c229-4530-ad4f-9637b0190890)


Introduction
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

Dashboard File
My final dashboard is in 1_Salary_Dashboard.xlsx.

Excel Skills Used
The following Excel skills were utilized for analysis:

 Charts
 Formulas and Functions
 Data Validation
 Data Jobs Dataset
 The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

 Job titles
 Salaries
 Locations
 Skills
Dashboard Build
 Charts
 Data Science Job Salaries - Bar Chart
![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/a93febee-e09d-4ddc-837a-db088a8a68c2)

 Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
 Design Choice: Horizontal bar chart for visual comparison of median salaries.
 Data Organization: Sorted job titles by descending salary for improved readability.
 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
 Country Median Salaries - Map Chart
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/6ff002d7-a057-4381-b386-eaef0394a82c)


 Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
 Design Choice: Color-coded map to visually differentiate salary levels across regions.
 Data Representation: Plotted median salary for each country with available data.
 Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.
 Formulas and Functions
 Median Salary by Job Titles
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.
 Background Table


![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/6d4e1e32-8e1e-49a1-95b8-ec3e69e9669c)

 Dashboard Implementation

![1_Salary_Dashboard_Job_Title](https://github.com/user-attachments/assets/c3df8fb4-90ab-4d6c-b6bf-16d507a0f5cc)

 Count of Job Schedule Type
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.
 Background Table

![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/83352428-9dea-4523-994e-08d98b362453)

 Dashboard Implementation:

![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/888125bd-fde8-4121-a87f-8fd4a6328b83)

 Data Validation
 Filtered List
 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
 User input is restricted to predefined, validated schedule types
 Incorrect or inconsistent entries are prevented
 Overall usability of the dashboard is enhanced
![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/8c00c6f5-425e-45a6-bdeb-61b114897694)


Conclusion
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
