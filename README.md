# Employee_Attrition_Analysis

##  Project Objective

To identify the factors contributing to employee attrition within an organization and develop a dashboard in MS-Excel to assist HR and management in making data-driven decisions.

## Dataset used

The dataset used in this project is taken from the Kaggle website.<br>Link-
<a href="https://www.kaggle.com/datasets/whenamancodes/hr-employee-attrition">Employee Attrition Dataset</a>

## Steps

1. **Data Importing and Cleaning**:
   * Imported data into Excel Power Query.
   * Cleaned data by removing unwanted columns, transforming data types, and handling undefined, duplicate, or null values.<br>

2. **Data Processing**: Created new columns using existing data to enhance analysis by using "Conditional Column" and "Custom Column" features in Power Query.<br>
   * **Age Group**: Categorized into 18-30, 31-40, 41-50, and 51-60.<br>
   * **Work Distance**: Categorized as Near-by, Far, and Very Far.<br>
   * **Monthly Income**: Grouped into Less than 5k, 5k-10k, 10k-15k, and 15k-20k.<br>
   * **Education Status**: Translated numeric levels into degree names as per given dataset.<br>
   * **Performance, Job Satisfaction, Work-Life Balance**: Converted numeric levels into descriptive labels as per given dataset.<br>
   
3. **Data Analysis**:
   * Created pivot tables and pivot charts to visualize attrition by education level, age group, gender, department, job role, monthly income and other factors.<br>
   * Slicers for gender and department were also created to enable users to interact with the dashboard and view specific subsets of data.<br>

5. **Interactive Dashboard**:
   * Designed and formatted the dashboard with charts, shapes, icons, text boxes, and slicers. <br>
   * While finalizing the dashboard, one problem was there i.e. when a filter was applied and some fields had 0 value for it, then on dashboard that field with 0 value was not appearing. This is because after applying filters the fields with 0 value disappear from pivot table as well and pivot table shrinks. And there were some formulas which use relative referencing with pivot table cells, so these formulas also become incorrect when pivot table shrinks. So, for this I took help of YouTube videos and found that it can be corrected by going to Pivot table field settings and turning ON the option "Show items with no data". But this option was greyed out, so instead I have to create a measure in pivot table so that if Employee count is blank show 0.<br>

## Dashboard 

<img width="920" alt="Employee Attrition Analysis Dashboard" src="https://github.com/user-attachments/assets/b0148537-3467-4419-b572-cbcc8accf6d4"><br><br>

![Employee Attrition GIF](https://github.com/user-attachments/assets/ad831f06-a949-40a7-86ef-d84c71cf4769)

## Insights

1. **Overall Attrition:**
* Employee Count = 1470<br>
* Attrition Count = 237<br>
* Attrition Rate = 16%<br>
2. **Attrition Analysis by Category:** <br>
- **Monthly Income**<br>
Highest attrition among employees earning less than 5k monthly.(163)<br>
- **Job Role**<br>
Laboratory Technicians have the highest attrition = 62 (59 with Less than 5k income)<br>
Followed by Sales Executives = 57 (10 with Less than 5k income)<br>
Followed by Research Scientists = 47 (All had Less than 5k income)<br>
Followed by Sales Representatives = 33 (All had Less than 5k income)<br>
- **Age group**<br>
Age group 18-30 with highest number of attrition (100)<br>
Age group 31-40 has second highest attrition (85)<br>
- **Gender**<br>
Higher attrition rate among males = 150 (63%)<br>
- **Education level**<br>
Bachelor’s degree holders experience the highest attrition (99).<br>
- **Performance Status**<br>
Employees with Excellent performance have the highest attrition (200)<br>
- **Work Distance**<br>
Employees living Near-by the office have highest attrition (133)<br>
- **Business Travel**<br>
Employees who travel rarely show the highest attrition (156)
- **Department**<br>
Research & Development (R&D) department has the highest attrition (133).<br>
3. **Conclusion** <br>
* High attrition rates are observed among Laboratory Technicians, Sales Executives, Research Scientists, and Sales Representatives (199). Out of 199, 149 had monthly income Less than 5k and 39 had monthly income between 5k-10k. Increasing the monthly income for these roles could potentially reduce attrition.<br>
* Consider conducting exit interviews or surveys with employees in high attrition roles to understand their specific reasons for leaving.<br>
* Developing a compensation strategy that addresses the low-income issue for roles with high attrition.<br>
* Analyzing if younger employees (18-30) have different needs or expectations compared to older age groups and tailor retention strategies accordingly.
