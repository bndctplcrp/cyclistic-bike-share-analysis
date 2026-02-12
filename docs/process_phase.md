# Process Phase Documentation

A duplicate check was performed on the Q1 dataset using a full-column comparison in Excel, and no duplicate records were identified; therefore, no rows were removed during this step.

Records with missing values in critical fields (trip ID, start time, end time, or trip duration) were removed, while records with missing demographic values (gender and birth year) were retained due to privacy constraints and their non-essential role in the primary analysis.

Date and time columns were validated for consistency by confirming numeric datetime values, logical start–end order, and reasonable date ranges.

A ride_length column was created by subtracting the trip start time from the trip end time and formatted as HH:MM:SS to represent trip duration.

A day_of_week column was created using the WEEKDAY function to identify the day each ride started, where 1 represents Sunday and 7 represents Saturday.

The cleaned dataset was validated by checking for missing critical values, verifying time logic, confirming valid ride durations, and ensuring all derived columns met expected ranges prior to analysis.


### Q2 Dataset Processing Summary

The Q2 dataset contained non-standard column names and required schema alignment prior to analysis. All column headers were renamed to match the standardized structure used across other quarterly datasets. Date and time fields were validated and confirmed to be in proper datetime format after adjusting column display settings.

Date and time columns were validated for consistency by confirming numeric datetime values, logical start–end order, and reasonable date ranges.

A ride_length column was created by subtracting the trip start time from the trip end time and formatted as HH:MM:SS to represent trip duration.

A day_of_week column was created using the WEEKDAY function to identify the day each ride started, where 1 represents Sunday and 7 represents Saturday.

### Q4 Dataset Processing Summary
Records with invalid ride lengths resulting from inconsistent start and end times were removed during validation.


Primary analysis was conducted on a merged full-year 2019 dataset to ensure reliable and unbiased insights. Quarterly data was analyzed separately to identify seasonal trends and provide contextual support for the full-year findings.

Ride duration was displayed using a custom elapsed-time format ([h]:mm:ss) to accurately represent total ride length while preserving any non-numeric values.

The original usertype field was transformed into a standardized member_casual classification to align with business definitions and support comparative analysis.

A pivot table was used to calculate the average ride length for annual members and casual riders, enabling comparison of typical ride duration by user type.

Pivot tables were used to analyze ride behavior by user type and day of week. Average ride length was calculated to compare typical ride duration, and ride counts were calculated to examine usage frequency across the week.

A pivot table was created to calculate the number of rides by user type and day of the week. Ride counts were computed using a count of trip IDs to accurately represent usage frequency.

### Data Processing (Power Query)

Power Query Editor was used to append Cyclistic trip data from Q1–Q4 into a single consolidated dataset. Data cleaning and transformation steps included standardizing columns, validating data types, and creating calculated fields such as `ride_length` and `day_of_week`.

Because the combined dataset is large, the query was loaded using **Only Create Connection** with **Add this data to the Data Model** enabled instead of loading directly into an Excel table. This approach avoids Excel row limitations and supports advanced analysis using Power Pivot, relationships, and PivotTables.

Due to dataset size, data was loaded into Excel using the Data Model. Descriptive statistics such as mean, maximum ride length, and ride frequency by day of week were calculated using PivotTables connected to the model.

The mode of ride start day was identified by determining the day of the week with the highest number of rides. Tuesday recorded the highest ride volume, making it the most frequent ride day.

The maximum ride length observed was significantly higher than typical usage, indicating the presence of outliers likely caused by system errors or bikes not properly returned. These values were retained for transparency but considered non-representative of typical rider behavior.

Note: Extreme ride durations likely reflect data logging anomalies.
Maximum Ride Length    2953:20:22  (Outlier)

An extreme ride duration was identified and classified as an outlier. This value was retained for transparency but excluded from interpretation of typical rider behavior.

### Summary Statistics

To better understand the overall structure and distribution of the Cyclistic bike-share data, summary statistics were calculated using PivotTables connected to the Excel Data Model.

The average ride length across all trips was approximately 24 minutes, indicating that most rides were relatively short in duration. The maximum recorded ride length was significantly higher than typical usage and was identified as an outlier, likely caused by data logging anomalies or bikes not properly returned. This extreme value was retained for transparency but excluded from interpretation of typical rider behavior.

An analysis of ride frequency by day of the week showed that Tuesday had the highest number of rides, making it the most common day for bike usage. In total, over 3.1 million trips were analyzed, providing a robust dataset for identifying usage patterns.

These summary statistics provided an initial understanding of the data and informed subsequent analyses comparing ride behavior between casual riders and annual members.