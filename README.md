# Clustering NBA Players Based on Performance
Analysing Player performance stats for NBA season 2020-2021. Basketball players are traditionally grouped into five distinct positions, but these designations are quickly becoming outdated. This study is an attempt to reclassify players into new groups based on personal performance in the 2020-2021 NBA regular season.

Is it possible that a new player designation can be determined based on the actual performance of modern basketball players? If such a designation is found, could it be used to build a strong basketball team?


## Quick Result Summary
Interpretting clusters with t-SNE projection of 18 metrics.

![__results___72_0](https://user-images.githubusercontent.com/93088807/197339005-4c70f0be-de88-4799-a6c1-6dd00dc425e9.png)

Looking at the average stats of players in each cluster, the Clusters can be interpreted as,
- Cluster 0 (blue): The Bruiser, moderate scorers, active players, excellent 2P shooting accuracy, very good offensive rebounds and good blocks.
- Cluster 1 (orange): The Carry, high scorers, very good 3P shooting, good 2P shooting and very good defensive rebounds.
- Cluster 2 (green): The Marksmen, moderate scorers, good 3P shooting accuracy, descent assists and best steals.
- Cluster 3 (red): The Support, relatively low scorers, descent 3P shooters, decent free-trow shooting accuracy.

### Importance of Players in Each Cluster
In order to understand if players in one cluster are more important in a team's success than the others, team rank can be visualized against fraction of player in each cluster.
![__results___101_0](https://user-images.githubusercontent.com/93088807/197339162-a20d2f07-ed23-4be5-a96c-b6a54050990c.png)

Failed to reject the null hypothesis with a significance level of 0.05 that, β = 0.

From the above analysis of Team rank and fraction of players in each cluster it is clear that there is no significance when applying linear regression to all four plots. This suggests that there is no relationship between how good a team is and membership in a particular cluster. **All clusters are equally important, suggesting there is no one type of player that dominates the NBA.**

### Average Variance and Mean Absolute Deviation of Teams
![__results___108_0](https://user-images.githubusercontent.com/93088807/197339230-a0941d10-3982-4980-a27f-20d19d82c04b.png)

From the analysis of spread of players in each team, we reject the null hypothesis, that β = 0, with a significance level of 0.05. This indicates that there indeed is a significant relationship between the team ranks and the average variance and mean absolute deviation on performance metrics for teams.

It looks like better teams have players more spread apart, while worse teams are more grouped together. This result is revealed through a p-value of **0.00299** and **0.00646** for the slopes in linear regression.

**The results indicate that strong teams have players whose success cannot be attributed to fundamentals alone. Players being more spread apart on the performance metrics space means that the team has more diversity and diversity in turn ensures that the players' skillsets complement each other.**


## About Dataset

This dataset has been obtained from [Basketball-reference](https://www.basketball-reference.com/)

Note:
Some of the advanced performance statistics may be missing in older data.
The N.B.A. introduced the 3-point shot in the 1979-80 season. So, 3PA, 3P, and 3P% are absent in older records.
Attribute Information:

**player_data.csv**

* From -- First year
* To -- Last year
* Pos -- Position
* Ht -- Height
* Wt -- Weight
* Birth Date -- Birth Date
* Colleges -- College

**seasons_stats.csv**

Over 50 performance stats,
Here is a list of Columns in this file and their descriptions, [Glossary](https://www.basketball-reference.com/about/glossary.html)













