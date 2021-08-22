# An Analysis of Kickstarter Campaigns

## Overview of Project

The project will focus on using our newly acquired excel skills in a realistic data analysis scenario.

### Purpose

We have been tasked to provide an analysis for Louise, an up-and-coming playwriter, who recently came close to her crowdfunded goal for the play "Fever". Her budget was for $10,000 and her goal was met in a short amount of time. Louise wants to know how different campaigns fared in relation to their launch dates and their funding goals.

To provide Louise with our assessment, we will be applying the concepts learned in Module 1 in order to derive insights on other campaigns.

## Analysis and Challenges

We have been provided data for kickstarter campaigns covering several years and categories. Using excel and its suite of analytical tools, we have been able to filter, sort and present the data to derive meaningful insights that Louise can utilize in better understanding how her campaign fared compared to other campaigns.

The dataset comprises 4,114 unique campaigns, of which 1,066 correspond to plays. Of this later subset, our analysis excluded campaigns which are still live, since their outcome is not known at this time. The final dataset analyzed focused on the remaining 1,047 campaigns which were either successful, failed or had to be canceled. The selection of this subset was done using filters and conditional statements in excel.

In wanting to know how campaigns fared in relation to launch dates and funding goals, Loise is focusing on two criteria for likely success: 

- when is the best time to launch a campaign? 
- what funding goal should be targeted?

### Analysis of Outcomes Based on Launch Date

To answer the first criteria, we created a pivot table to organize the data by month, with filters for parent category ("plays" subcategory falls within the "theaters" parent category) and years.

The result of this analysis is summarized in the chart that follows.

https://github.com/IJG-DR/kickstarter-analysis/blob/58a6a9999e377c4844b6f2fe49009f8f508c69bc/resources/Theater_Outcomes_vs_Launch.png

As a note, we also added a filter for subcategory to the pivot table, discriminating only for "plays" and found that this subcategory follows the same trends as that for the "theater" parent category.

### Analysis of Outcomes Based on Goals

To answer the second criteria regarding the optimal funding goal, we extracted data only for the "plays" subcategory and organized the subset by ranges of funding amount in roughly $5,000 increments. This was achieved by creating a table using excel's COUNTIFS() function. The information extracted in this manner is presented in the following chart.

https://github.com/IJG-DR/kickstarter-analysis/blob/58a6a9999e377c4844b6f2fe49009f8f508c69bc/resources/Outcomes_vs_Goals.png

### Challenges and Difficulties Encountered

#### Cleaning, organizing and filtering the data

Several of the challenges encountered were first, organizing and cleaning the data to make it easier to analyze. This entailed creating filtered columns, freezing panes, converting data to useable date formats, segregating categories into parent categories and subcategories as well as creating a year field for easier filtering.

Since Louise's project falls under the "theater" parent category and "play" subcategory, we filtered the data to focus our analysis on this relevant subset. This was done with pivot tables and COUNTIFS() excel formulas.

## Results

### Conclusions based on Launch Date

Three conclusions that can be drawn from the data based on Launch Date Outcomes are:

1) Summer is the time when most campaigns launched tend to have a successful outcome, with the month of May being the month most likely to produce successful results.

2) It is also the time of the year when most campaigns are launched (35% of total yearly campaigns), which means any campaign launched at this time will have more campaigns to compete with. Therefore, the showcase presentation for the campaign will need to be catchy in order to stand-out.

3) There have been very few campaigns launched either before 2014 or after 2016, which may indicate that play campaigns may have followed a trend or fad. The data does not provide sufficient insight to reach a definitive conclusion on why that is so.

### Conclusions based on Launch Goals

As to our analysis of campaigns based on funding goals, we could draw the following conclusions:

1) Campaigns with goals of less than $5,000 seem to have higher rates of success, with roughly 73%-76% of them succeeding, while campaigns in Louise's target of $10,000 seem to have about an even chance to succeed or fail.

2) It is also relevant to point out that 85% of all Kickstarter campaigns for crowdfunded plays have goals of less than $10,000, with few above that amount. Louise's budget was therefore on the high end in terms of funding goal.

### Dataset Limitations

The dataset has its limitations. Very few campaigns are reported before 2014 and after 2016. The causes may require further analysis. Is it that no-one had thought of using Kickstarter for plays before then? If so, what would explain the few campaigns after 2016? Was it a temporary fad? Without further analysis and data, we cannot draw any conclusion on whether a campaign's chances of success can rely solely on the dataset analyzed.

Also, for campaigns on the higher-end of the goal scale, the number of data points may not provide statistical significance if we were to focus on this subset alone.

### Further Analysis

Given that Louise's budget was on the high-end in terms of funding goal, with about even chances for success, it would be interesting to know what where the probabilities for this to happen. To determine that, we could have derived statistical summaries on the data and used several tools, like the quartiles box-and-whiskers chart and standard deviation analysis. Also, it is interesting that her funding goal was met in a short amount of time. We could also perform an analysis of successful campaigns based on duration from launch to finish, using the same excel tools (i.e. using duration instead of goal with a table created using the COUNTIFS() function).

