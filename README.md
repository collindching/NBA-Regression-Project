# NBA Regression Project

The winning strategy for a successful NBA team consists of several key components: great players, a team whose personality and playstyles complement each other, and a coach who can take advantage of each players' strengths--all while working with salary constraints. My question is: how do you build the best possible team and choose a strategy that best plays to their strengths, all while dealing with financial constraints? 

Optimizing for win-loss record. Also optimizing for score. Might be evaluating how accurate model is. 

You'd break this down into: which combination of traits would, according to your model, lead to the best possible team? And for that team, what would the best shot selection strategy be?

Obviously, this depends on the NBA talent pool for a given year. Maybe certain traits matter more than others.

Optimize for fantasy basketball?

#### Keys

- Iterate quickly through workflow
    - Scrape some, clean quickly, plot, model; scrape more, clean, plot, model
    - Build exploratory plots early
- Use Scikit-Learn Pipelines
- You could try tiered regression
    - Salary first
    - Then score
    - Who spends the most per point?
- Apply different types of analysis, think about angles and be thoughtful

**Tools used:** BeautifulSoup, Pandas, Scikit-Learn, MySQL

### Brainstorm 

####  Possible regressions

- Use team attributes to predict game scores (with confidence intervals) against other teams
- Use player statistics to predict regular season win-loss results 
- NBA shots to game scores

#### Questions

- How to combine teams? 
- What time of strategy is best? All-round? Specialized?
- How does defense affect scoring, and offense?
- Better to have higher defense on average? Or to have a couple strong defenders who can take out star scorers
- Defense: DFG%
- Which players are undervalued?
- Predict player salaries
- How deep is your bench?

#### Hypotheses

- Some attributes are more important for determining game score
- Attributes are strong against some attributes and weak against others
- A team with good attributes but the wrong strategy will not do well
- A diversity of attributes is good for a well-rounded team; some teams that do well, though, will specialize more in a specific attribute
- Spurs strategy is good despite not being how a lot of the NBA plays

**Data to use**

- Target: game scores 
- Shot efficiency
    - [Shooting efficiency](https://stats.nba.com/teams/shooting-efficiency/?Season=2018-19&SeasonType=Regular%20Season)
    - [Players shooting data](https://stats.nba.com/players/shooting/?Season=2018-19&SeasonType=Playoffs&DistanceRange=By%20Zone)
- Player efficiency rating
- Defensive statistics
- [NBA stats API](https://pypi.org/project/nba-api/)

## Plan:

- Tuesday: scope out project, scrape game scores
- Wednesday: scrape a few datasets, cursory clean, and baseline regression
- Thursday: 
- Friday:
- Saturday: 

**Steps**

- Scope project
- Generate questions and hypotheses
- Scrape player statistics from basketball-reference.com
- Build baseline regression model
- Exploratory analysis 
- Feature engineering
- Feature extraction?
- Build regression model
- Think about how it ties into conclusion

## Literature Review

Types of analysis:
- Best two-way players: points scored vs points given up... this could become a ratio that you feed into your model



## References

1. [Insights from Raw NBA Shot Log Data](https://towardsdatascience.com/insights-from-raw-nba-shot-log-data-and-an-exploration-of-the-hot-hand-phenomenon-1f1c6c63685a)
2. [NBA vs. NCAA Shooting](https://toddwschneider.com/posts/nba-vs-ncaa-basketball-shooting-performance/)
3. [Visualizing Game Style and Shooting Performance for Top Players](https://nycdatascience.com/blog/student-works/nba-shot-log/)
