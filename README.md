# NCAA
In NCAA football the BCS(Bowl Champion Series) comittee meets on a weekly basis and makes a AP(Associated press) top 25 poll. These polls are used to rank collegiate football teams based on not only there previous week but what they have done all season considering strength of schedule and win-loss records. These polls are important because they lead to the college football playoffs and bowl games. The voting for the top 25 is composed of 62 sportswriters and broadcasters from across the nation.(for AP) The Voting for the top 25 is composed of 65 coaches across the nation.(Coaches poll) Each writer votes who they think deserves the number 1 ranked spot and so on down to 25. Then the teams are given points based on how many votes they got and for what placing 1st ~ 25 points

1st ~ 25 points
2nd ~ 24 points
3rd ~ 23 points
4th ~ 22 points
5th ~ 21 points
6th ~ 20 points
7th ~ 19 points
8th ~ 18 points
9th ~ 17 points
10th ~ 16 points
11th ~ 15 points
12th ~ 14 points
13th ~ 13 points
14th ~ 12 points
15th ~ 11 points
16th ~ 10 points
17th ~ 9 points
18th ~ 8 points
19th ~ 7 points
20th ~ 6 points
21th ~ 5 points
22nd ~ 4 points
23rd ~ 3 points
24th ~ 2 points
25th ~ 1 point
After the voting is done the team with the most points gets placed in first place and so on. Without looking two deep into it the process seems fair and that the best teams more often then not get the proper recocgnition but this is not always the case. The problem faced is that not every team plays the same level of competitition and or has the same schedule. This creates something called conference bias where teams with more known to be more difficult schedules tend to get the benefit of the doubt in these rankings. This can cause teams that might deserve to be in these rankings but arent in as prestigious of conference to be overlooked. This model will attempt to fairly place BCS points and create a top 25 eliminating conference bias.

My Target Variable is going to be the differnce in votes per week and this will eventually lead to predicting the rank of each team by week. First things first we need to determine the biggest cause of drop or gain in rank.

My features are as listed and will change every week. team_points_x opponent_points_x won_x loss_x total_win_count_x total_loss_count_x opponent_rank opponent_votes offense_overall_x defense_overall_x team_rank team_votes cumulative_count difference_per_week

Loss- wether the team lost the game or not
Win- wether the team won the game or not.
team_votes: how many votes the home got to be ranked.
Opponent_votes: how many votes the opponent got to be ranked.
Teampoints ~ how many points the home team scored
opponent_points_x ~ how many points the away team scored.
Overall_offense- is calculated by summing up the Total EPA(Estimated points added) for all offensive plays in a game and dividing by the total number of offensive possessions in the game. This gives the average OPPA(Offense predicated Points Added) per offensive possession for the team over the course of the game.

Overall OPPA takes into account a team's offensive performance over the game and is useful for evaluating the effectiveness of a team's offense in comparison to other teams in the same conference or division, or across the entire NCAA. A higher OPPA indicates a more effective offense that is able to consistently add points to the team's score throughout the season, while a lower OPPA indicates a less productive offense that may struggle to move the ball and score points.

Defense_overall to calculate DPPA(defense predicated points added), the same basic process used for OPPA can be applied to the defense. Specifically, the Success Rate and Expected Points Added (EPA) for each defensive play can be calculated to obtain the Total EPA for all defensive plays in a game. Then, the Total EPA can be divided by the total number of defensive possessions in the game to obtain the average DPPA per defensive possession for the team over the course of the game.

Like OPPA, DPPA takes into account a team's defensive performance during the game and is useful for evaluating the effectiveness of a team's defense in comparison to other teams in the same conference or division, or across the entire NCAA. A higher DPPA indicates a more effective defense that is able to consistently prevent points from being scored by the opposing team, while a lower DPPA indicates a less effective defense that may struggle to stop the opposing team from moving the ball and scoring points.

In a game a teams offense and defense directly dependant on the other teams offense and defense performance so one teams offense performance number will be the opposing teams defense performance number and vice versa.
