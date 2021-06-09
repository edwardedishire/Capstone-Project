# Capstone Project
GA Capstone Project - Edward Koh

### 1) Problem Statement

I am the sporting director of General Assembly Football Club (GAFC). My main role is to recruit players which suits the profile of my football club to strengthen the current squad so as to achieve better results going forward.

The transfer market have been very busy all the time, with many players changing clubs constantly. There are many possible reasons for a player to seek a transfer elsewhere; more game time, playing for a more reputable club/league, higher wages etc. It is pretty common for players to play for as many as 6 clubs during their playing career compared the past whereby players usually stick to about 3 clubs throughout their career.

In the midst of these transfer frenzy between clubs and players, certain problems arises. Firstly, players' transfer fees are greatly inflated these days as clubs get richer mainly due to  (1) massive injection in capital from recent high profile takeovers by rich businesssmen, and (2) increased broadcasting revenue. Back then, a 35 million transfer fee would be deemed as a marquee signing. However, in recent times, a transfer of that value would be deemed as a normality as the top players in game are worth easily over 70 million.

In addition, many clubs tend to make impulse purchases, leading to many transfer being deemed as flops. It is important to consider the various characteristics and traits of a player and assess his suitability before making purchasing. Many clubs overlooked that and there is new pattern of buying players that are more well known and hyped up by the media. This leads to severe consequences as many clubs end up paying a hugely inflated transfer fee for a players that does not suit the clubs' needs. More often than not, the new purchase will most likely have a disappointing season and be deemed as a flop or failed transfer. As such, it deals a huge blow to the financials of football clubs especially the smaller ones which do not have much budget to spare with regards to transfers.

Therefore, this project aims to resolve the issues above by:

(1) Creating a regression model which correctly predicts a player's transfer value based on various features. The success metric would be accuracy. I am looking to find out how a change in certain variables can affect the change in players' value.

(2) Building a recommender system to filter out players which we can share with our scouting department to aid them in finding the right players for the club at the right price. It is also crucial to make sure departing key players are properly replaced with similar players. (eg. we need a clinical striker, with fantastic finishing and speed, preferably ard the range of 30-50 million).

The target audience for this project involves anyone associated with talent recruitment and scouting for footballers.

### 2) Background

Football, also known soccer in US and Canada, is a well renowned sport with 4 billion fans worldwide. It is particularly popular in Europe, South America and Africa. One reason for its popularity is due to its accessibility. To play football one only requires a football unlike other sports like golf where the equipments can be very costly. Hence, this sport can be played by both the poor and rich. 

Since the past decade, famous video gaming creators EA Sports has been coming out with yearly video game versions of football titled "FIFA" followed by the year. In the game, all players are rated based on real life performances and the ratings are updated weekly. Each player has an "overall score" which is determined by the player's attribute score for this particular position. The game also lists the players estimated transfer value based on real life transfer prices along with other features like the wages and nationality. Hence, this game is very realistic as it relates very closely to the real life situation.

Therefore, for this project, i will be using the FIFA19 dataset on kaggle. It has data on 18207 players with 89 different features.

### 3) Data Dictionary

ID                            int64
Name                         object
Age                           int64
Nationality                  object
Overall                       int64
Potential                     int64
Club                         object
Value (€ Mil)               float64
Wage                        float64
Preferred Foot               object
International Reputation    float64
Weak Foot                   float64
Skill Moves                 float64
Work Rate                    object
Body Type                    object
Position                     object
Contract Expiration          object
Height                       object
Weight                       object
Crossing                    float64
Finishing                   float64
HeadingAccuracy             float64
ShortPassing                float64
Volleys                     float64
Dribbling                   float64
Curve                       float64
FKAccuracy                  float64
LongPassing                 float64
BallControl                 float64
Acceleration                float64
SprintSpeed                 float64
Agility                     float64
Reactions                   float64
Balance                     float64
ShotPower                   float64
Jumping                     float64
Stamina                     float64
Strength                    float64
LongShots                   float64
Aggression                  float64
Interceptions               float64
Positioning                 float64
Vision                      float64
Penalties                   float64
Composure                   float64
Marking                     float64
StandingTackle              float64
SlidingTackle               float64
GKDiving                    float64
GKHandling                  float64
GKKicking                   float64
GKPositioning               float64
GKReflexes                  float64
General Position             object

