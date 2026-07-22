# Jack Huffard

**Baseball Operations/Analytics** M.S. Business Analytics candidate at Wake Forest University (May 2027) and Scouting Coordinator for Wake Forest Baseball Analytics.

I build models to inform strategic decision making on the baseball field, and the R infrastructure that puts them in front of a coaching staff. Most of that work is proprietary to Wake Forest and is not public, so this profile is the other half: research on public data and coursework. The Wake systems are described below without the code.

<img src="https://img.shields.io/badge/R-9E7E38?style=flat-square&logo=r&logoColor=white" alt="R"> <img src="https://img.shields.io/badge/Python-9E7E38?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/PostgreSQL-9E7E38?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Snowflake-9E7E38?style=flat-square&logo=snowflake&logoColor=white" alt="Snowflake"> <img src="https://img.shields.io/badge/Shiny-9E7E38?style=flat-square&logo=rstudioide&logoColor=white" alt="Shiny"> <img src="https://img.shields.io/badge/Tableau-9E7E38?style=flat-square&logo=tableau&logoColor=white" alt="Tableau"> <img src="https://img.shields.io/badge/Git-9E7E38?style=flat-square&logo=git&logoColor=white" alt="Git">

---

## Background

- **M.S. Business Analytics**, Wake Forest University, expected May 2027
- **B.S. Mathematical Business**, Wake Forest University, May 2026. Minors in Entrepreneurship and Statistics
- **Scouting Coordinator**, Wake Forest Baseball Analytics, December 2023 to present. Lead a team of eight student analysts producing opponent scouting reports for the coaching staff
- **NASCAR Analytics Intern**, Active Decision Support, 2025. Driver evaluation metrics and race-outcome models
- **Data Science Intern**, Tenable, 2024. Customer segmentation in Python and SQL against Snowflake, delivered as a Tableau dashboard still in use

---


## How I work

**Creative analytical strategies** I pride myself on thinking outside of the box, and staying flexible and resilient throughout the modeling process. For example, the small sample size issues in college baseball forced me to dive into Bayesian strategies which eventually resulted in a much improved final model (See DIP below). 

**Tools that get used during games.** The pitching coach calls pitches off a PDF my code generates. That constraint, that it has to work on a Tuesday afternoon with the actual staff, shapes the modeling more than any accuracy metric does.

**Decision problems over descriptive stats.** While descriptive stats help us understand what happened, I focus on modeling what we think WILL happen. 

**AI for productivity, efficiency, and brainstorming** I use Claude as a thought partner and an efficiency tool, it helps me move faster without compromising quality. The key is knowing how to write clear, effective prompts to get exactly what you need, whether that’s analyzing feedback, generating ideas, or fact-checking. I treat it as a powerful tool when used with intention and skill. I've also linked my Claude Code to an Obsidian folder which serves as a persistent, searchable record of every project I've built, so I'm not re-explaining my own work at the start of every session, cutting my token usage significantly. 

---

## Selected work

### Public repositories

| Project | Summary |
| :--- | :--- |
| **[nba-statistical-analysis](https://github.com/jackhuffardiii/nba-statistical-analysis)** | Predicting NBA wins from Dean Oliver's Four Factors across 10,780 games (2017-2022). Logistic regression, KNN, and random forest compared under 10-fold cross-validation, with permutation importance from the forest. Shooting efficiency and opponent shooting efficiency dominate; free throw rate is the least influential of the four. |
| **[pitch-velocity-bayesian-hierarchical-model](https://github.com/jackhuffardiii/pitch-velocity-bayesian-hierarchical-model)** | How much of a pitch's release speed comes down to game situation (count, inning, baserunners) versus the pitcher throwing it and the pitch type? Four JAGS models compared by DIC across eight starters. Adding pitch type and pitcher random intercepts cuts DIC by more than half, and leaving pitch type out systematically understates fastball velocity by 4 to 6 mph. |

### Built for Wake Forest Baseball Analytics

Proprietary to the program, so no code here. Included because it is the work that best represents what I do.

| Project | Summary |
| :--- | :--- |
| **DIP (Deacon Independent Pitching)** | A pitching metric that predicts next-season ERA, built from a coach's brief: make a stat that predicts future ERA, with a correlation over .40. Bayesian Gamma regression on K%, BB%, and a custom contact-quality feature fit from an empirical exit-velocity and launch-angle wOBA grid, estimated across roughly 1,228 pitcher-seasons with conference-tier intercepts. Correlates .402 with next-season ERA, against .290 for ERA itself, .315 for cFIP, and .308 for xFIP. Shipped as a production R function, a Shiny app with percentile bars, and conference leaderboards the staff uses. |
| **Automated scouting infrastructure** | The system that turns raw tracking and charting data into the printable opponent reports the coaching staff works from. PostgreSQL through R Markdown and `gt` to PDF, rendered per opponent and per series, plus the hitter attack plans the pitching coach uses in game. |
| **Stuff+ and xRV revamp**| Currently working to audit and update the underlying models that our Stuff+ and xRV models are built on top of, so that later when we retrain the Stuff+ and other models which use xRV as the target we get improved results. |


### In progress

| Project | Summary |
| :--- | :--- |
| **ABS challenge optimization** | When should a team spend an ABS challenge, and how much win probability did MLB teams leave on the table in the system's first season? A challenge is an option, not a coin flip, so the model is a dynamic program over game state (inning, margin, challenges remaining) against the win-probability value of flipping the call, with a hierarchical layer for player-level challenge accuracy and a perception model so the policy conditions on what the challenger could plausibly see rather than on Hawk-Eye truth. Analysis finished on the first half of 2026; writeup in draft. |
| **Batter-pitcher matchup engine** | Simulates plate appearance outcomes for any hitter-pitcher pairing: Beta shrinkage toward population priors, Marcel-style recency weighting, log5 combination, Monte Carlo, and a count-state Markov chain layered over pitch-level tendencies. Coded the matchup engine and shiny app using Claude given the statistical techniques and workflow that I perscribed, verifying the results and code myself.|

---

Reach me at [huffjc22@wfu.edu](mailto:huffjc22@wfu.edu), [jackhuffardiii@gmail.com](mailto:jackhuffardiii@gmail.com) or on [LinkedIn](https://www.linkedin.com/in/jack-huffard).
