# Introduction

This directory contains a top level look at the results from the 2016 Hong Kong marathon. I used the dataset hosted at https://www.kaggle.com/melvincheung/hong-kong-marathon-2016. I was much more comfortable working within R, so this was my first for foray into Pandas as a primary replacement for native R data-frames.

# What I did

I started by performing simple manipulations on one of the two included csv's. This involved trimming the white space from the column names, converting the race times to timedelta format for further use, and creating a 'Gender' column derived from the race category of the participant.

In terms of descriptive statistics, I tabulated the athelete's country of origin, analyzed finish position by gender, binned finish time by gender by 15 minute interval, and binned finish time by race category.

I then calculated the average pace in the first and second half of the marathon to look at differences between them. On average, unsurprisingly, the second half was slower then the first. I then directly compared this difference in pace by gender and found that while both genders had a lagging second half marathon pace, women on average had a smaller difference. As a final look at the data, I then performed the same analysis, seperated by race category. Here, we see that MFI and MMI are the inferred elite group due to their runner count relative to other groups and their discipline in terms of difference in pace. The average man within this category ran 12.6 seconds slower in the second half and the average woman ran 4.3 seconds faster. This is in line with previous research that woman have better race discipline. While this article studies non-elite runners, measure of race displine by gender is reported here: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4289124/.

# Working with Pandas

As working within Pandas was one of the major learning goals of this analysis, here are my main takeways.

1. The timedate and timedelta format are very useful for this time of analysis. I still ran into issues manipulating the specific labelling.  
2. Column level changes are best handled by a lambda function. I take this for granted using R.  
3. While it is easy to add on additional data to plots, it does not appear to be as flexible as ggplot.  
4. The groupby function is powerful, but its resultant object is a bit more difficult to interact with then the data frame you're coming from.  

Cameron
