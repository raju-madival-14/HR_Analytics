👥 HR Analytics Dashboard

📌 Project Overview

This project is an HR Analytics Dashboard built using Power BI to analyze workforce metrics such as employee attrition, hiring trends, salary distribution, and workforce demographics.
It helps HR teams and stakeholders make data-driven decisions by providing insights into employee performance, retention, and growth patterns.

📊 Dashboard Preview

https://app.powerbi.com/links/LcbbI7HKhL?ctid=180e4901-edf9-47a0-9756-059be2fb1cc1&pbi_source=linkShare 

⚙️ Tools & Techniques Used

Power BI Desktop

Data Modeling (Star Schema)

DAX (Data Analysis Expressions) for custom KPIs

Power Query for data cleaning and transformation

Interactive Filters & Slicers

Custom visuals for HR-specific analytics

🔑 Key Metrics

1.Employee Headcount – Total active employees at any given time.

    Total Employees = COUNT(Employee_details[Employee_ID])
    Active Employees = CALCULATE([Total Employees],Employee_status[Status]="active")

2.Attrition Rate – Percentage of employees leaving the organization.

    Attrition Count = [Total Employees]-[Active Employees] 
    Attrition % = DIVIDE([Attrition Count],[Total Employees],0)

3.Employee Growth % – Month-over-month workforce expansion or decline.

    Employee growth = [Active Employees]-[PY Hires]
    Employee growth % = DIVIDE([PY Hires],[Employee growth],0)

4.Diversity Ratio – Gender diversity.

    Female Employees = CALCULATE([Total Employees],Employee_details[Gender]="female")

    Female % = DIVIDE([Female Employees],[Total Employees],0)
   
5.Average Salary -- Total active employees at any given time.

    Average Salary = AVERAGE(Salary[Total_Salary])

6.LY Hires and PY Hires
    
    LY Hires = TOTALYTD(
          CALCULATE(
              COUNT(Recruitment[Hiring_Decision]),Recruitment[Hiring_Decision]="hired"),Recruitment[Application_Date].[Date])
    PY Hires = TOTALYTD(
          CALCULATE(
              COUNT(Recruitment[Hiring_Decision]),Recruitment[Hiring_Decision]="hired"),SAMEPERIODLASTYEAR(Recruitment[Application_Date].[Date]))        
        

💡 Key Insights

The Attrition Rate was highest in the Sales and Customer Support departments, indicating a need for improved retention strategies.

 Hiring Rate grew by 15% over the last quarter, showing strong workforce expansion.

Gender diversity improved by 10% YoY, with technology teams showing the highest improvement.

Average employee tenure dropped in the Operations team, suggesting possible employee dissatisfaction.

Top-performing employees consistently achieved 90% or more of their KPIs, while a small segment requires additional training and support.

Attrition Trend: A major drop in employee count occurred in 2025, indicating mass layoffs or restructuring.

📂 Files Included

HR_Analytics_Dashboard.pbix → Power BI dashboard file.

HR_Dataset.xlsx → Source dataset with multiple HR-related tables.

Screenshot.png → Dashboard preview image.

README.md → Project documentation.

Data_Modeling_Structure.png → Star schema snapshot.

Demo_Video.mp4 → Video showcasing interactive dashboard features.

🎯 Purpose of the Project

To help HR managers and leadership teams monitor employee performance and retention.

Identify workforce diversity gaps and areas for improvement.

Optimize salary distribution and hiring plans.

Provide real-time analytics for informed decision-making.

👨‍💻 Author

A Raja

LinkedIn: linkedin.com/in/a-raja4

Email: rajumadival02@gmail.com

Contact: 8618072982
