# How_does_a_bike-share_navigate_speedy_success:

[![forthebadge made-with-R](https://img.shields.io/badge/Made%20with-R-blue?style=for-the-badge&logo=R)](https://www.r-project.org/)
[![forthebadge made-with-RStudio](https://img.shields.io/badge/Made%20with-RStudio-blue?style=for-the-badge&logo=RStudio)](https://www.rstudio.com/)

```bash
## Project Structure
How_does_a_bike-share_navigate_speedy_success/
│
├── README.md                            # Project overview and findings
├── data/                                # Data files used in the analysis (optional)
├── images/                              # Visualizations generated from the analysis
├── Cyclistic_Bike_Share_Analysis.Rmd    # The single R script containing data loading, cleaning, analysis, and visualizations
```
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

## 2. PREPARE

**Dataset Overview:**
- The dataset includes 12 months of bike trip data (2021/01-2021/12) from Cyclistic, containing ride duration, start and end times, stations, and user type (casual or annual member).

**Preparation Steps:**
- **Data Import**: Combined multiple CSV files into a single dataset in R.
- **Data Cleaning**:
  - Removed rows with missing `start_station_name` or `end_station_name`.
  - Calculated `ride_length` by subtracting `started_at` from `ended_at`, converted to minutes.
  - Filtered out negative ride lengths.
- **Data Integrity**: Checked for inconsistencies, missing values, and errors to ensure accuracy.

## 3. PROCESS

**Data Processing Steps:**
- **Missing Values**: Removed rows with missing `start_station_name` or `end_station_name`.
- **Ride Length Calculation**: Created `ride_length` column (duration in minutes) from `started_at` and `ended_at`.
- **Handling Invalid Data**: Filtered out negative `ride_length` values.
- **Consistency Check**: Ensured proper formatting of date-time columns and consistent data types.
- **Grouping by User Type**: Grouped data by `member_casual` for comparison.

## 4. ANALIZE

**Analysis Steps:**
- **Ride Length by User Type**: Calculated summary statistics (mean, median, min, max) of `ride_length` by `member_casual`. Found that casual riders take longer rides.
- **Ride Patterns by Day of the Week**: Analyzed average ride length and total number of rides by day of the week. Casual riders were more active on weekends; annual members had consistent usage throughout the week.
- **Seasonal Trends**: Examined monthly totals and average ride lengths. Casual riders had higher usage in summer; annual members had consistent usage year-round.
- **Bike Type Preferences**: Compared bike type usage between casual and annual members. Casual riders preferred electric bikes; annual members favored classic bikes.

## 5. SHARE

**Visualizations:**

1. **Average Ride Length by Day of the Week**:
   - A bar chart comparing the average ride length for casual riders and annual members by day. Casual riders generally take longer rides, especially on weekends.

2. **Total Number of Rides by Day of the Week**:
   - A chart showing the number of rides per day for casual riders and annual members. Casual riders are more active on weekends, while annual members use the service consistently throughout the week.

3. **Total Rides by User Type**:
   - A chart depicting the total number of rides by casual riders versus annual members. Annual members have a higher total ride count, though casual riders take longer trips on average.

4. **Average Ride Length by Month**:
   - A visualization of how the average ride length varies month by month. Casual riders' ride lengths increase during the summer months.

5. **Number of Rides by Bike Type and User Type**:
   - A bar chart breaking down bike type usage (classic, electric, docked) by user type. Casual riders favor electric bikes more than annual members.

All visualizations are saved in the **images** folder.

## 6. ACT

The analysis of Cyclistic's bike-share data highlights key differences between casual riders and annual members, offering actionable insights for targeted marketing strategies.

**Key Insights:**

- **Ride Length**: Casual riders take longer rides, especially on weekends, suggesting leisure use. Annual members have shorter, more consistent rides, indicating utility-based use such as commuting.

- **Total Rides**: Annual members ride more frequently overall, with peak usage during weekdays. Casual riders increase their usage on weekends, reflecting occasional leisure use.

- **Seasonal Trends**: Both groups show increased activity in warmer months (June to August). Casual riders' usage spikes in summer, while annual members maintain steady usage year-round.

- **Bike Type Preferences**: Classic bikes are favored by both groups, with annual members showing a stronger preference. Casual riders use electric bikes more, likely due to longer leisure rides.

**Recommendations:**

- **For Casual Riders**: 
  - Develop promotions for weekends and summer to attract users who favor leisure rides.
  - Highlight membership benefits for frequent weekend riders and electric bike users.

- **For Annual Members**:
  - Emphasize the utility of the service for commuting and everyday use.
  - Offer incentives for consistent weekday use and provide perks like priority access to electric bikes.