|Feature|Type|Dataset|Description|
|---|---|---|---|
|ID|Int|fifa19.csv|Player's ID|
|Name|String|fifa19.csv|Player's Name|
|Age|Integer|fifa19.csv|Player's Age|
|Nationality|String|fifa19.csv|Player's Nationality|
|Overall|Integer|fifa19.csv|Player's Overall Score|
|Potential|Integer|fifa19.csv|Player's Potential|
|Club|String|fifa19.csv|Player's Club|
|Value (€ Mil)|Float|fifa19.csv|Player's Value in € Millions|
|Wage|Float|fifa19.csv|Player's Wages|
|Preferred Foot|String|fifa19.csv|Player's Preferred Foot|
|International Reputation|Float|fifa19.csv|Player's International Reputation (1-5)|
|Weak Foot|Float|fifa19.csv|Player's Weak Foot Capabilities (1-5)|
|Skill Moves|Float|fifa19.csv|Player's Skill Moves Rating (1-5)|
|Work Rate|String|fifa19.csv|Player's Work Rate (High/Medium/Low)|
|Body Type|String|fifa19.csv|Player's Body Type|
|Position|String|fifa19.csv|Player's Position|
|Contract Expiration|Float|fifa19.csv|Player's Year of Contract Expiration|
|Height|Object|fifa19.csv|Player's Height in Inches|
|Weight|Object|fifa19.csv|Player's Weight in Pounds|
|Crossing|Float|fifa19.csv|Player's Crossing Score|
|Finishing|Float|fifa19.csv|Player's Finishing Score|
|Heading Accuracy|Float|fifa19.csv|Player's Heading Accuracy Score|
|Short Passing |Float|fifa19.csv|Player's Short Passing Score|
|Volleys|Float|fifa19.csv|Player's Volley Score|
|Dribbling|Float|fifa19.csv|Player's Dribbling Score|
|Curve|Float|fifa19.csv|Player's Curve Score|
|FK Accuracy|Float|fifa19.csv|Player's Free Kick Accuracy Score|
|Long Passing|Float|fifa19.csv|Player's Long Passing Score|
|Ball Control|Float|fifa19.csv|Player's Ball Control Score|
|Acceleration|Float|fifa19.csv|Player's Acceleration Score|
|Sprint Speed|Float|fifa19.csv|Player's Sprint Speed Score|
|Agility|Float|fifa19.csv|Player's Agility Score|
|Reactions |Float|fifa19.csv|Player's Reactions Score|
|Balance|Float|fifa19.csv|Player's Balance Score|
|Shot Power|Float|fifa19.csv|Player's Shot Power Score|
|Jumping|Float|fifa19.csv|Player's Jumping Score|
|Stamina|Float|fifa19.csv|Player's Stamina|
|Strength|Float|fifa19.csv|Player's Strength|
|Long Shots |Float|fifa19.csv|Player's Long Shots Score|
|Aggression|Float|fifa19.csv|Player's Aggresion Score|
|Interceptions|Float|fifa19.csv|Player's Interceptions Score|
|Positioning|Float|fifa19.csv|Player's Positioning Score|
|Vision|Float|fifa19.csv|Player's Vision Score|
|Penalties|Float|fifa19.csv|Player's Penalty Score|
|Composure|Float|fifa19.csv|Player's Composure Score|
|Marking|Float|fifa19.csv|Player's Marking Score|
|Standing Tackle|Float|fifa19.csv|Player's Standing Tackle Score|
|Sliding Tackle|Float|fifa19.csv|Player's Sliding Tackle Score|
|GK Diving|Float|fifa19.csv|Player's Goalkeeper Diving Score|
|GK Handling|Float|fifa19.csv|Player's Goalkeeper Handling Score|
|GK Kicking|Float|fifa19.csv|Player's Goalkeeper Kicking Score|
|GK Positioning|Float|fifa19.csv|Player's Goalkeeper Positioning Score|
|GK Reflexes|Float|fifa19.csv|Player's Goalkeeper Reflexes Score|
|General Position|String|fifa19.csv|Player's General Position (ATT/MID/DEF/GK)|
|Main Position|Float|fifa19.csv|Player's Simplified Position|

### 4) Notebooks
1) Notebook (1): Data Cleaning and EDA
2) Notebook (2): Modelling
1) Notebook (3): Recommender System

### 5) Modelling Summary

**Summary table for Models**

**Raw Dataset**

| Model| Train Accuracy|Test Accuracy|Variance|Cross Validation Score|
|:---------:|:---:|:--------:|:-------:|:----------:|
Linear Regression|0.8776|-1.110|1.9876|-2.9315|
Lasso Regression|0.8776|0.8348|0.04285|0.8435|
Ridge Regression|0.8733|0.8347|0.03855|0.8423|
Random Forest Regression|0.9967|0.9804|0.01629|0.9719|

**Clean Dataset**

| Model| Train Accuracy|Test Accuracy|Variance|Cross Validation Score|
|:---------:|:---:|:--------:|:-------:|:----------:|:-----:|
Linear Regression|0.8417|-2.3443|3.1862|-6.9552|
Lasso Regression|0.8407|0.8420|0.001291|0.8114|
Ridge Regression|0.8398|0.8430|0.003259|0.8102|
Random Forest Regression|0.9945|0.9725|0.02197|0.9601|

### 6) Conclusion and Executive Summary

**Executive summary**

Having evaluate five models for our classifier (i.e. KNN, SMV, Log Reg, Random Forest and Extra Trees), their respective scores are as such:

| Model| Train Accuracy|Test Accuracy|   Sensitivity | Baseline acc|True Pos |False Pos|False Neg|True Pos|
|:---------:|:---:|:--------:|:-------:|:----------:|:-----:|:----------:|:-----:|:-------:|
Random Forest Regression|0.9946|0.9731|0.02139|0.9604|

As we are concerned about correctly predicting a player's transfer value, we have predominantly used the test accuracy score to choose the best performing model. Notwithstanding this, we also looked at the variance and cross validation score so as to ensure that our model does well on unseen data along with a low possibility of under or overfitting. Taking these evaluation metrics into account, we observed that our Random Forest model is the most ideal (as shown in the table above). This goes to suggest that our model predicts 97.31% of the test observations correctly.

Our model also lists out the importance features that highly co-relates to a player's value. Not surprisingly, the feature with the highest corelation with value is the player's overall score, followed by potential.
