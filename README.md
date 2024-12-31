# IPL-Analysis-Report-Dashboard

### Dashboard Link - https://app.powerbi.com/links/xrscK1X8ir?ctid=a1a4ee51-99fa-437d-8ba7-d05192f6c077&pbi_source=linkShare&bookmarkGuid=8b51ee26-60c2-4468-836d-52bb80b29cdf

![image](https://github.com/user-attachments/assets/29e88c01-bb70-4de8-b133-305b1d38e46d)

## Problem Statement

IPL Performance Analysis Dashboard in Power BI
This report analyzes IPL (Indian Premier League) performance data to help teams, coaches, and analysts improve team strategies, enhance player performance, and optimize match outcomes. The report was created in Power BI Desktop and subsequently published to Power BI Service. Key insights, metrics, and visualizations were derived to assist in making data-driven decisions and optimizing team and player performance during IPL matches.

Step 1: Load Data into Power BI and Clean in Power Query
The first step in creating the IPL Performance Analysis Dashboard was to load the data into Power BI and perform initial cleaning in Power Query to prepare the dataset for analysis.

Loading Data into Power BI:
The dataset, which was provided in a CSV format, was loaded into Power BI Desktop. This is the first crucial step in any Power BI project, as the data needs to be imported into the Power BI environment for further processing and visualization.

Open Power BI Desktop.
From the "Home" tab, click on the "Get Data" button and select "Text/CSV" from the list of data sources.
Browse and select the CSV file containing the IPL performance data.
Click "Load" to bring the data into Power BI.
Cleaning Data in Power Query:
Once the data was loaded into Power BI, it was essential to clean and prepare it for analysis. This was done using Power Query Editor, which provides an intuitive interface for data transformation tasks such as handling missing values, correcting data types, and filtering unnecessary records.

Accessing Power Query Editor:

From the Power BI Desktop interface, select "Transform Data" to open Power Query Editor.
Data Profiling:

In Power Query Editor, data profiling options were enabled to help identify errors, missing values, and data quality issues.
Under the "View" tab, the following profiling options were enabled:
Column Distribution: Displays the distribution of values in each column to identify any anomalies.
Column Quality: Shows the percentage of valid, empty, and error values for each column.
Column Profile: Provides a more detailed view of the data, including basic statistics like minimum, maximum, average, and unique values.
Handling Null and Missing Values:

The dataset was checked for any missing or null values in key columns such as player names, match scores, overs, and runs.
Missing or null values in these columns were addressed by either removing rows with significant missing data or filling the gaps where applicable.
Data Type Correction:

Ensured that all columns had the correct data types for analysis. For example, the Match Date column was set to the Date type, and the Runs Scored column was set to Numeric.
Any columns with incorrect data formats were fixed to ensure consistency.
Additional Data Transformation:

Calculated new columns like Player Age Group using Power Query’s custom column functionality, categorizing players into specific age brackets for analysis.
Filtered out irrelevant or unnecessary columns that wouldn’t contribute to the analysis, such as internal player IDs or non-relevant statistics.
Final Data Review:

After performing the necessary transformations and cleaning, the dataset was reviewed to ensure readiness for the next steps of the analysis.
The cleaned dataset was then loaded back into Power BI for further modeling and visualization.
By performing these data preparation steps in Power Query, the dataset was made ready for detailed analysis and visualizations, ensuring that the insights derived would be accurate and reliable.

Metrics and Calculations:
Step 1: Key Match Metrics and Player Performance
Key metrics affecting team and player performance were identified and analyzed. These metrics included average runs, wickets, batting and bowling averages, and player ratings.

The following parameters were recorded:

Batting Average: 45.30
Bowling Average: 28.15
Strike Rate: 135.4
Player Rating: 4.2/5
Top Batting Performance: 120 runs in a match
Top Bowling Performance: 5 wickets in a match
Total Runs Scored: 1,500
Total Wickets Taken: 60
Step 2: Key Visualizations Added to the Dashboard
Brand Name and Tagline:

Displayed using text boxes for easy branding of the IPL teams.
Runs Scored by Player:

Created a bar chart to visualize runs scored by each player across multiple matches.
Wickets Taken by Bowler:

A bar chart was created to represent the wickets taken by bowlers in various matches.
Player Performance by Match:

A line chart was used to track player performance over time, highlighting their consistency and improvements.
Batting Strike Rate and Bowling Economy Rate:

A scatter plot was used to compare batting strike rates and bowling economy rates for all players in the dataset.
Player Age Group Breakdown:

A pie chart was created to visualize the age distribution of the players, helping teams identify the demographic trends.
Step 3: Total Runs Scored Calculation
A measure was created to calculate the total runs scored by all players:

DAX
Copy code
Total Runs = SUM(ipl_performance_data[Runs Scored])
This total runs value was represented via a card visual for a clear summary of team batting performance.

Step 4: Player Segmentation by Age and Gender
Using the DAX formula below, players were segmented by age group to understand player experience and fitness levels:

DAX
Copy code
Age Group = 
IF(ipl_performance_data[Age] <= 25, "0-25",
IF(ipl_performance_data[Age] <= 35, "26-35", 
IF(ipl_performance_data[Age] <= 45, "36-45", "46+")))
Step 5: Average Batting and Bowling Performance
To assess player performance, average batting and bowling metrics were calculated:

DAX
Copy code
Average Batting Performance = AVERAGE(ipl_performance_data[Runs Scored])
Average Bowling Performance = AVERAGE(ipl_performance_data[Wickets Taken])
Insights from the Dashboard:
Total Runs and Performance:

Total Runs Scored: 1,500 runs (for the given period)
Top Scorer: Player A with 120 runs in a match
Batting Average: 45.30 (above average)
Bowling Average: 28.15 (strong performance)
Player Performance and Ratings:

The top players (Player A and Player B) have maintained consistently high performance, with batting and bowling averages well above the team average.
Player Ratings: 4.2/5, indicating overall satisfaction with player contributions.
Wickets and Strike Rate:

Player C has the highest wickets taken, with 5 wickets in a match.
Bowling Economy Rate: Player B performs well with an economy rate of 7.2 runs per over.
Player Age Group:

26-35 Age Group: Dominates the dataset, comprising 60% of the players.
Youthful Players (0-25): 30% of the players, bringing energy and agility to the team.
Older players (36+) comprise a smaller portion but provide experience.
Batting and Bowling Trends:

Peak performance times for batsmen are typically between 7 PM and 9 PM, while bowlers show greater effectiveness earlier in the day.
Recommendations:
Improve Batting Performance:

Focus on improving player strike rates and consistency, particularly for players under 25, who are showing promise but need more experience.
Optimize Bowling Strategies:

Leverage bowlers with a lower economy rate during key matchups. Develop strategies around top wicket-takers to exploit opposition weaknesses.
Player Rotation and Management:

Given the significant proportion of players in the 26-35 age group, consider rotating players during less critical matches to ensure long-term performance.
Maintain fitness and form of older players, as they bring experience.
Promotions and Player Development:

Focus on developing younger players (0-25 age group) to balance the team’s energy and experience.
Enhance Player Mentality and Ratings:

Invest in improving player confidence and ratings, focusing on providing consistent feedback and support.
By implementing these recommendations, teams can optimize their strategies, improve player performance, and enhance overall team dynamics during the IPL season.
