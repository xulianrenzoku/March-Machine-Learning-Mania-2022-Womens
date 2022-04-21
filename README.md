# March-Machine-Learning-Mania-2022-Womens
**#12 Solution for 'March Machine Learning Mania 2022 - Women's at Kaggle**

[March Machine Learning Mania 2022 - Women's](https://www.kaggle.com/competitions/womens-march-mania-2022)

<img src='static/ncaaw-2022.png'>

### About the Competition
---
- **Task:** Predict the outcomes of this year's US women's college basketball tournament (NCAA Div. I). 
- **Eval Metric:** Submissions are scored on the log loss. According to Kaggle, the use of the logarithm provides extreme punishments for being both confident and wrong. Therefore, in the ideal world, you want your predictions to be relativefly aggressive when you nail the outcomes and relatively modest when the upsets occur.
- **Timeline:** Participants were asked to submit their predictions before the first round started. Therefore, all participants must predict all the possible matchups (2,016 in total). 

### Feature Engineering
---
Number of features: 66

Features used in the model:
- **Seeding**: The assumption behind the inclusion of seeding is, the gaps in competitiveness between top-seeded teams and bottom-seeded teams are relatively greater in womens' competition. In other words, strong favorites were relatively immune to upsets, based on historical results. 
- **Points Per Possession**: Both offensive and defensive points per possession (PPP) are used as measures of teams' performances on both ends. The inclusion of PPP over points scored/allowed per game were made because the tempos of a teams' games in a season were just different and using PPP took away the pace factor. Moreover, predicting difference in PPP over raw points in Stage 1 (will explain later) did lead to better predictions. Number of possessions of games wrere estimated by using (Kenpom's coefficient on free throws)[https://kenpom.com/blog/the-possession/].
- **Four Factors**: (Dean Oliver's Four factors)[https://www.basketball-reference.com/about/factors.html] are included as means to summarize teams' performance on various aspects.
  - Effective Field Goal Percentage (eFG):
  - Turnover Rate (TO%):
  - Offensive Rebound Rate (OR%):
  - Free Throw Rate (FTr):
- **538 Rating**: 

Features not used in the model:
- **Winning Percentage**: Disparities exist among conferences in terms of competition level. Comparing teams with higher winning percentage in a Mid-Major conference to teams with lower winning percentage in a Power Five conference is not an apples to apples proposition. Therefore, teams' winning percentages are not used as features.

### Modeling
---



