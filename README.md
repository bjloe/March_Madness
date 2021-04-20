# March Madness, Kendall's Tau, ROC Curves, and Machine Learning

## Background

My wife and I were watching the first weekend of the NCAA Division 1 Basketball Tournaments, switching back and forth between the men 
and the women. My wife asked, "Doesn't it seem like we're watching teams from the same schools?" We wondered whether it was the case that when 
a school has a strong men's team, does it have a strong women's team too?  

What does the data say?

## Data

I started thinking about the **strength** of basketball programs and how they were related. I went to [Massey Ratings](https://www.masseyratings.com). 
Ken Massey has rated sports teams for a long time, and he produces ratings for teams in a wide variety sports at many levels of competition. This 
data gives us a starting point in part because it lists all Division 1 teams for men and women as well as giving an objective measure of team 
strength. In one notebook we use the rating as a way ranking teams. In the other notebook we use the ratings directly.

Note: There is more data at [this Kaggle site](https://www.kaggle.com/andrewsundberg/college-basketball-dataset) and [this one too](https://www.kaggle.com/c/ncaam-march-mania-2021).

## Statistics

There are a couple of ways to think about the "relatedness" of men's and women's programs. One is their rating, in this case the Massey Rating. Another 
way is to just look at whether a team has made the tournament.  One Jupyter Notebook investigates the former using 
[Kendall's rank correlation](https://en.wikipedia.org/wiki/Kendall_rank_correlation_coefficient) which is usually denoted by the Greek letter tau. 
The other notebook tries to predict tournament appearances by men's and women's teams based on their Massey Rating.

## Notes on downloading the data and loading into pandas

Once you navigate to the ratings pages (click [here](https://www.masseyratings.com/cb/ncaa-d1/ratings) for the men 
and [here](https://www.masseyratings.com/cbw/ncaa-d1/ratings) for the women), you can select "Export" from the button labeled "More". 
The data is included in this repository in the files Massey_men_d1.csv and Massey_women_d1.csv. 
_I have not modified the CSV files after I downloaded them._ The website puts two numbers in some columns; so there will be unnamed 
columns if you import the whole CSV file into a pandas dataframe.

I created a couple of CSV files listing teams that got tournament bids. These lists had to be edited to make sure that the team names matched.
