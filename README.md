# ABC CALL VOLUME TREND ANALYSIS

### Table of Contents

- [Project Description](#project-description)
- [Dataset Details](#dataset-details)
- [Data Understanding](#data-understanding)
- [Data Cleaning](#data-cleaning)
- [Tasks and Insights](#tasks-and-insights)
- [Conclusion](#conclusion)

### Project Description

In this project, we will explore Customer Experience (CX) analytics, focusing on an inbound calling team over a 23-day dataset. The CX team plays a vital role in analyzing customer feedback and data to derive insights that inform the organization. They deal with a variety of support requests, with the goal of engaging and satisfying consumers through inbound help. The competitive nature of advertising demands sharp analytical skills to identify cost-effective platforms. The goal is to analyze call volume trends and derive insights to improve customer experience, culminating in a data analysis report, actionable recommendations, and a presentation of findings. This project will enhance our understanding of inbound customer support and its impact on CX, providing valuable insights to optimize customer service operations.

### Dataset Details

The dataset contains information that spans 23 days and includes various details such as the agent's name and ID, customer phone number, the queue time (how long a customer had to wait before connecting with an agent), the date and time of the call, the duration of the call, the call status (whether it was abandoned, answered, or transferred) and Interactive Voice Response (IVR) duration.

### Data Understanding

- Total number of Records/ Rows : 1,17,988
- Total number of Columns : 13
- Columns containing BLANK / NULL values : `Wrapped_By` (47,877)
- Column having Abnormal Data Points (N/A) : `Agent_Name` (34,198) & `Agent_ID` (34,198)
  
### Data Cleaning

- Initially, we filtered the records based on `Call status`. For all the calls having the status “abandon”, their corresponding `Agent_Name`, `Agent_ID` and `Wrapped_By` were replaced with “Abandoned Call”. This will remove all the #N/A value from `Agent_Name` and `Agent_ID` column.
- The remaining Blank values in the `Wrapped_By` column were having the `Call status` as “answered” or “transfer”. All the “transfer” calls were wrapped by Agent. So replaced the blank values in `Wrapped_By` column corresponding to “transfer” call status with “Agent”. All the remaining blank values in `Wrapped_By` column corresponding to “answered” call status were replaced with “Agent” which was obtained as the MODE.

### Tasks and Insights

**1. Average Call Duration: What is the average duration of calls for each time bucket?**
Determine the average duration of all incoming calls received by agents. This should be calculated for each time bucket.
- Overall Average Duration of Call : 199 sec
![image](https://github.com/user-attachments/assets/8b92aff8-2880-4f7f-87d2-927c762a9a71)

**2. Call Volume Analysis: Can you create a chart or graph that shows the number of calls received in each time bucket?**
Visualize the total number of calls received. This should be represented as a graph or chart showing the number of calls against time. Time should be represented in buckets (e.g., 1-2, 2-3, etc.).
- Maximum No. of calls are received during the time interval : 9 AM – 3 PM
![image](https://github.com/user-attachments/assets/22693d8a-8c9f-45d5-8863-ff444809c061)

**Assumptions:** An agent works for 6 days a week; On average, each agent takes 4 unplanned leaves per month; An agent's total working hours are 9 hours, out of which 1.5 hours are spent on lunch and snacks in the office. On average, an agent spends 60% of their total actual working hours (i.e., 60% of 7.5 hours) on calls with customers/users. The total number of days in a month is 30.

**3. Manpower Planning: What is the minimum number of agents required in each time bucket to reduce the abandon rate to 10%?**
The current rate of abandoned calls is approximately 30%. Propose a plan for manpower allocation during each time bucket (from 9 am to 9 pm) to reduce the abandon rate to 10%. In other words, you need to calculate the minimum number of agents required in each time bucket to ensure that at least 90 out of 100 calls are answered.
- Most of the calls are abandoned during the initial and closing hours : 9 AM – 12 PM and 8 PM – 9 PM
![image](https://github.com/user-attachments/assets/d81706ea-bb74-4593-9ba3-828c84372c18)
![image](https://github.com/user-attachments/assets/2ca2923b-648e-4427-a00b-e77926535e77)

**4. Night Shift Manpower Planning: Propose a manpower plan for each time bucket throughout the day, keeping the maximum abandon rate at 10%.**
Customers also call ABC Insurance Company at night but don't get an answer because there are no agents available. This creates a poor customer experience. Assume that for every 100 calls that customers make between 9 am and 9 pm, they also make 30 calls at night between 9 pm and 9 am. The distribution of these 30 calls is as follows:
![image](https://github.com/user-attachments/assets/910e2999-961d-4582-bf53-788ea441f19e)
- This chart showing the number of agents required  during the night time to get a 10% Abandoned rate with a calculation that an agent can handle 18 calls per hour. 
![image](https://github.com/user-attachments/assets/657a9c20-1068-44ea-8184-f8950f9dcea9)
- This is the chart showing the number of agents required to get a 10% Abandoned rate for an overall day with a calculation that an agent can handle 18 calls per hour. 
  - Least number of Agents required : 12 AM – 05 AM
  - Maximum number of Agents required : 09 AM – 03 PM
![image](https://github.com/user-attachments/assets/209487f4-5913-4e32-8ea9-fdba221075be)

### Conclusion

This project enables to get a thorough understanding of the dynamics of inbound customer support and the ability to derive insights that can enhance the overall customer experience. The analytical contributions regarding the average call duration, number of calls received during each time frame, the number of agents / employees needed to get maximum output will help the company optimize its customer service operations and maintain a competitive edge in the market.








