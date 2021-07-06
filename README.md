# Kickstarting with Excel

## Overview of Project

### This analysis is to display how relevant campaigns fared in relation to their launch dates and their funding goals. 
---
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
### ![image_name](https://github.com/PirateSuit/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png?raw=true)
I used =YEAR() to take the date from the "Date Created Conversion" column (R) we had made earlier. I then copied it down through all rows. I created a pivot table using the Parent Category and Years as filters, the Outcomes for the columns, the Date Created conversion as the Rows, deleting all but the month info. Then I put the Parent Category into the Values. Then I filtered the columns to show only Successful, Failed, and Canceled, and the Parent Category to only show Theater data. I sorted the Outcomes in descending order. Then I created the line chart and titled it and saved it.


### Analysis of Outcomes Based on Goals
![image_name](https://github.com/PirateSuit/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png?raw=true)
I created the Goal column and filled in the twelve rows below. Then I created the four rows displaying the numbers of successful, failed, and canceled campaigns, as well as one that totals these up. Then three more with the percentages of successful, failed, and canceled campaigns. I used the =COUNTIF() function to populate columns B,C,D, adjusting the number criteria to match the goal range.  
Here's an example: =COUNTIFS(Kickstarter!$E:$E,"Failed",Kickstarter!$Q:$Q, "plays",Kickstarter!$C:$C,">=1000",Kickstarter!$C:$C,"<=4999")

Then I used the SUM() function to populate column E with totals.  
Like so: =SUM(B2:D2)

Finally, I calculated the percentages for columns F,G,H by dividing the successful or failed or canceled projects in A,B,C, individually, by the total projects (column E), in that row.  
Like so:=(B2/E2)

Then I created a line chart by selecting columns A,F,G,H, and clicking the line chart button under the insert tab. I resized the chart, titled it, and saved it as a .png.
___


### Challenges and Difficulties Encountered
I was hung up on making the Outcomes Based on Goal graph for a little bit, as I couldn't recall how to make a graph directly from data without putting together a pivot chart first. But I jumped into the class recording and found the demonstration. A cinch, in the end!

Also, to be honest, I started writing this analysis as if it were to our imaginary client, Louise, before realizing you wanted me to actually describe my process. Oops. Let me know if my descriptions/overviews are too wordy or if you're looking for something different. Thanks!

---
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The amount of failures is much more consistent than the successes. This makes large increases in successes, such as in May and June, a clear indicator of a good time to launch a campaign. Conversely, the months from September to March are much less forgiving. Also, cancelled campaigns don't appear to make much of a statement.

- What can you conclude about the Outcomes based on Goals?

With the exception of the $30,000 - $50,000 range, it seems that the lower your goal, the higher your rate of success.

- What are some limitations of this dataset?

On the Outcomes Based on Launch Date graph, it would be beneficial for comparisons sake to display the exact number of results per category per month on points along the line and to perhaps display the percentage of the total of each the successes, failures, and cancellations.   

  On the Outcomes based on Goals chart, it would be helpful to show the amount of kickstarters per category, as they vary dramatically. in the $1,000 - $4,000 range, there are 534 total projects, compared to only 1 in both the $40,000 - $45,000 and $45,000 - $50,000 ranges. This makes those datapoints speak much louder on the graph than they ought to.
- What are some other possible tables and/or graphs that we could create?

We could put together a display to see if there was a correlation between the number of backers on a campaign with the likelihood of it's success. Or, perhaps one that compares average size of donation with success rate. Length of campaign could be something worthwhile as well. Finally, if Louise was already considering a production in Great Britain, we could search more countries to see which had the best chance of success based on these or other already discussed factors.
