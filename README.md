# Basketball-Game-Prediction
This project asks you to predict the winning team based on data studiously collected by a basketball fan and a former analyst for the Dodgers. The team names and leagues have been disguised, and the dates removed so that you are forced to use the data, and not your knowledge of the outcomes, for the prediction. The response variable indicates whether, for a given game, the hometeam wins. Roughly 1600 games have been set aside, and you have been given "testing data" that you use to predict whether or not the hometeam wins in each game.

You are given three files. The first, train.csv, contains the variables described below as well as the outcome variable (HTWins). There are 218 variables and 9520 rows. The second, test.csv, contains all of the variables except the outcome variable. IT has 1648 rows. The third is a sample submission that indicates the format for your submission. Note that the ID numbers in your submission file must match the ID numbers in the test file.

CODEBOOK:
VT Visiting Team Name abbr
HT Home Team Name abbr

VTleague League of Visiting Team abbr
HTleague League of Home Team abbr

didHTwin in {0, 1}, did the home team win?

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

The vars

VT.pmxU
VT.pmxW
HT.pmxU
HT.pmxW

are very complicated composites that attempt to express the offensive and defensive difficulty of past games for the VT and HT
