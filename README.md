# March Madness, Kendall's Tau, and Conditional Probability

We were watching the first weekend of the NCAA Division 1 Basketball Tournaments, switching back and forth between the men 
and the women. My wife asked, "Doesn't it seem like we're watching teams from the same schools. If a school has a strong
men's team, does it usually have a strong women's team too?"

I took that as a challenge!

My calculus teacher used to say, "When you have a problem, ask yourself what do you know and what are you trying to find out." 
So what do we know? Or what data do we have? How should we measure the strength of a program?

I started out thinking about the **strength** of programs and went to [Massey Ratings](https://www.masseyratings.com). Ken Massey started 
this site a long time ago, and he produces ratings for teams in many different sports at a variety of levels of competition. This 
gives us a starting point, because this site lists all Division 1 teams for men and women. Once you navigate to the ratings pages (click
[here](https://www.masseyratings.com/cb/ncaa-d1/ratings) for the men and [here](https://www.masseyratings.com/cbw/ncaa-d1/ratings) 
for the women), you can select "Export" from the button labeled "More".  The data is included in this repository in the files Massey_men_d1.csv 
and Massey_women_d1.csv. _I have not modified the CSV files after I downloaded them._ 

The Jupyter notebook in this repository loads the data from the CSV files, only importing the team Name and Rating. Massey Ratings puts two 
numbers in some columns; so there will be unnamed columns if you import the whole CSV file into a pandas dataframe.
