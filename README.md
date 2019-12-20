# Basketball-Game-Prediction
We wanted to predict the winning team based on data studiously collected by a basketball fan and a former analyst for the Dodgers. 

The data is composed of 2 files. The first, train.csv, contains the variables described below as well as the outcome variable (HTWins). There are 218 variables and 9520 rows. The second, test.csv, contains all of the variables except the outcome variable. IT has 1648 rows. 

### CODEBOOK:

VT Visiting Team Name abbr
HT Home Team Name abbr

VTleague League of Visiting Team abbr
HTleague League of Home Team abbr

VTcumRest cumulative rest (travel, workouts, etc.) of VT
HTcumRest cumulative rest (travel, workouts, etc.) of HT

* The remainder of the variables are predicted/forecast values. They were produced by various types of time filters, including the "information filter" and Kalman Filter.
* there are many var names of the form "AA.BB.ccc", or the like. They fall into two main categories, Team-level variables, and Starting-Player-level variables.

Team variables
AA:
VT Visiting Team
HT Home Team

BB:
TS Team Scored
TA Team Allowed
OTS Opposing Team Scored
OTA Opposing Team Allowed

ccc:
(not all are included)
min Minutes
fgm Field Goals Made
fga Field Goals Attempted
tpm 3pt Shots Made
tpa 3pt Shots Attempted
fta Free Throws Attempted
ftm Free Throws Made
oreb Offensive Rebounds
dreb Defensive Rebounds
treb Team Rebounds
ast Assists
stl Steals
blk Blocked Shots
to Turn Overs
pf Personal Fouls
pts Total Points

Player variables

AA:
(same as team vars above)

BB:
S1 Starting Player position 1
S2 Starting Player position 2
S3 Starting Player position 3
S4 Starting Player position 4
S5 Starting Player position 5
OS1 Opposing Starting Player position 1
OS2 Opposing Starting Player position 2
OS3 Opposing Starting Player position 3
OS4 Opposing Starting Player position 4
OS5 Opposing Starting Player position 5

ccc:
(same as team vars above)

plmin Points plus/minus -- a general measure of how effective player is

The vars VT.pmxU, VT.pmxW, HT.pmxU and HT.pmxW are very complicated composites that attempt to express the offensive and defensive difficulty of past games for the VT and HT.


## Data Cleaning

* No missing values in both training and testing datasets. 

* However, we found some repetitive columns in the data when we went through. For example, we found values of “VT.TS.fga” are exactly the same as values of “HT.OTS.fga”. “VT.TS.fga” represents total ‘field goals attempted’ by the Visiting Team; and “HT.OTS.fga” represents total ‘field goals attempted’ by the Home Team’s opposing team, which is just VT. Therefore we removed all columns that has “.O” in it

* We also removed id, game id, date, in the training data and same for in test dataset. These variables are unique in each row and shouldn’t be significant indicators of the teams’ future game win or loss

## Adding New Variables

** pht




