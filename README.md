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

According to the Centers for Disease Control and Prevention, the West Nile virus (WNV) is the leading mosquito-borne disease in the United States ([*Source: CDC, 2009*](https://www.cdc.gov/westnile/index.html)).It is most commonly spread to people by the bite of an infected mosquito. Cases of WNV occur during mosquito season, which starts in the summer and continues through fall. There are no vaccines to prevent or medications to treat WNV in people. Fortunately, most people infected with WNV do not feel sick. About 1 in 5 people who are infected develop a fever and other symptoms. About 1 out of 150 infected people develop a serious, sometimes fatal, illness. People can reduce their risk of WNV by using insect repellent and wearing long-sleeved shirts and long pants to prevent mosquito bites. This is essential as the medical costs can be outstanding especially if the disease progresses and causes neurological symptoms.

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
|ID|Int||Player's ID|
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

| Model| Train Accuracy|Test Accuracy|   Sensitivity | Baseline acc|True Pos |False Pos|False Neg|True Pos|
|:---------:|:---:|:--------:|:-------:|:----------:|:-----:|:----------:|:-----:|:-------:|
KNearest Neighbours|1.0|0.9476|0.0563|0.0539|5284|8|285|17|
Support Vector Machine|0.9471|0.9458|0.0033|0.0539|5290|8|301|1|
Logistic Regression|0.9488|0.9480|0.0762|0.0539|5280|12|279|23|
Random Forest| 0.9957|0.9544|0.4172|0.0539|5213|79|176|126|
Extra Trees| 0.9521|0.9097|0.6126|0.0539|4904|388|117|185|

### 6) Cost-Benefit Analysis and Executive Summary

**Executive summary**

Having evaluate five models for our classifier (i.e. KNN, SMV, Log Reg, Random Forest and Extra Trees), their respective scores are as such:

| Model| Train Accuracy|Test Accuracy|   Sensitivity | Baseline acc|True Pos |False Pos|False Neg|True Pos|
|:---------:|:---:|:--------:|:-------:|:----------:|:-----:|:----------:|:-----:|:-------:|
KNearest Neighbours|1.0|0.9476|0.0563|0.0539|5284|8|285|17|
Support Vector Machine|0.9471|0.9458|0.0033|0.0539|5290|8|301|1|
Logistic Regression|0.9488|0.9480|0.0762|0.0539|5280|12|279|23|
Random Forest| 0.9957|0.9544|0.4172|0.0539|5213|79|176|126|
Extra Trees| 0.9521|0.9097|0.6126|0.0539|4904|388|117|185|

As we are concerned about correctly identifying the presence of the West Nile Virus, we have predominantly used the test accuracy score to choose the best performing model. Notwithstanding this, we also looked at the sensitivity score so as to ensure that we keep our false positives to a minimum. Taking these two evaluation metrics into account, we observed that our Random Forest model is the most ideal (i.e. test accuracy of 0.9544 and sensitivity of 0.4172).

This goes to suggest that our model predicts 95.44% of the test observations correctly. Among obsevations that have the West Nile Virus, our model has 41.72% of them classified accurately.

Re cost-benefit analysis, our earlier paragraph shows that the cost of spraying the whole of Chicago fortnightly for 6 months (including the summer months) will cost about $2.8mil. This is far lower that the total estimated hospitalisation costs (see figures under "Chicago Mean Cost" from table above) from West Nile Virus and demonstrates a clear impetus for the city of Chicago to spray insecticide city-wide to reduce the spread of the virus.
