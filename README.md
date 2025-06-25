# Morocco Electricity Consumption Analysis for the year 2017

### Project Overview
This project focuses on analysing electricity consumption patterns across three zones in Morocco using Power BI. The primary objective is to gain actionable insights into how electricity is consumed over time, how consumption varies across different regions, and how external factors such as temperature influence energy demand.


### Data Source
The dataset used in this analysis contains detailed records of electricity consumption and related environmental conditions across three zones in Morocco. The data was collected at 10-minute intervals, providing high-resolution insights into energy usage patterns over time. The dataset was assessed from the Maven Analytics website. 

[Download Here](https://mavenanalytics.io/data-playground?page=4&pageSize=5)


### Tools

- Power Query
- PowerBI


### Data Cleaning/Preparation
In carrying out the analysis, Power Query and PowerBI were used exclusively. The .csv file was imported into PowerBI, then transformed and analysed. The steps followed during the analysis process are listed below. 

1. The datetime column was separated into separate columns, date, and time, to each contain the date and time data in that order.

2. Renamed Columns for better readability.

3. Set the proper data type for each column. 

4. Created a new column, weekday, to include the day of the week each data was collected e.g. Monday, Tuesday etc. Another column was created labeled ‘weekday num’, which stores the numeric value of each day of the week, i.e. 1 for Sunday, 2 for Monday. This was used in sorting the Weekday column.

5. Data analysis expressions (DAX) was written to create some calculated measures needed for analysis. Measures created are:
 
  - Average hourly consumption – to determine the trend of consumption hourly
  - Average weekly consumption - to determine the trend of consumption weekly
  - mom % growth – to determine the growth or decline rate of consumption across months
  - total consumption – to determine the total usage. It can be segmented across months, days etc. 
  - Correlation factor – 3 different correlation factors were calculated for the 3 different external variables, to determine       their relationship with the electricity consumed.


### Results/Findings

This phase of the report presents the results of the analysis process. Analysis reveals that a total of 3.73 thousand GWh was consumed across the 3 zones for the year 2017. The results are presented in a manner to answer the objective questions.


**1. Monthly Trend:**
There is a noticeable drop in consumption from January to February. Consumption steadily increases month-by-month from February to July, with the sharpest rise occurring between June and July, where it reaches the peak. After peaking in July, consumption decreases sharply through August and September. Afterwards, consumption stabilises at a lower level, with a slight decline as the year ends. The data shows a mid-year peak (July) in electricity consumption, possibly driven by seasonal factors such as high temperatures (e.g., cooling loads during summer).


![image](https://github.com/user-attachments/assets/f5be373e-133c-4bc9-8b91-923e3dc62faf)


**2. Weekly Trend:**
Consumption starts at its lowest point on Sunday, just under 1,400 MWh, and then experiences a significant jump to reach a peak on Monday, rising to just over 1,470 MWh. After the sharp rise on Monday, consumption continues to increase, but at a much slower, more gradual rate, reaching its highest on Thursday. It then begins to decline steadily through Friday and Saturday. 
In summary, the consumption trend shows a strong start to the week with a large increase from Sunday to Monday, followed by a period of relatively high and stable consumption mid-week (Monday to Thursday), and then a decline towards the weekend.


![image](https://github.com/user-attachments/assets/74ed9fc3-c31b-436f-93a3-8c4ca79c4381)


**3. Hourly consumption:**
Consumption starts high, around 72 units at midnight and then steadily decreases, reaching its lowest point of approximately 50 units at 6:50 AM. This suggests a period of minimal activity or demand during the very early hours of the morning.

After hitting its lowest point, consumption begins to rise sharply from 6:50 AM, indicating the start of daily activities. It continues to increase, peaking around 76 units by 1:00 PM. 

Following the midday peak, there's a slight dip in consumption between 1:00 PM and approximately 4:00 PM, where it drops to around 72 units. After this dip, consumption starts to rise again as the late afternoon progresses towards evening. 

Consumption experiences a significant surge in the evening, starting from around 6:00 PM and reaching its highest peak for the day, just shy of 100 units, between 8:00 PM and 9:00 PM. This likely corresponds to peak evening activities when many people are home.


![image](https://github.com/user-attachments/assets/bf044b0d-4db3-4490-8a18-f69d7eebe66f)


**4. Which Variable affects electricity consumption more**


![image](https://github.com/user-attachments/assets/43e8cb25-3ea6-4a3f-86d7-9e22a3b1a080)



Temperature has the strongest relationship with electricity consumption. With a strong overall positive correlation of 0.73


### Recommendations

The following recommendations were made based on insights from the data:

1. Given the strong positive correlation (0.73) between consumption and temperature, prioritise temperature forecasts in electricity demand prediction models.
   
2. Use the hourly trend data to optimize generation, transmission, and distribution operations.
   
3. Schedule maintenance activities for early morning hours (e.g., 3:00 AM - 6:00 AM) when average hourly consumption is at its lowest.
