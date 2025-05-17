# Employee-Survey-Dataset

This project analyzes Employee Survey Responses that are actual responses from an employee engagement survey conducted by Pierce County WA and completed voluntarily by government employees. The dataset is a Single table and contains 14,725 records. The total number of fields is 10.
---

## Table of Contents
1. [Overview](#overview)
2. [Raw Data](#raw-data)
3. [Dashboard & Dashboard Features](#dashboard-features)
4. [Data Cleaning Process](Data--cleaning--process&preprocessing)
5. [Key Metrics](#key-metrics)
6. [Insights & Conclusions](#insights--conclusions)
7. [Tools & Techniques Used](#tools--techniques-used)
8. [Questions & Answers](#questions--answers)
9. [Recommendation](#Recommendation)
10. [Conclusion](#Conclusion)
11. [Author](#author)

---

## Overview
The Employee Performance Dashboard visualizes insights from a county-wide engagement survey of over 14,000 government employees, highlighting trends in satisfaction, growth, and workplace culture by role and department. It enables quick identification of strengths and improvement areas to support data-driven HR decisions.

---

## Raw Data
The raw data for this dashboard includes a comprehensive dataset of employee details from a fictional company. It consists of the following fields:

1. **Response ID**: Unique, sequential ID representing a response to a survey question.
2. **Status**: Identifies whether a response was complete or incomplete.
3. **Department**: Survey respondent's job department (Human Resources, Public Works, etc.).
4. **Director **: Binary (0/1) field indicating if the respondent is in a Director role.
5. **Manager**: Binary (0/1) field indicating if the respondent is in a Manager role.
6. **Supervisor**: Binary (0/1) field indicating if the respondent is in a Supervisor role.
7. **Staff**: Binary (0/1) field indicating if the respondent is in a Staff role.
8. **Question**: Full survey question text.
9. **Response**: Survey response value (0, 1, 2, 3, 4).
10. **Response Text**: Survey response text (Not Applicable, Strongly Disagree, Disagree, Agree, Strongly Agree).

---

### Data Cleaning Process in Power Query
- **Column Renaming for Clarity**: Long and complex survey questions were shortened for readability and better visualization in the dashboard (e.g., “1. I know what is expected of me at work” was renamed to “Job Expectation Clarity”).
- **Data Type Formatting**: Ensured columns like Employee ID, Department, Role, and survey responses were in appropriate data types (text, categorical, etc.) to support filtering and calculations.
- **Duplicate Removal**: Checked and removed any duplicate rows to ensure each employee's response was only counted once.
- **Handling Missing Values**: Addressed missing survey responses (e.g., using “Not Applicable” or excluding them from certain calculations depending on context).
- **Category Grouping**: Grouped departments into 10 broad categories for better aggregation and analysis.
- **Role Filtering**: Filtered and calculated the total and percentage of staff, managers, directors, and supervisors for comparative insights.

---

## Dashboard Features
- **Interactive Filters**: Users can filter survey results by department, employee role, response type, and specific survey questions for deeper analysis and segmentation.
- **Visualizations**: The dashboard uses bar charts, stacked columns, and summary cards to display employee satisfaction, departmental performance, and response trends.
- **Custom Groupings**: Departments were categorized into 10 broader groups to simplify analysis and highlight trends across organizational clusters.
- **Survey Question Simplification**: Long survey questions were renamed to concise, readable labels to enhance dashboard clarity and usability.
- **Highlight Cards (KPIs)**: Summary cards provide quick insight into the total number of Staff, Managers, Directors, and Supervisors.
- **Departmental Insights**: Key sections focus on job satisfaction, workplace support, productivity, and growth opportunities across departments.
- **Dynamic Data Updates**: All visuals update instantly based on slicer selections, enabling targeted comparisons and scenario-based insights.

![Employee_Survey_Dataset]("")

---

## Key Metrics
1. **Total Survey Responses**: 14,725
2. **Employee Role Breakdown**:
   - Staff: 1,239
   - Managers: 1,061
   - Directors: 164
   - Supervisors: 1,645
3. **Highest Agreed Survey Statement**: “Department Inclusion & Diversity” (663 agreements)
4. **Lowest Agreed Survey Statement**: “Job Role Clarity” (495 agreements)
5. **Department with Highest Satisfaction**: Infrastructure & Transportation
6. **Top Department for Learning & Growth**: Human Resources
7. **Department with Lowest Employee Satisfaction**: Economic Development
8. **Key Engagement Areas**: Job Satisfaction, Supervisor Support, Workplace Friendship, and Opportunity to Excel

---

## Insights
1. **High Agreement with Inclusion & Diversity**: Employees responded most positively to questions related to diversity and inclusion, showing strong support for an inclusive workplace culture.
2. **Departments with Clear Growth Paths Show Higher Satisfaction**: Departments like Infrastructure & Transportation and Human Resources had the highest satisfaction and learning opportunities, indicating that development opportunities influence engagement.
3. **Job Role Clarity and Recognition Are Weak Points**: Statements about job role clarity and recent recognition received the lowest levels of agreement, suggesting gaps in communication and appreciation.
4. **Supervisors Have a Strong Impact on Engagement**: Survey items related to supervisor support and accountability had varied responses across departments, indicating that leadership quality differs significantly by team.

---

## Tools & Techniques Used
1. **Power BI**:
   - Power Query Editor for extensive data cleaning and transformation.
   - DAX (Data Analysis Expressions) to calculate key metrics.
   - Slicers for dynamic filtering.
   - Custom Visuals including bar charts, pie charts, stacked columns, and KPIs for clear insight presentation.
2. **Figma**: Designed visual mockups and layout guides to ensure a clean, user-friendly dashboard interface.

---

## Questions & Answers
### Q1: Which survey questions did respondents agree with or disagree with most? 
**Ans**: Respondents agreed most with statements related to inclusion and diversity and job satisfaction, while the least agreement was observed in areas concerning recognition for good work, supervisor accountability, and clarity around job roles.

### Q2: Do you see any patterns or trends by department or role? 
**Ans**: Yes. Departments like Infrastructure & Sustainability and Legal & Judicial had the highest satisfaction levels and growth opportunities, while departments like Facilities Management and Economic Development showed lower levels of positive sentiment. In terms of roles, supervisors had the highest representation, and staff made up the majority of respondents. Certain roles consistently reported lower satisfaction, especially in areas of praise and performance accountability.

### Q3:  As an employer, what steps might you take to improve employee satisfaction based on the survey results?  
**Ans**: To improve satisfaction, I would prioritize recognizing employee efforts, enhancing clarity of job expectations, and holding supervisors more accountable for team performance.

---

## Recommendation
1. Implement structured recognition systems to regularly highlight employee achievements and foster a culture of appreciation.
2. Provide role-specific training and frequent manager check-ins to ensure employees clearly understand their responsibilities and performance expectations.
3. Replicate learning and development initiatives from high-performing departments (e.g., Human Resources) across other units to improve satisfaction organization-wide.
4. Equip all supervisors with people-management training to ensure consistent employee support, accountability, and workplace experience.
---

## Conclusion
The employee engagement survey analysis revealed key strengths in workplace inclusivity and growth opportunities, while also identifying areas needing improvement such as recognition and job clarity. Addressing these gaps through targeted initiatives can significantly enhance overall employee satisfaction and organizational performance.

---

## Author
This project was created by Sakira, a data analyst with a strong background in data storytelling, dashboard design, and analytical problem-solving. I use tools like Excel, Power BI, and SQL to transform raw data into actionable insights. I'm passionate about building user-centric dashboards that reveal trends, improve decision-making, and create impact across various industries. [[www.linkedin.com/in/sakira-daodu-b44666275](https://www.linkedin.com/in/sakira-daodu-b44666275/)].
