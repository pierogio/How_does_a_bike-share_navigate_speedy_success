# How_does_a_bike-share_navigate_speedy_success:

[![forthebadge made-with-R](https://img.shields.io/badge/Made%20with-R-blue?style=for-the-badge&logo=R)](https://www.r-project.org/)
[![forthebadge made-with-RStudio](https://img.shields.io/badge/Made%20with-RStudio-blue?style=for-the-badge&logo=RStudio)](https://www.rstudio.com/)

### Introduction

Welcome to this Cyclistic bike-share analysis project! In this case study, I step into the role of a junior data analyst for the fictional company Cyclistic. The goal of this project is to solve key business questions using real-world data. I'll be following the complete data analysis process—asking questions, preparing and analyzing data, and sharing insights to drive business decisions.
Through this project, I aim to demonstrate my analytical skills while exploring bike-share usage patterns and trends. 

### Scenario

You are a junior data analyst on the marketing team at Cyclistic, a bike-share company in Chicago. The company’s director of marketing, Lily Moreno, believes increasing annual memberships is key to Cyclistic's growth. Your team is tasked with understanding how casual riders and annual members use the service differently to inform a new marketing strategy aimed at converting casual riders into annual members. Before implementing any recommendations, the executive team needs to approve your insights, which must be supported by data-driven analysis and professional visualizations.

### Key Stakeholders

**Director of Marketing (Lily Moreno)**  
Oversees marketing strategy and uses data insights to convert casual riders into annual members.

**Marketing Analytics Team**  
Collects and analyzes data to inform marketing strategies.

**Cyclistic Executive Team**  
Approves marketing strategies based on data-driven insights.

#### About the Company

Cyclistic launched a bike-share program in 2016, now offering 5,824 bikes across 692 stations in Chicago. The bikes can be unlocked and returned at any station in the system. Cyclistic's marketing strategy has focused on general awareness with flexible pricing options: single-ride passes, full-day passes, and annual memberships.
Casual riders use single-ride or full-day passes, while annual members are more profitable. Cyclistic's finance team has emphasized the importance of growing the annual membership base for future success. Marketing director Lily Moreno aims to convert casual riders into members, believing they are already familiar with Cyclistic. To develop targeted strategies, the team will analyze historical bike trip data to understand rider behaviors and how digital media can support these efforts.

### ASK
#### Task Overview

Three key questions guide the future marketing strategy:
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy annual memberships?
3. How can digital media be used to convert casual riders into members?

Your task is to address the first question: ***How do annual members and casual riders use Cyclistic bikes differently?***

#### Deliverables:

1. A clear statement of the business task
2. A description of all data sources used
3. Documentation of data cleaning and manipulation
4. A summary of your analysis
5. Visualizations and key findings
6. Top three recommendations based on the analysis


### 2. Prepare

The dataset used for this analysis consists of 12 months of historical bike trip data (2021/01-2021/12) from the Cyclistic bike-share service. The data is publicly available and provided by **Motivate International Inc.** under a public license. The dataset includes information on ride duration, start and end times, stations, and the user type (either casual or annual member).

Key steps in preparing the data:
- **Data Import**: All CSV files containing the data were loaded into R and combined into a single dataset.
- **Data Cleaning**: 
  - Removed rows where `start_station_name` and `end_station_name` were missing to avoid incomplete ride data.
  - Calculated `ride_length` as the difference between `ended_at` and `started_at` to assess trip durations.
  - Filtered out negative ride lengths caused by data entry errors.
- **Data Integrity**: The dataset was checked for inconsistencies, missing values, and errors to ensure accurate analysis.

By ensuring the data was cleaned and prepared effectively, I could then proceed to analyze and generate insights on how casual riders and annual members use Cyclistic bikes differently.

### 3. Process

In this phase, I processed the data to ensure it was clean and ready for analysis. The following steps were taken:

- **Checking for Missing Values**: After loading the data, I identified that some fields, such as `start_station_name` and `end_station_name`, contained missing values. These rows were removed to avoid inaccuracies in the analysis.
  
- **Ride Length Calculation**: I created a new column, `ride_length`, to calculate the duration of each ride. This was done by subtracting the `started_at` time from the `ended_at` time, and the result was converted into minutes for easier comparison.

- **Handling Invalid Data**: Some ride lengths were negative due to errors in the data. These rows were filtered out to maintain data accuracy.

- **Ensuring Consistency**: The data types of each column were checked and ensured to be consistent with the analysis needs (e.g., `started_at` and `ended_at` columns were properly formatted as date-time).

- **Grouping by User Type**: I grouped the data by the `member_casual` column to distinguish between casual riders and annual members for comparison throughout the analysis.

With the data fully processed and cleaned, I ensured that it was accurate and consistent for the following analysis phase.

### 4. Analyze

After cleaning and processing the data, I conducted an analysis to uncover key insights into how **casual riders** and **annual members** use Cyclistic's bikes differently. The following analysis steps were taken:

- **Ride Length by User Type**: I calculated summary statistics (mean, median, minimum, maximum) for the `ride_length` column, grouped by `member_casual`. This allowed for a comparison between the typical ride durations of casual riders and annual members. The analysis revealed that casual riders tend to take longer rides compared to annual members.

- **Ride Patterns by Day of the Week**: I analyzed the average ride length and the total number of rides by day of the week, for both casual riders and annual members. This showed that casual riders are more active on weekends, while annual members maintain steady usage throughout the week, likely using the service for commuting.

- **Seasonal Trends**: I examined the total number of rides and the average ride length by month. Casual riders' usage spiked during the summer months (June to August), while annual members maintained a more consistent pattern of usage throughout the year, even during colder months.

- **Bike Type Preferences**: I explored the use of different bike types (classic, electric, and docked) among casual riders and annual members. It was observed that casual riders are more likely to use electric bikes, likely due to their longer ride durations, while annual members favor classic bikes for commuting.

These insights were key in understanding the behavioral differences between casual riders and annual members, providing valuable information for the marketing team to develop targeted strategies.

### 5. Share

After analyzing the data, I created a series of visualizations to effectively communicate the key findings to Cyclistic's stakeholders. These visualizations were essential in providing clear insights into how casual riders and annual members use Cyclistic's bikes differently. Below are the visualizations generated:

1. **Average Ride Length by Day of the Week**:
   - This bar chart compares the average ride length for casual riders and annual members across each day of the week, showing that casual riders tend to take longer rides, especially on weekends.

2. **Total Number of Rides by Day of the Week**:
   - This visualization highlights the number of rides taken by casual riders and annual members each day. It demonstrates that casual riders are most active on weekends, while annual members have consistent usage throughout the week.

3. **Total Rides by User Type**:
   - This chart breaks down the total number of rides taken by casual riders and annual members, showing that annual members have a higher overall number of rides, despite casual riders taking longer trips on average.

4. **Average Ride Length by Month**:
   - This visualization shows how the average ride length changes month by month for both casual riders and members, highlighting the increase in ride length for casual riders during the summer months.

5. **Number of Rides by Bike Type and User Type**:
   - This bar chart shows the breakdown of bike types (classic, electric, docked) used by casual riders and annual members, demonstrating that casual riders prefer electric bikes more than annual members.

All visualizations are saved in the **images** folder and are used to support the analysis and recommendations presented to the Cyclistic marketing team. These visualizations help explain the distinct behaviors of casual riders and annual members, making the findings easier to understand for stakeholders.

### 6. Act

The analysis of Cyclistic's bike-share data reveals clear distinctions between how casual riders and annual members use the service, with significant implications for marketing strategies aimed at converting casual riders into members.

Starting with ride length, casual riders consistently take longer rides compared to annual members. This trend is evident throughout the week, but it is especially pronounced on weekends, with casual riders taking notably longer trips, particularly on Sundays. This suggests that casual riders are primarily using Cyclistic’s bikes for leisure or recreational purposes. In contrast, annual members exhibit more consistent ride lengths across all days, with shorter, more frequent rides. These patterns suggest that members are using the service for more utility-based purposes, such as commuting or running errands, rather than for extended leisure trips.

When we examine the total number of rides, annual members dominate in terms of ride frequency. Despite taking shorter rides, members account for a higher overall number of trips across both weekdays and weekends. Their usage peaks slightly during the workweek, likely aligning with typical commuting schedules, while casual riders show a sharp increase in activity during weekends. This supports the notion that casual riders view bike-sharing as an occasional service for leisure, while members incorporate it into their regular routines.

Seasonally, both groups exhibit increased activity during the warmer months, particularly from June to August, when casual riders' usage surges. This seasonal trend likely corresponds with improved weather conditions, which encourage recreational rides, especially for casual users. However, members maintain a relatively steady level of usage even in colder months, which further supports the idea that their rides are more necessity-driven, such as for commuting, regardless of the weather.

The data also reveal preferences in bike types. Classic bikes are the most popular among both casual riders and members, but annual members show a stronger preference for them, likely due to their practical nature for commuting and shorter trips. Casual riders, on the other hand, make more use of electric bikes, which could be due to the longer leisure rides they typically take, where electric assistance would be beneficial.

Given these findings, Cyclistic should consider developing marketing strategies that capitalize on casual riders' weekend and seasonal behavior. For instance, offering weekend or summer-specific membership promotions could attract casual users who already demonstrate a willingness to use the service for extended leisure trips during these periods. Additionally, marketing the advantages of membership for frequent riders, such as cost savings over multiple weekend trips or electric bike use, could appeal to casual users who enjoy longer, recreational rides but may not yet see the value in committing to an annual membership.

For annual members, Cyclistic might focus on highlighting the utility of the service, especially for everyday commuting, by offering promotions or incentives for consistent weekday use. Providing value-added features, such as priority access to electric bikes for members or rewards for frequent usage, could further incentivize casual riders to convert to memberships.

In conclusion, the data clearly show that casual riders and annual members use Cyclistic bikes in very different ways. Casual riders are primarily weekend and leisure users, while members are more frequent, utility-driven riders. By tailoring marketing campaigns to these distinct patterns, Cyclistic can increase membership conversions and ultimately drive the long-term success of the bike-share program.

