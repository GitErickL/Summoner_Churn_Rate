# Summoner_Churn_Rate

The purpose of this project is to analyze play rates and churn rates of League of Legends (LoL) players. I will refer to LoL players as summoners. 

I utilize a Python library called riotwatcher which is used to requeset data from Riot's API. I acquire 144 summoners' data of the times of each of their games played from June 18th, 2021 to May 26, 2022. 

I realize that this is not a lot of summoners to do analysis on, but acquiring the data proved to be quite time-consuming and I leave gathering larger amounts of data for a future project. However since I acquire each game these summoneres played over the span of about 11 months, I acquired data on about 80,000 games.

The main notebook which covers the data analysis is Lol_Player_Churn_Rate_Analysis.ipynb and is split up into 5 sections. The first two are explorations of the variable $\Delta t$, which is defined as the time difference between the start of a game and then end of the previous one. It's essentially the time between games. 

The next part of the notebook is the data analysis portion which covers:

1. **The average number of games played per day as a function of time** and how LoL community events influence these play rates. I also perform time series decomposition on this data and found that the LoL 2021 world championship (Worlds 2021) had  positive influence on the average number of games played per day.  

2. Final game played by summoners as a function of time. This sesction analyzes which players have churned or are almost churning. I define a player as **churned** if the date of their last game played is at least 2 months before the final date of which we attempted to acquire data of games played by that summoner. Similarly, a player has **almost churned**, if the date of their last game they played is between 1 month and 2 months before the final date of which we attempted to acquire data of games played by that summoner. We found that about 15% of summoners churned, and about 3% almost churned.


3. **Number of games played per session as a function of time** for summoners who churned or almost churned. I find that for many of these players, they were playing less games per session nearing the date of their final game played.


The code I used to acquire summoner data is not shown as it is not the point of this project and would clutter this repo, however, I'm happy to share it upon request. The future goals for this project are many and are listed in the analysis notebook as it goes along.

