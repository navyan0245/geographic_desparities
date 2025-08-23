# geographic_desparities




## Table of Contents
* [Summary](#Summary)
* [PowerBI Dashboard](#PowerBI-Dashboard)
* [Motivation](#motivation)
* [Questions](#questions)
* [Normalizing the Data](#normaling-the-data)
* [Problems and Hurdles](#problems-and-hurdles)
* [Technologies Used](#technologies-used)
* [Data Sources](#sources)
* [Conclusion](#conclusion)

## Summary
This project investigates the distribution of licensed healthcare facilities across Tennessee counties and examines how that distribution correlates with factors such as urban vs. rural classification, age demographics, income levels, and racial composition. It also explores patient visit types including inpatient, outpatient, and emergency room visits and provides insights into the healthcare revenue cycle.
Additional drill-down options allow users to explore each metric by facility type, county, year(2021-2023) and individual facility.


## PowerBI Dashboard
Link: https://app.powerbi.com/view?r=eyJrIjoiYjM5NWE4N2EtMjA1NS00ODdlLWEzZDYtMWFjYmIzZDczMjE3IiwidCI6IjEwMWRhNTg3LTE4NDMtNGY1Mi04YjhhLTE3YjA2OWM2NmQzMyIsImMiOjJ9&pageName=276cb8cb035b7ceab0ce

## Motivation:
Access to healthcare is a critical determinant of public health, and disparities in facility distribution can exacerbate inequalities in health outcomes. Tennessee includes both highly urban and deeply rural regions, making it an ideal case study for analyzing spatial healthcare access. By mapping facilities and comparing access across counties, especially in relation to socioeconomic indicators, this project can provide insights useful to public health departments, policy makers, and advocacy groups. 

## Questions:
1) Are there geographic disparities in the distribution of licensed healthcare facilities across Tennessee counties?
2) Which Tennessee counties have fewer healthcare facilities per capita?
3) How does healthcare facility access correlate with median income, age, and race/ethnicity?
4) Are rural counties systematically underserved compared to urban ones?
5) Do In Patient visits increase with age?

## Normalizing the Data
The dataset I selected focused on licensed healthcare facilities across Tennessee counties, along with supporting demographic and socioeconomic data. Since the raw sources included multiple years and formats, I standardized them into a consistent structure by cleaning column names, ensuring county identifiers (FIPS codes) were properly formatted, and reshaping wide tables (such as age group patient counts) into long format for analysis.

## Exploratory Analysis
After cleaning and normalizing the data, I began exploring geographic and demographic patterns. 
Key steps included:Summarizing the number of licensed healthcare facilities per county and comparing urban versus rural counties.Aggregating patient visits by age group (14 & under, 15–17, 18–64, 75–84, 85 and over) to examine demand across different population segments.Evaluating the role of health insurance providers and the share of patients receiving government aid, broken down by county, race/ethnicity, and education level.Identifying counties with high disparities in facility availability relative to their population size and health needs.

## Problems and Hurdles
It was a challenge to clean and organize data because the file had multiple header rows and I had to concatenate them all with the actual column name to get the actual column name. This required extensive cleaning, unpivoting, and normalization.
The Azure Maps visual did not support choropleth fills at the county level, so a Shape Map with TopoJSON was required.

## Technologies Used
1) Python / Pandas - for exploration, normalizing and aggregation of the dataset
2) Power BI - for creating interactive dashboard
3) Canva - for presentation of Project
4) Git - for version control

## Data Sources
I used the following sources to collect datasets for my analysis

1) Public Joint Annual Report Data by Tennessee Department of health
https://internet.health.tn.gov/PublicJArs/default.aspx

2) Census data by census.gov. The dataset includes 2021-23 Tennessee county population by ethnicity.
https://data.census.gov/


## Conclusion
This project highlights clear geographic disparities in healthcare access across Tennessee counties. Urban areas tend to have higher concentrations of licensed facilities, while many rural counties operate with limited healthcare infrastructure despite having populations with high needs. Age group analysis further showed that older populations 75+ and younger populations under 18 face particular challenges in certain regions where facilities are sparse.
By incorporating demographic factors such as insurance type, government aid participation, race/ethnicity, and education, the analysis provided a more comprehensive view of healthcare access. These insights can help inform policymakers, healthcare organizations, and community planners on how resources might be better allocated to reduce inequities.


