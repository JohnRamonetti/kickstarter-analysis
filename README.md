# Analysis of Kickstarter Funding Campaigns

## Overview of Project

### Purpose:  The purpose herein was to determine what elements of a kickstarter campaign are most likely to lead to a successful fundraising campaign. Data was received and analyzed for several thousand crowdfunding projects to uncover any hidden trends, and specifically to determine how different campaigns fared in relation to their launch dates and their funding goals.  More specifically, we focused on theater, and specifically plays, because the funding of a play is the ultimate goal.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
####	The first chart prepared is a line graph showing the number of successful, failed and canceled kickstart theater campaigns by launch date (Theater Outcomes Based on Launch Date).  The data was tabulated and graphed in decending order (successful, failed, canceled) and filters were included in the PivotTable for both 'Parent category' and 'Years' so the data can be looked at and visualized more broadly (by other categories) or specifically (by year) if desired.

### Analysis of Outcomes Based on Goals
####	The second visualization is also a line graph [Outcomes Based on Goal](Resources/Outcomes_vs_Goals.png).  It shows the percentage of successful, failed and canceled funding campaigns for Plays based on the funding goal sought.  Interestingly, it illuminated that there were no canceled kickstarter campaigns in this subcategory.  Data was tabulated using a series of COUNTIFS() formulas, then percentages were calculated/tabulated as well. 

### Challenges and Difficulties Encountered
####	Like any large data set, this kickstarter data first had to be reviewed, organized and cleaned up.  Some simple formatting, conditional formatting, value shading, etc helped.  Dates were included as Unix timestamps, so they were all converted using '=(((J2/60)/60)/24)+DATE(1970,1,1)' and later, the year was also placed into a separate column to readily break down annual data.  Categories and subcategories were initially condensed and had to be split into 2 columns using the "Convert Text to Columns Wizard" to look at data within subcategories.  The biggest problem that we encountered was the limited size of the data sample within certain categories, which affects the ability to draw confident conclusions for certain segments of the data.  Some light debugging was done (IfError()).  Fortunately, our data set was organized well.  We could have experienced problems if the entries had lacked consistency within columns.

## Results

- Conclusions drawn about Outcomes based on Launch Date:
	The most significant conclusion that can be drawn from this data, based on Launch date, is that there is a clear peak for successful campaigns beginning in May, then gradually reducing through the remainder of the year.  The greatest number of successful kickstarter theater campaigns were those launched in May, followed by June, July and August.  
	A second conclusion is that, while the number of failed campaigns doesn't change dramatically through most of the year, December is clearly the month with the fewest successful campaigns launched, and the only month where the number of failed campaigns is virtually the same as the number of successful campaigns.

- Conclusions drawn about Outcomes based on Goals:
	From our "Outcomes Based on Goal" table and graph, we can clearly conclude that the greatest percentage of successful campaigns in the "Plays" subcategory are those campaigns with more modest goals.  Kickstarter campaigns with fundraising goals of $5,000 or less were successful 75% of the time, and those seeking up to $20,000 were successful about 50% of the time.  While there is much less data for larger campaigns, the failure rate for campaigns seeking $45,000 or more is around 90%.

- Limitations of this dataset?
	As mentioned above, there is not enough data from certain categories and subcategories to draw confident conclusions about certain segments of the data. For example, our data shows a 67% success rate for campaigns in the "Plays" subcategory attempting to raise $35,000 to $45,000, however this is based on a total of 9 campaigns in this goal range, versus a total of 720 campaigns seeking $5,000 or less.  

- Other possible tables and/or graphs that we could create:
	There are many other ways we can still review and evaluate this data.  For the current project, we might consider tabulating and/or graphing the correlation between campaign duration and success.  We might also look more closely to see where (i.e., in which countries) campaigns see the most success.  We can look at the data by year to see if the results vary year-to-year, or whether the annual patterns hold steadily.  And finally, we might look more broadly at categories and subcategories that don't have an intuitive correlation with plays, but that might render useful information when visualized.
