# KickStarter_Challenge

# Kickstarting with Excel

## Overview of Project

### Purpose
Louise wants to start crowdfunding for her play write. She is estimating a budget of $10,000.By performing data analysis on several thousand crowdfunding projects, we can uncover hidden trends.
Now, Louise’s play Fever came close to its fundraising goal in a short amount of time. Now, she wants to know how different campaigns fared concerning their launch dates and their funding goals. Using the Kickstarter dataset that you’ve already combed through, you’ll visualize campaign outcomes based on their launch dates and their funding goals. 
## Analysis and Challenges
There are two types of Analysis we have done, "Outcomes based on Launch date" and "Outcomes based on goals".
### Analysis of Outcomes Based on Launch Date
First of all, I made sure that I have the right name for the file as well as for the worksheet. For analysis of "Outcomes based on Launch Date", I had to make a new column "Years"(by using the function =YEARS(Serial_number)) so I could extract the year from the "Date Created Conversion" column. Then I created a pivot table by setting "Outcomes" in the columns section, "Date Created Conversion" in the rows section, "Outcomes" in the values section, and filtering"Parent Category" and "Years".After making some alterations to the pivot table (filtering the column labels for "successful", "failed", "canceled" and theater category for "theator"), I created a line chart showing the number of successful, failed, or canceled projects by month. 

### Analysis of Outcomes Based on Goals
To visualize the percentage of successful, failed, and canceled plays based on the funding goal amount, I used the function called COUNTIFS. 

First I created a new sheet called "Outcomes Based on Goals".In this new sheet, I created the following columns,
Goal
Number Successful
Number Failed
Number Canceled
Total Projects
Percentage Successful
Percentage Failed
Percentage Canceled
Then I created different dollar amounts ranges in the "Goals" column. And finally, Used COUNTIFS function for to populate the "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges created in Step 3, and on the "Subcategory" column using "plays" as the criteria.

For Example, column "Number Successful", Cell B2 has "=COUNTIFS(Kickstarter!D:D,">=1000",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays",Kickstarter!D:D,"<=4999",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays")" as the COUNTIFS function. Look, how it only picked plays (subcaegory) that were successful for goal amount in between 1000 and 4999. 

Then I created the line chart to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis.
### Challenges and Difficulties Encountered
1) The first challenge I faced was not having the right Exel version for this assignment as pivot tables does not work very well in the old versions. So, I had to update Exel before I could do anything else. 
2)When I was creating "Date Created Conversion" and "Date Ended Conversion", I forgot to change the type of data from "general" to "Long Date format". I realized my mistake's effect when I made a pivot table for the data that how important it is to keep these small things in mind.
## Results

- What are two conclusions you can draw about the Outcomes-based on Launch Date?
By looking at the chart" Theater Outcomes Based on Launch Date" it is obvious that months through April to August have a high success rate.
- What can you conclude about the Outcomes based on Goals?
By looking at the line graph "Outcomes based on Goals", it is clear that for Louise to have a successful Campain, she should set her goal either be less than 5000 or between 35000 to 42000.
- What are some limitations of this dataset?
While doing our analysis, we did not take currency from different countries into the account. For example, there is a clear difference between pounds and dollars. There should be a column in the dataset converting different currencies into one, so we don't get errors while analyzing the data later on.
- What are some other possible tables and/or graphs that we could create?

Like I mentioned in the previous question, a currency conversion column is necessary for this data set.
Furthermore, we can also analyze other factors(i.e.countries) in the dataset that can also impact Louise's decision.
