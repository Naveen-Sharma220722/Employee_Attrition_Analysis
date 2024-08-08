# Employee_Attrition_Analysis

##  Project Overview

The project objective is to uncover the factors that lead to employee attrition within an organisation. A dashboard is prepared in MS-Excel for this purpose. This dashboard helps HR professionals and management understand the trends and make data-driven decisions to improve employee retention.

## Dataset used

The dataset used in this project is taken from the Kaggle website.<br>Link-
<a href="https://www.kaggle.com/datasets/whenamancodes/hr-employee-attrition">Employee Attrition Dataset</a>

## Steps

1. **Data Importing and Cleaning**: The data was imported into Excel Power Query where unwanted columns were removed and some columns were transformed for proper analysis of data. All columns were checked whether they had proper data type or not. It was also ensured that all columns did not contain any undefined, duplicate or Null values.<br>

2. **Data Processing**:  As per requirement, Some new columns were also created using existing columns by using "Conditional Column" and "Custom Column" features in Power Query.<br>
   a) From "Age" column, a new column "Age Group" was created where age was categorized into four different groups as 18-30, 31-40, 41-50, and 51-60.<br>
   b) In the same way, Work Distance from Home was categorized as Near-by, Far, and Very Far.<br>
   c) Monthly Income was categorized as Less than 5k, 5k-10k, 10k-15k, and 15k-20k.<br>
   d) A column "Education" was there in which levels were given as 1,2,3,4; so a new column "Education Status" was created showing education degree corresponding to given level which was already given in dataset.<br>
   e) Similarly Performance levels, Job Satisfaction levels, work Life Balance levels were given from which new columns were created showing meaning of the corresponding level.<br>
   
3. **Data Analysis**: Now the data was ready for analysis, so various pivot tables and pivot charts were created to visualize attrition by education level, age group, gender, department, job role, monthly income and other factors. Slicers for gender and department were also created to enable users to interact with the dashboard and view specific subsets of data.<br>

4. **Interactive Dashboard**: All the charts and both the slicers were formatted as per theme decided for the dashboard. Finally after formatting of Shapes, Icons, Text boxes, Charts, and Slicers, the interactive dashboard showing employee attrition trends was ready. After that meaningful insights were drawn which are discussed below.<br> (While finalising the dashboard, one problem was there i.e. when a filter was applied and some fields had 0 value for it, then on dashboard that field with 0 value was not appearing. This is because after applying filters the fields with 0 value disappear from pivot table as well and pivot table shrinks. And there were some formulas which use relative referencing with pivot table cells, so these formulas also become incorrect when pivot table shrinks. So, for this I took help of youtube videos and found that it can be corrected by going to Pivot table field settings and turning ON the option "Show items with no data". But this option was greyed out, so instead I have to create a measure in pivot table so that if Employee count is blank show 0.)<br>

## Dashboard 

<img width="920" alt="Excel Project1 img" src="https://github.com/user-attachments/assets/ff1b134f-51f8-495d-a4ad-61462076c310"><br><br>

## Insights

Employee Count = 1470<br>
Attrition Count = 237<br>
Attrition Rate = 16%<br>
- Attrition by **Monthly Income**<br>
Employees with Monthly Income Less than 5k left the organisation most (163)<br>
- Attrition by **Job Role**<br>
Highest = Laboratory Technicians = 62 (59 with Less than 5k income)<br>
Second highest = Sales Executives = 57 (10 with Less than 5k income)<br>
Third highest = Research Scientists = 47 (All had Less than 5k income)<br>
Fourth highest = Sales Representatives = 33 (All had Less than 5k income)<br>
- Attrition by **Age group**<br>
Age group 18-30 with highest number of attrition (100)<br>
Age group 31-40 has second highest attrition (85)<br>
- Attrition by **Gender**<br>
Male has the highest attrition of 150 (63%)<br>
- Attrition by **Education level**<br>
Bachelor degree holders has the highest attrition of 99.<br>
- Attrition by **Performance Status**<br>
Employees with Excellent performance left the most (200)<br>
- Attrition by **Work Distance**<br>
Employees living Near-by to the office left the most (133)<br>
- Attrition by **Business Travel**<br>
Employees who travel rarely, left the most (156)
- Attrition by **Department**<br>
Employees belonging to Research & Development (R&D) department has the highest attrition of 133.<br>

## Recommendations

There is high attrition rate among the four job roles i.e. Laboratory Technicians, Sales Executives, Research Scientists, and Sales Representatives (199). Out of 199, 149 had monthly income Less than 5k and 39 had monthly income between 5k-10k. So, if organisation wants to retain the employees in future, it has to increase the monthly income of employees specially belonging to above four job roles.  
