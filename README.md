# A-B-Testing-Analysis

Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It's a classic "connect three" style puzzle game where the player must connect tiles of the same color in order to clear the board and win the level. It also features singing cats. We're not kidding!

As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention and game rounds.

To complete this project, you should be comfortable working with pandas DataFrames and with using the pandas plot method. You should also have some understanding of hypothesis testing and bootstrap analysis.

The data is from 90,189 players that installed the game while the AB-test was running. The variables are:

userid - a unique number that identifies each player.
version - whether the player was put in the control group (gate_30 - a gate at level 30) or the test group (gate_40 - a gate at level 40).
sum_gamerounds - the number of game rounds played by the player during the first week after installation
retention_1 - did the player come back and play 1 day after installing?
retention_7 - did the player come back and play 7 days after installing?
When a player installed the game, he or she was randomly assigned to either gate_30 or gate_40.

AB Testing Process

1. Understanding business problem & data
2. Detect and resolve problems in the data (Missing Value, Outliers, Unexpected Value)
3. Look summary stats and plots
4. Apply hypothesis testing and check assumptions
5. Check Normality & Homogeneity
6. Apply tests (Shapiro, Levene Test, T-Test, Welch Test, Mann Whitney U Test)
7. Evaluate the results
8. Make inferences
9. Recommend business decision to your customer/director/ceo etc.

The users installed the game but 3994 users never played the game! Some reasons might explain this situation.

* They have no free time to play game
* Users might prefer to play other games or they play other games already
* Some users don't like the app etc.
* You can comment below for this users also
* The number of users decreases as the levels progress

* Most of users played the game at early stage and they didn't progress.
* Tactile Entertainment should learn why users churn playing the game.
* Doing research and collecting data about the game and users would help to understand user churn
* The difficulty of the game can be measured
* Gifts might help player retention

Assumptions:¶

1. Check normality
2. If Normal Distribution, check homogeneity

Steps:

1. Split & Define Control Group & Test Group
2. Apply Shapiro Test for normality
3. If parametric apply Levene Test for homogeneity of variances
4. If Parametric + homogeneity of variances apply T-Test
5. If Parametric - homogeneity of variances apply Welch Test
6. If Non-parametric apply Mann Whitney U Test directly

Conclusion

As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention and game rounds.

Firstly, we investigated relationships and structures in the data. There was no missing value problem but was one outlier problem in the data. Summary stats and plots help us to understand the data and problem.

Before A/B Testing, we shared some details about game, players, problems and suggestion to our customer/director/ceo etc.

After applying A/B Testing, the analysis result gives us some important information. Shapiro Testing rejected H0 for Normality assumption. Therefore we needed to apply a Non-parametric test as called Mann Whitney U to compare two groups. As a result, Mann Whitney U Testing rejected H0 hypothesis and we learned A/B groups are not similar!

Briefly, There are statistically significant difference between two groups about moving first gate from level 30 to level 40 for game rounds.

Which level has more advantages in terms of player retention?
 
1-day and 7-day average retention are higher when the gate is at level 30 than when it is at level 40.
