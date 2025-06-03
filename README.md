Cyclistic Data Integration and Cleaning Project (Python)

Introduction:
This project focuses on integrating and cleaning large-scale bike trip datasets from Cyclistic, a bike-sharing service. The goal is to consolidate and standardize multiple CSV files into a single, clean dataset suitable for analysis and modeling.

Objectives:

Merge multiple monthly CSV files into one unified DataFrame.
Clean the dataset by addressing missing values and removing duplicates.
Convert data types and standardize formats for consistency.
Export the cleaned dataset for future use.

Methodology:

Data Collection: CSV files were sourced from Cyclistic’s public dataset repository.
Integration: Using the pandas library, all files were merged via pd.concat() to form a single DataFrame without data loss.
Cleaning:
Missing Values: Null values in object columns (e.g., station names) were filled with "not specified"; numerical columns (e.g., coordinates) were filled with -999.
Duplicates: Duplicate rows were detected and removed using duplicated() and drop_duplicates().
Date Conversion: Start and end times were standardized using pd.to_datetime() for better temporal analysis.
Export: The cleaned dataset was saved as merged_data.csv for use in later stages of the analysis pipeline.


Results:

Successfully merged 12 CSV files, totaling over 20 million ride records.
Cleaned dataset is now consistent, de-duplicated, and ready for EDA, visualization, and predictive modeling.


Cyclistic Bike Usage Analysis (SQL)

Introduction:
This project investigates the behavioral differences between Cyclistic’s annual members and casual riders. By analyzing ride history data through SQL, the project aims to derive actionable insights for operational and marketing strategies.

Objective:
To uncover how ride frequency, duration, timing, and bike preference vary between casual riders and annual members.

Methodology:

Database Setup: Ride data was loaded into a PostgreSQL table named cyclist using the COPY command.
Data Enrichment: SQL functions such as TO_CHAR() and EXTRACT() were used to derive new columns (month, weekday, time of day, ride length).
Data Cleaning: Ensured uniformity in categorical fields (e.g., rider_type, rideable_type) and checked for nulls.


Analysis:

Usage Breakdown:
Count and proportion of rides per bike type and rider category.
Average ride duration for each bike-rider combination.
Temporal Trends:
Ride frequency by month, weekday, and time of day.
Comparison of average ride length across these dimensions.


Key Insights:

Bike Preference: Electric bikes are most popular across all users, while docked bikes are least used.
Ride Duration: Casual riders typically take longer rides than members.
Time Trends:
Annual members favor short weekday rides, reflecting a commute pattern.
Casual riders prefer longer rides on weekends and evenings, indicating recreational usage.


Conclusion:
This SQL-based analysis reveals clear differences in usage patterns between casual and annual Cyclistic users. While members ride more often on weekdays for short commutes, casual users ride longer and more often on weekends. These insights can help tailor services, infrastructure, and promotions to each user group more effectively.
