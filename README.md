# kickstarter_analysis

# Crowdfunding Analysis for Louise

## Overview of Project

### Louise is an up and coming playwright who wants to start a Crowdfunding campaign to fund her own play, *Fever*. She has never done a fundraiser through Crowdfunding and is hesistant of where to start. This is where the data analysts' job comes in; to analyze data of past Crowdfunding campaigns to glean from the data which factors of a campaign are often successful and give Louise recommendations of what to consider in her future campaign.

### The purpose of this analysis was to look closely into the relationship of the outcomes (failed, successful, or canceled) based on the launch dates of the campaigns and then again based on the goals of the campaigns. This deep dive and analysis of the data will provide Louise with relevant information to help her move forward more productively in her own Crowdfunding campaigns based off which past parameters were more and less successful. This project used Excel functions and Excel graphing techniques to organize, comb through, and analyze the data statistically and create visualization of the data in the form of graphs.

## Analysis and Challenges

### Outcomes Based on Launch Dates

#### First to analyze this data for outcomes based on launch dates, the year of each campaign was extracted from the Date Created Conversion column using the YEAR() Excel function to create a new column of data. A pivot table was then created from the worksheet and designed to show the canceled, failed, and successful campaigns as well as the grand total in columns. Parent category and years were set as the filters. The pivot table was filtered to show each month and how many campaigns were in each category for that month. The data was filtered to only show theater campaigns as these were the most successful overall and therefore the focus for Louise. A line chart was created from this pivot table to show a clear visualization and is shown below:

#### 
![Theatre_Outcomes_vs_Launch.png](/Theatre_Outcomes_vs_Launch.png)

#### May was the most successful month by a significant margin. February and October are close together for the second and third more successful months. Interestingly, October also shows a spike in failed campaigns. However, the failed outcomes do not have much variation between different months especially when compared to the variation of the successful campaigns, which varies the most per month. The canceled campaigns hold a consistent level throughout the months, with October being the only month to have zero.

### Outcomes Based on Goals

#### The next analysis of this data was the outcomes (successful, failed, canceled) versus the goal (the amount of money hoped to be raised). To extract these data points from the larger data set, the COUNTIFS() Excel function was utilized and a chart was created in a new data sheet. Again, this was to specifically analyze the ‘plays’ subcategory data, so a COUNTIFS() function was created for that filter as well. A line graph was created to visualize these findings:

####
![Outcomes_vs_Goals.png](/Outcomes_vs_Goals.png)

#### The graph shows that for the campaigns under $15000, there were more successful campaigns than failed. Once the threshold of $15000 was passed, where the successful and failed campaigns converge to the same amount, the percentage failed rises above the successful. This inverts again between the ranges of $35000-$44999, and then the failed campaigns spike while the successful campaigns plummet for the goal of $45000. This campaign goal range is the only to have no successful campaigns.

## Challenges

### A challenge I encountered when analyzing the outcomes based on goals was filtering the large data set from the ‘Kickstarter’ sheet to only show the results for the ‘plays’ subcategory. I used the Excel filter feature to filter the data set for ‘plays’ but when extracting the data using the COUNTIFS() function all of the results for each subcategory was shown. I overcame this difficulty by using an additional COUNTIFS() function to isolate the ‘plays’ subcategory data and resulted in a correct graph! I now understand that the COUNTIFS() function can be nested within multiple COUNTIFS() to isolate only the data being analyzed. I also had a couple typos in the COUNTIFS() function the first time I entered all of them; there are so many functions with small modifications it is important to be diligent when entering each one.

## Results

### In conclusion, I recommend May as the most profitable month to run a Kickstarter campaign. The second month I recommend is June followed by July. In short, campaigns in the spring and early summer have the best chances of success; most likely due to people being more active and willing to go out than in the winter. I recommend against running campaigns in the winter, specifically November, December, and January as these have the lowest numbers of successful campaigns. 

### I recommend Louise sets her goal for the campaign <$15,000. Based on the Outcomes versus Goals line chart, there are consistently more successful than failed campaigns when the goal is set under this amount. Given that Louise’s estimated budget for her play is $10,000+ this will still allow her to reach her goals. This sets a reasonable goal that is likely to be achieved. As the goal amount continues to increase all the way up to $50,000, the likelihood of the campaign failing becomes higher. 

### My recommendations are drawn from the data given which does have inherent limitations. This will be Louise’s first campaign and it is unknown how many campaigns the people that provided this data have run before, so Louise could run into unforeseen challenges herself that could impact her results. It would be more accurate if the data set only included campaigns that were run by someone for the first time. The data is also self-reported and could have some misleading or incorrectly reported data points. I recommend additional analysis of the Backers Count to understand how having a backer (or several) affects the outcome of the campaign. A pivot chart and bar graph of this analysis would show a clear visualization. I also recommend analyzing the average donation for the ‘plays’ subcategory to understand how much is being donated per person and then how many people Louise should aim to invite to her campaign. An additional work sheet extracting this data using Excel COUNTIFS() function and the AVERAGE() function could be used to extract this amount. 
