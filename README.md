# Kickstarter Campaigns Analysis

## Overview of Project

### Purpose
This project consists of a dataset that includes information about multiple Kickstarter Campaigns and their performance over time. The data will be manipulated to generate insights into how different factors influence compaign outcomes. The goal of this project is to help Louise to understand how different campaigns fared in relation to their launch dates and their funding goals. 

## Analysis and Challenges

This analysis was performed by, after taking an initial look at the data, converting the columms that contained dates into a readable format, breaking down the Categories into Parent category and subcategory, extracting the year from the lanch date column, and defining the average donation and the percentage funded for each campaign.

After that, a pivot table was created to visualize the outcomes of the theater campaigns at each month of the years in the dataset, and a table was generated to define the percentage of successful, failed and canceled campaigns, based on the goal of each campaign.

### Analysis of Outcomes Based on Launch Date

The graph below shows how the campaigns performed according to their launch month:

![Figure 1. Theater Outcomes based on Launch Date](https://github.com/ericosabino/kickstarter-analysis/blob/main/resources/Theater_Outcomes_vs_Launch.png)


### Analysis of Outcomes Based on Goals

The graph below shows the percentage of each type of outcome (successful, failed and canceled) based on how much was the goal for each campaign:

![Figure 2. Outcomes based on Goals](https://github.com/ericosabino/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered

1. The Launch and Deadline dates were displayed in a Unix format, so it was needed to convert this columns into a readable format to be able to perform the analysis.

2. There was no information related to each goal of the campaigns, so a new table had to be created to perform this analysis using the COUNTIFS() formula to generate the graph of Outcomes Based on Goals.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

   1. May and June are the best months to launch a campaign, based on the performance of the campaigns listed on the dataset.
   2. December is the worst month to launch a campaign.

   Additional comments:
   - While the performance trends downwards starting in May, October broke the trend with 65 successful campaigns, compared to 59 in September and 54 in November.
   - There were no canceled campaigns in October, but the number of failed campaigns was 50, compared to 34 in the previous month and 31 in the following month.

- What can you conclude about the Outcomes based on Goals?

   1. The higher the goal, the higher the likelihood of the campaigns fail. With the exception of the range between 35000 and 45000, the percentage of failures is higher when campaigns have a goal higher than 20000.
   2. The most successful campaigns are the ones with goals under 5000, as more than 70% percent of the campaigns withing this range were successful.
   3. Campaigns with goals between 20000 and 35000, and above 45000 had the worst performance.


- What are some limitations of this dataset?

   1. The data provided contains information from campaigns created from May 2009 to March 2017, and ended from August 2009 to May 2017. This data may be old and may not reflect the same situation in the current year.

   2. There is no information about how many of the backers are still active, so it's unclear whether the campaigns to be launched in the future will have the same performance as in the past, as the backers base may be different. 

   3. The numbers of campaigns with goals above 15000 is much lower than campaigns with goals within lower ranges. There are 186 projects with a goal lesser than 1000, 534 with a goal from 1000 to 4999, 169 with a goal of 5000 to 9999, and 72 with a goal ranging from 10000 to 14999. The number of campaigns with a goal of 15000 and above range between 0 and 12, which add some bias to the analysis. If there were more campaigns within the range from 15000 and above, maybe we could come to different conclusions.

- What are some other possible tables and/or graphs that we could create?

   1. We can create a pivot table and a graph to validate the performance of campaigns based on the campaign duration. With that we could determine how long Louise's campaign should be.

   2. We can create a table to determine the performance by country and isolate the data in the graphs to analyze data only on the countries Louise wants to launch the campaign on.

   3. We can create a pivot table to validate performance by category so potential campaigns can be created in the future, if Louise decide to invest in other catgeories as well.

   4. We can create a boxplot to determine the outliers and remove them from the goals, and then analyze what's the impact on our current analysis, and whether make sense to keep the outliers.
