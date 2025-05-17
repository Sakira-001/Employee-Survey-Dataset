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
4. **Director**:Binary (0/1) field indicating if the respondent is in a Director role.
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
1. **Total Reported Collisions**: 91,286
2. **Total Injuries**: 45,317
   - Persons Injured: 37,198
   - Pedestrians Injured: 4,211
   - Cyclists Injured: 1,932
   - Motorists Injured: 1,976
3. **Total Fatalities**: 276
   - Persons Killed: 213
   - Pedestrians Killed: 39
   - Cyclists Killed: 12
   - Motorists Killed: 12
4. **Borough with Most Collisions**: Brooklyn
5. **Most Common Contributing Factor**: Driver Inattention/Distraction
6. **Peak Collision Hours**: Between 3 PM – 6 PM
7. **Collisions by Vehicle Type**:
   - Passenger Vehicles: 58%
   - Commercial Vehicles: 18%
   - Two-Wheelers (Motorcycles, Bicycles): 9%
   - Emergency Services: 3%
   - Others: 6%
   - Unknown/Not Reported: 6%
8. **Seasonal Pattern**: Highest collisions recorded in October, lowest in February
9. **Most Affected Demographic**: Motorists and pedestrians injured in Brooklyn and Queens
10. **Location Hotspots**: Most incidents occurred in densely populated areas with high traffic volume

---

## Insights & Conclusions
1. **Leading Causes of Collisions**:
   - The top contributing factor to collisions is "Unspecified", meaning a lack of detailed reporting.
   - Driver inattention/distraction is the most reported cause, emphasizing the need for awareness campaigns on focused driving.
2. **Fatalities Across Boroughs**:
   - Brooklyn has the highest fatalities among pedestrians, motorists, and cyclists.
   - Motorists experience the most fatalities overall, suggesting that driver safety improvements are needed.
3. **Vehicle Types in Collisions**:
   - Passenger vehicles account for the highest number of collisions, far exceeding any other vehicle type across all boroughs.
   - Bicycles, taxis, motorcycles, and buses contribute to accidents but at significantly lower numbers compared to passenger vehicles.
   - Brooklyn leads in overall collisions, followed by Queens and the Bronx, possibly due to higher traffic density and population.

---

## Tools & Techniques Used
1. **Power BI**:
   - Power Query Editor for extensive data cleaning and transformation.
   - DAX (Data Analysis Expressions) to calculate key metrics like total collisions, injuries, fatalities, and percentage breakdowns.
   - Slicers for dynamic filtering by borough, vehicle type, month, and contributing factors.
   - Custom Visuals including bar charts, pie charts, stacked columns, KPIs, and heatmaps for clear insight presentation.
2. **Figma**: Designed visual mockups and layout guides to ensure a clean, user-friendly dashboard interface.

---

## Questions & Answers
### Q1: Compare the % of total accidents by month. Do you notice any seasonal patterns? 
**A**: Yes, a clear seasonal pattern emerges. The highest percentage of accidents occurred in October, followed by June and August. The months with the lowest accident rates were February and January.

### Q2: Break down accident frequency by day of week and hour of day. Based on this data, when do accidents occur most frequently?
**Ans**: - Accidents peak sharply around midnight (12:00 AM) — likely due to the timestamp default or batch reporting practices — followed by a steady increase from 6:00 AM, with consistent spikes between 8:00 AM to 6:00 PM, especially around 3:00 PM to 6:00 PM, coinciding with afternoon rush hours.
         - By Day of Week: Fridays have the highest accident frequency, followed closely by Thursdays and Wednesdays.
Weekends (especially Sundays) see fewer incidents, likely due to reduced commuting traffic.

### Q3:  On which particular street were the most accidents reported? What does that represent as a % of all reported accidents? 
**Ans**: The street with the most reported accidents was Brooklyn.

### Q4: What was the most common contributing factor for the accidents reported in this sample (based on 
Vehicle 1)? What about fatal accidents specifically?  
**Ans**: - The most common contributing factor across all accidents (based on Vehicle 1) was Unspecified.
         - For fatal accidents specifically, the leading contributing factor remained Unspecified.

---

## Recommendation
1. Enhance Driver Awareness & Distraction Prevention Campaigns: Implementing stricter penalties for distracted driving and Conducting public awareness campaigns on focused driving and accident prevention.
2. Improve Traffic Control & Law Enforcement: Increase traffic patrols in high-collision areas and Enforce speed limits, right-of-way laws, and lane discipline more strictly.
3. Develop Safer Infrastructure for Cyclists & Pedestrians: Expand dedicated bike lanes and pedestrian-friendly zones and Install more traffic calming measures (e.g., speed bumps, pedestrian islands).
4. Targeted Safety Measures in High-Collision Boroughs: Brooklyn & Queens: Implement city-wide road safety programs due to high fatalities.
---

## Conclusion
This project successfully analyzed NYC traffic accident data to identify key patterns and risk factors. The insights gathered can help inform safety initiatives, improve traffic management, and reduce accident occurrences through data-driven decisions.

---

## Author
This project was created by Sakira, a data analyst with a strong background in data storytelling, dashboard design, and analytical problem-solving. I use tools like Excel, Power BI, and SQL to transform raw data into actionable insights. I'm passionate about building user-centric dashboards that reveal trends, improve decision-making, and create impact across various industries. [[www.linkedin.com/in/sakira-daodu-b44666275](https://www.linkedin.com/in/sakira-daodu-b44666275/)].
