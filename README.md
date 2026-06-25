HR Attrition Analytics Dashboard

Tool: Power BI | Dataset: IBM HR Analytics (Kaggle) | Records: 1,470 Employees

About This Project

I built this dashboard to explore a question that most HR teams deal with but rarely analyze properly why do employees leave, and who is most likely to leave next?

The IBM HR Analytics dataset gave me a solid base to work with: 1,470 employee records across 35 attributes including job role, department, income, satisfaction scores, and whether the employee eventually left the company. I used Power BI to clean, model, and visualize this data into an interactive dashboard that an HR manager could actually sit down and use.

The dashboard is built around five core questions:

1. What is the overall attrition rate, and how many employees are currently active?
2. Which departments and job roles are losing the most people?
3. Does age, gender, or education field affect the likelihood of leaving?
4. How much does job satisfaction and work-life balance influence attrition?
5. Is there a relationship between monthly income and attrition?

To answer these, I created KPI cards for headline numbers (total employees, total attrition, attrition rate), bar and donut charts for department and role breakdowns, a satisfaction matrix to cross-reference ratings with attrition counts, and slicers to let the user filter by department, gender, age group, and education field.


Key Findings

- The overall attrition rate sits at 16.1% — 237 employees out of 1,470
- Sales had the highest attrition rate proportionally; R&D had the highest in absolute numbers
- Sales Executives and Laboratory Technicians were the most affected job roles
- Employees aged 26–35 left at the highest rate early career restlessness is real
- Employees with low job satisfaction (rating 1) showed nearly double the attrition of those rated 4
- Lower monthly income combined with poor work-life balance was the strongest predictor of turnover

DAX Measures Used


Total Employees = COUNT(HR_Analytics[EmployeeNumber])

Total Attrition = COUNTROWS(FILTER(HR_Analytics, HR_Analytics[Attrition] = "Yes"))

Attrition Rate = DIVIDE([Total Attrition], [Total Employees], 0)

Active Employees = [Total Employees] - [Total Attrition]

 Tools Used

- Power BI Desktop (data modeling, DAX, visualization)
- Power Query (data cleaning and transformation)
- IBM HR Analytics Dataset — sourced from Kaggle

 Files in This Repository


HR-Attrition-Analytics-Dashboard/
├── HR_Attrition_Dashboard.pbix     Power BI project file
├── HR_Analytics.csv                Source dataset
├── Dashboard_Screenshot.png        Dashboard preview
└── README.md                       Project documentation

 How to Open

1. Download the repository
2. Open `HR_Attrition_Dashboard.pbix` in Power BI Desktop
3. If the data doesn't load, go to Transform Data > Data Source Settings and point it to `HR_Analytics.csv`
4. Use the slicers on the dashboard to filter by department, gender, age, or education

About Me

Muhammad Shahzaib — Biotechnology graduate with a focus on data analytics. I'm building this portfolio while preparing for postgraduate opportunities, using real datasets to develop practical skills in Excel, Power BI, and MySQL.
