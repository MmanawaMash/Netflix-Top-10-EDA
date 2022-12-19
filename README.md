# Netflix-Top-10-EDA

In this project, I was required to do an EDA on a datasetof my choice and then present the results of my analysis. I chose the Netflix Daily Top 10 from Kaggle. 

To facilitate the analysis, I made use of NumPy, pandas, Matplotlib, squarify, wordcloud and seaborn modules.

This project was one of the tasks I was required to complete for my Data Science Bootcamp with HyperionDev.

### Summary of the data set
NETFLIX DAILY TOP 10 2020 – 2022 (United States)
Over-the-top (OTT) media services have expanded in recent years. One of the top OTT services with the most subscribers and watchers is Netflix.
We can examine the audience and movie content thanks to Netflix's distribution of the daily Top 10 Movies and TV Shows for various weeks and days. 
The total number of days this program spent in the top 10—not necessarily in order—is displayed in the Days in Top 10 column. Each show receives a score based
on its historical daily rating, with 10 points awarded for each position one, 9 points for each position two, etc.

### DATA SOURCE: https://www.kaggle.com/code/bcruise/netflix-daily-top-10-eda/data

### DATA CLEANING

•	The date columns need to be changed from the object data type to datetime. The to.datetime() pandas function helps us do that. This will help us later analyse yearly data at a later stage  
•	In the dataset, there are missing values that are denoted with a "-". I will use the replace() function to replace the "-" with an np.nan so we are able to denote the missing values better
•	The Netflix exclusive column looks like it only has 'Yes' in it. The code below should show that there is no "No".

### MISSING DATA
•	In the dataset, there are missing values that are denoted with a "-". I will use the replace() function to replace the "-" with an np.nan so we are able to denote the missing values better
•	The Netflix exclusive column looks like it only has 'Yes' in it. The code below should show that there is no "No" – I replaced all the NaN values in this column with a “No” 
•	Drop the Last Week Rank because it has more than 50% data missing in it.
•	12 percent of the Year to Date Rank has missing values, we delete the Year to Date Rank column. This column will not be useful in our analysis.

### CONCLUSIONS

TV series are more likely than movies, stand-up comedy specials, and concerts to remain in the Top 10. This makes logical given that a TV season is longer to watch.

Ariana Grande's Excuse Me, I Love You was the only concert to appear in the Netflix Daily Top 10 from 2020 to 2022, spending two days there.

From 2020 to 2022, Dave Chappelle and Kevin Hart were the only two comedians to remain in the top 10 on Netflix for ten or more days.

Cocomelon TV Show, followed by "Ozark," spent the most days in the top 10 over the course of two years (428).

The only film to spend more than 30 days at the top of the charts was "Mitchells vs. The Machines."

The greatest performers in the TV programs category are Netflix Exclusive.

There are no stand-up comedy shows that are not Netflix-exclusive.

The Viewership Score increases with the Days In the Top 10 because it is the assigned to the show depending on what position in the Top 10 the show is on a day it is in the Top 10. This means Cocomelon and Ozark have the highest Viewership Scores.
