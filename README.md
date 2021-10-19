# An Analysis of Kickstarter Campaigns

## Overview of Project
Data on over 4,000 kickstarters have been collected to visualize & analyze multiple kickstarter campaigns based on varying criteria. The purpose of this analysis is to identify & compare any existing trends on specific outcomes of Kickstarter with a focus on launch dates & thier funding goals. Analysis has a central focus on **Theater Kickstarters** and will serve as informational insight for Louise's Project. 

## Analysis and Challenges

*Challenges and Difficulties Encountered
* We choose to begin the analysis by organizing & visualizing results of Outcomes for Theater related Kickstarters based on Launch Dates. By filtering our Kickstarter list to focus on Theaters, we use Excel to created a pivot table quantifying a count of all successful, failed, & canceled outcomes per month of the year. The pivot table seen below, gives us clear numerical comparison of grand totals for each outcome & each month. 
* The base of this pivot table used the formulas & functions listed to restructure the raw data provided ("x" represents value of any given cell):
1. Convert Launch Date Unix timesamps  :arrow_right:  "=(((**x**/60)/60)24)+DATE(1970,1,1)"
2. Pull year values  :arrow_right:  "=YEAR(**x**)"

<img width="475" alt="Pivot Chart Outcomes vs Launch dates" src="https://user-images.githubusercontent.com/91990957/137817815-6b0edc2f-f8e4-45ce-b2be-c279a6b31b94.png">

Connected to our pivot table is a Line graph visualizing these results using each month of the year as the X-axis & measuring count of each outcome on the y-axis. 

![line graph of theater outcomes](https://user-images.githubusercontent.com/91990957/137605662-d7bfeba5-b57d-498b-ab41-33a230b918ac.png)

No immidiate challenges encountered during this portion of the analysis.  


* Our next visulization details a closer look at Theater Kickstarter with **Plays** as a subcategory, and compares a percentage count of the successful, failed or canceled Outcomes in regards to their Funding Goals. Using Excel to extract a subcategory data column, we filter for Kickstarter plays and create a count of projects per outcome & confining this percentage count into Goal Funding Intervals. 
* With the use of Nesting Conditions in Excel, we used the below formulas & functions to extract & format this information from raw data ("x" represents value of any given cell):
1.  CountIFs function with multiple criteria  :arrow_right:  "=COUNTIFS(Kickstarter!$D:$D,">=**MIN RANGE VALUE**", Kickstarter!$D:$D, "<=**MAX RANGE VALUE**", Kickstarter!$F:$F,"**SPECIFIED OUTCOME**", Kickstarter!$R:$R, "**PLAYS**")
2.  Sumation of values within  range of a Row   :arrow_right:  "=SUM(**x**:**y**)"
3.  Percentage of Outcome total out of Total Project count    :arrow_right:   "=ROUND(**x**/(**total project value**) * 100,0)"

With these newly formated data we can create a line graph visualizing our Goal Funding intervals as the x-axis & Play Outcome Percentage for the y-axis.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/91990957/137822089-056062e3-07ab-4fe2-872c-46b15f272af0.png)

Challenges that arose during this portion of the analysis included:
* Proper placement of range values while nesting multiple criteria within the CountIFs function 
    * Solution!:key:  AskBCS LA provided clarity with an example of a successful formula that did not specify placement of range value within the formula (Thanks Susan! :wink: )
*   Formulating Percentage value to display "%" as unit of measurement. 
    * Unresolved:hole: I was not able to find a solution to this issue. Instead I rounded the value to the nearest whole integer & used the decrease decimal ability to format the values presented. 
    
    
### Results
* 2 conclusions about Theater Outcomes Based on Launch Date
* 1 conclusion about Outcomes based on Goals
* what are some limitations of the dataset 
* recommendations for other tables & graphs to create. 


* , but please note this is an vizualization of results from the Parent Category 1369 "Theaters" while our next visualization focus' on a Subcategory containing a rough 77% of data within the Parent Category.  

Feedback: May & June are peak months for launching a Campaign. There is also a strong correlation between Failed Campaigns & high-cost requests for funding.
Performing analysis on Kickstarter data to uncover trends for Louise's Project. 
