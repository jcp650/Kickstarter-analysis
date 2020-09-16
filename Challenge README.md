# Kickstarting with Excel

## Project Overview
This project compares the client's Kickstarter campaign for the play *Fever*, with related Kickstarter campaigns in Great Britain. The client launched a Kickstarter campaign to raise funds for this play, and is nearly succesful in reaching the $4,000 goal.

### Purpose
Comparing the performance of the Kickstarter campaign for *Fever* with other campaigns will provide insight into how the client's campaign performed in relation to other campaigns for plays in Great Britain. This analysis will provide useful metrics for gauging the success of the *Fever* campaign while informing the launch and structure of future campaigns. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To analyze the success of Kickstarter campaigns for plays, it is crucial to find the most effective launch date. The provided Kickstarter data contained launch dates in Unix timestamp format, which was converted in Excel using this equation:
```
=(((timestamp/60)/60)/24)+DATE(1970,1,1)
```
The Unix timestamp was divided by 60 (for seconds), then 60 (for minutes), then 24 (for hours), and was then added to the Unix epoch of January 1st, 1970. This number was then converted to the date format in Excel, which appeared as:
```
Month/Day/Year Hours:Minutes
```
After filling this conversion throughout all rows in the data set, a pivot table was created to create a subset of relevant launch date information. The pivot table filtered on the parent category and years variables, with outcomes (excluding live campaigns) as the column varaible, launch date conversion as the row variable, and count of outcomes as the value. Next, the rows were grouped by month instead of date to provide optimized visualization for the best time to launch. With this information, a graph was created to visualize the outcomes of Kickstarter campaigns based on their launch date (figure 1).

### Figure 1
![](Resources/Theater_Outcomes_vs_Launch.png)

Figure 1 shows that May has the most successful launches while October has the most the most failed launches. In other words, campaigns launched after May tend to be less successful. Figure 1 decidedly demonstrates that May is the best time to launch a Kickstarter campaign for theater. 
