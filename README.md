## Starcraft Rank Predictor

### Objective
Given a dataset of Starcraft player performance data in ranked games, develop a model to predict a player’s rank using the information provided in the dataset.

### Observations
- Age is inversely proportional to LeagueIndex. This is true because Starcraft like othercompetitive e-sports require quick reflexes and it caps at around 24. The reflexes andmuscle memory develop much better at a younger age
- In order to stay in touch with the game, it is important to keep in touch. This wouldmean spending enough hours on the game every day. HoursPerWeek gives us thisinformation and it increases with higher leagues. Typically, Pro gamers spend almost 8hours a day
- TotalHours tells you how much experience the player has playing the game and it isdirectly proportional to being in higher leagues. TotalHours for league 5 does notappear to fall in line and it is discussed in the upcoming sections
- Starcraft is a multitasking game and all about managing the macro - keeping up a steadrate of income, expansions, proper buildings & upgrades. Being able to performmultiple actions in a short time is important and players capable of handling this will befound in higher leagues. APM (Actions per minute) shown in the above graph correlatesto this
- Using Hotkeys is vital in keeping up with the pace of the game. The time spent inmoving the cursor to click and perform an action is much higher than tapping a coupleof keys in the keyboard to perform the same action. Features SelectByHotkeys,AssignToHotkeys and UniqueHotkeys give this information and show that players inhigher leagues use more hotkeys
- Similar to using hotkeys, clicking on the minimap takes you to a location directly, rather
than scrolling and reaching to it. This also saves a lot of time and players in higher
leagues will have features such as MinimapAttacks and MinimapRightClicks higher than
players in lower leagues


### Conclusion
- The number of hours spent in playing the game is directly proportional to higherleague rankings. Players are advised to put in enough effort on a daily basis to gain therequired skills and experience for the game
- Starcraft is a multitasking game and it is important to manage the macro in the game.Features such as APM, NumberOfPACs, GapBetweenPACs, ActionsInPAC relate to thisand an ideal player should have low GapBetweenPACs, high NumberOfPACs andmaintain low ActionLatency between these actions. Players should strive to performmultiple actions within a short span to improve their game
- Micro management is also important as it involves effective movement and skillutilization of different units without taking too much time. Features such asMinimapRightClicks, SelectByHotkeys, AssignToHotkeys and UniqueHotkeys give agood indication on these metrics and how it relates to players from higher leagues
- Having the ability to effectively use diverse unit types is crucial for achieving success ingameplay. Metrics such as WorkersMade, UniqueUnitsMade, ComplexUnitsMade, andComplexAbilitiesUsed demonstrate this pattern, where higher-level players exhibithigher values in these metrics
- Higher usage of Minimap and Hotkeys is encouraged as it reduces the time taken toperform these actions
- The accuracy with which we can predict a player's League index is currently 38%. Basedon the confusion matrix, we can see that predicting LeagueIndex for 4,5,6 has thehighest error rate. It is possible that more data can help with better accuracy in theseleagues. Also, the variables APM and TotalHours are key predictors.

### If we were to collect more data?
- We need to first define the problem at hand as we might require additional featuresbased on the problem
Ensure that the features Age, HoursPerWeek and TotalHours are also collected. Thesefeatures are important in predicting the LeagueIndex of the players
- It would help to prioritize data collection where available data is less (For example,Leagues 7 & 8 have very few data points)
- It would help to analyze players data at different points in time to see how the playergrows and how each feature changes as the player progresses in different leagues
- Ensure that data is not restricted to one region. Different regions tend to have differentplay styles and features might differ based on region. It would be great to have this as afeature as well
