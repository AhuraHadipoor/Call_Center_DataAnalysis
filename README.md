# Call Center Dashboard using Power BI

## Introduction
This project involves creating an interactive dashboard using Power BI to analyze call center performance. The dataset contains various attributes related to customer service interactions, including call details, agent performance, response times, and customer satisfaction levels. The project aims to derive meaningful insights and key performance indicators (KPIs) to assess call center efficiency and customer experience.

## Background
Call centers are critical for businesses to manage customer interactions effectively. Monitoring and analyzing call center data can help improve agent efficiency, reduce response times, and enhance customer satisfaction. In this project, I developed a Power BI dashboard to visualize key metrics and trends that impact customer service quality.

## Tools Used
- **Power BI**: For data visualization and dashboard creation
- **Microsoft Excel**: For preprocessing and managing dataset
- **DAX (Data Analysis Expressions)**: For calculating key performance indicators (KPIs)

## How It Works
### Dataset
The dataset includes the following columns:
- **CallID**: Unique identifier for each call
- **Agent**: The agent who attended the call
- **Date & Time**: Timestamp of the call
- **Topic**: Subject of the call
- **Answered (Y/N)**: Whether the call was answered
- **Resolved (Y/N)**: Whether the issue was resolved
- **Speed of Answer (seconds)**: Time taken to answer the call
- **Average Talk Duration**: Duration of the call in seconds
- **Satisfaction Level (1-5)**: Customer's rating of satisfaction
- **Month**: Month in which the call was made

### Key Performance Indicators (KPIs)
1. **Customer Satisfaction (CSAT)**
   - Measures the percentage of answered calls that were resolved.
   - Formula in DAX:
   ```DAX
   CSAT = DIVIDE(
       COUNTROWS(FILTER(Sheet1, Sheet1[Resolved] = "Y")),
       COUNTROWS(FILTER(Sheet1, Sheet1[Answered (Y/N)] = "Y"))
   ) * 100
   ```
   - Helps understand how well customer issues are being resolved.

2. **Average Speed of Answer**
   - Measures the average time taken to answer a call.
   - Helps assess efficiency in responding to customer calls.

3. **Percentage of Calls Blocked by Month**
   - Determines the percentage of calls that were not answered each month.
   - Helps analyze trends in customer service availability.

4. **Average Satisfaction Rating by Month**
   - Displays customer satisfaction trends over time.
   - Helps identify periods of high or low satisfaction.

5. **Average Satisfaction Rating by Speed of Answer**
   - Measures the impact of response speed on customer satisfaction.
   - Helps understand whether quicker responses lead to higher satisfaction levels.

### Dashboard Features
- **Interactive Filters**: Users can filter data by agent, month, and satisfaction level.
- **Visualizations**: Bar charts, line graphs, and KPI cards for quick insights.
- **Trends Analysis**: Allows monitoring of trends over different periods.
- **Performance Evaluation**: Helps managers assess agent efficiency and service quality.

## What I Learned
- Gained hands-on experience in designing interactive dashboards with Power BI.
- Improved understanding of customer service metrics and KPIs.
- Learned how to use DAX functions to calculate and visualize key insights.
- Understood the importance of data visualization in decision-making processes.

## Challenges
- Handling missing and inconsistent data in the dataset.
- Optimizing dashboard performance for large datasets.
- Ensuring accurate KPI calculations with DAX expressions.
- Designing a user-friendly and intuitive dashboard layout.

## Future Upgrades
- **Advanced Analytics**: Implement predictive analytics to forecast customer satisfaction trends.
- **Integration with Real-time Data**: Connect Power BI to a live database for real-time monitoring.
- **Enhanced User Experience**: Add more interactive elements like drill-through reports.
- **Agent Performance Analysis**: Include detailed breakdowns for individual agent performance.

## Conclusion
This project highlights the importance of data-driven decision-making in call center management. By using Power BI, we can transform raw data into meaningful insights, helping organizations improve their customer service efficiency and satisfaction levels. Future improvements will enhance the analytical capabilities of the dashboard, making it even more valuable for call center management.

