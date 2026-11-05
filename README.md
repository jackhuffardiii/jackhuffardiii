<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/header-light.svg">
  <img src="assets/header-dark.svg" alt="Jack Huffard, Baseball Operations and Analytics" width="100%">
</picture>

<img src="assets/headshot.jpg" alt="Jack Huffard" width="170" align="right">

**Baseball Operations and Sports Analytics** M.S. Business Analytics candidate at Wake Forest University (May 2027) and Scouting Coordinator for Wake Forest Baseball Analytics.

I build models to inform strategic decision-making on the baseball field, and the R infrastructure that puts them in front of a coaching staff. Most of that work is proprietary to Wake Forest and is not public, so this profile is the other half: research on public data, personal projects, and coursework. The Wake systems are described below without the code.

<img src="https://img.shields.io/badge/R-101216?style=flat-square&logo=r&logoColor=C9A227" alt="R"> <img src="https://img.shields.io/badge/Python-101216?style=flat-square&logo=python&logoColor=C9A227" alt="Python"> <img src="https://img.shields.io/badge/PostgreSQL-101216?style=flat-square&logo=postgresql&logoColor=C9A227" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Snowflake-101216?style=flat-square&logo=snowflake&logoColor=C9A227" alt="Snowflake"> <img src="https://img.shields.io/badge/Shiny-101216?style=flat-square&logo=rstudioide&logoColor=C9A227" alt="Shiny"> <img src="https://img.shields.io/badge/Tableau-101216?style=flat-square&logo=tableau&logoColor=C9A227" alt="Tableau"> <img src="https://img.shields.io/badge/Git-101216?style=flat-square&logo=git&logoColor=C9A227" alt="Git">

---

## Resume

**[View my resume](assets/jack-huffard-resume.pdf)** or **[download the PDF](https://github.com/jackhuffardiii/jackhuffardiii/raw/main/assets/jack-huffard-resume.pdf)**. 
---

## Background

- **M.S. Business Analytics**, Wake Forest University, May 2027
- **B.S. Mathematical Business**, Wake Forest University, May 2026. Minors in Entrepreneurship and Statistics
- **Scouting Coordinator**, Wake Forest Baseball Analytics, December 2023 to present. Lead a team of eight student analysts producing opponent scouting reports for the coaching staff. I own the pipeline the reports are built on and translate the coaches' questions into the analyses that answer them
- **NASCAR Analytics Intern**, Active Decision Support, 2025. Built the driver evaluation system: custom performance metrics and machine learning models that predict race outcomes and separate over- from underperformers by track type, delivered as R Markdown leaderboards for a non-technical audience
- **Data Science Intern**, Tenable, 2024. Customer segmentation in Python on Snowflake data pulled with SQL, scored on license usage, scan frequency, and scan size. Delivered as a Tableau dashboard still in use today, demoed to more than 50 data scientists, engineers, and customer success managers, and used to hand the sales team its 400 strongest upsell leads

---


## How I work

**Creative analytical strategies** I pride myself on thinking outside of the box, and staying flexible and resilient throughout the modeling process. For example, the small sample size issues in college baseball forced me to dive into Bayesian strategies, which eventually resulted in a much improved final model (See DIP below). 

**Tools that get used during games.** The pitching coach calls pitches off a PDF my code generates. That constraint, that it has to work on a Tuesday afternoon with the actual staff, shapes the modeling more than any accuracy metric does.

**Decision problems over descriptive stats.** While descriptive stats help us understand what happened, I focus on modeling what we think WILL happen. 

**AI for productivity, efficiency, and brainstorming** I use Claude as a thought partner and an efficiency tool; it helps me move faster without compromising quality. The key is knowing how to write clear, effective prompts to get exactly what you need, whether that’s analyzing feedback, generating ideas, or fact-checking. I treat it as a powerful tool when used with intention and skill. I've also linked my Claude Code to an Obsidian folder, which serves as a persistent, searchable record of every project I've built, so I'm not re-explaining my own work at the start of every session, cutting my token usage significantly. 

---

## Selected work

### Public repositories

| Project | Summary |
| :--- | :--- |
| **[nba-statistical-analysis](https://github.com/jackhuffardiii/nba-statistical-analysis)** | Predicting NBA wins from Dean Oliver's Four Factors across 10,780 games (2017-2022). Logistic regression, KNN, and random forest compared under 10-fold cross-validation, with permutation importance from the forest. Shooting efficiency and opponent shooting efficiency dominate; free throw rate is the least influential of the four. |
| **[pitch-velocity-bayesian-hierarchical-model](https://github.com/jackhuffardiii/pitch-velocity-bayesian-hierarchical-model)** | How much of a pitch's release speed comes down to game situation (count, inning, baserunners) versus the pitcher throwing it and the pitch type? Four JAGS models compared by DIC across eight starters. Adding pitch type and pitcher random intercepts cuts DIC by more than half, and leaving pitch type out systematically understates fastball velocity by 4 to 6 mph. |
| **[milb-hitter-value](https://github.com/jackhuffardiii/milb-hitter-value)** | Surplus dollar values for every A through AAA hitter and pitcher, with an audit trail from the minor league stat line to MLB-equivalent rates, P(reach MLB), expected WAR over six control years, ETA, and surplus dollars with a 10/50/90 range. On the 2013-17 hitter holdout, it beats a naive baseline on P(MLB) log loss (.371 vs .447). However, Baseball America's rankings still order prospects better (.238 vs .369 Spearman with realized six-year WAR). Live at https://milb-hitter-value.netlify.app, including a beta trade page. |
| **[mlb-trade-web](https://github.com/jackhuffardiii/mlb-trade-web)** | Engineered an MLB trade flow visualization app using agentic coding. A GitHub action runs daily at 7:00 AM EST, which scans for new trades and adds them to the dataset. Deployed app at https://mlb-trade-web.vercel.app/. Feel free to check it out! |
| **[claude-desktop-mods](https://github.com/jackhuffardiii/claude-desktop-mods)** | Here is how I set up my Claude workflow: an auto-handoff mod that moves long sessions to a fresh one at 300k context tokens, the skills I wrote (spec interviews before any code, a model audit checklist, a sports ML workflow, brainstorming, handoffs, and slide rules), and the open-source skills I use with them. |

### Built for Wake Forest Baseball Analytics

Proprietary to the program, so no code here. Included because it is the work that best represents what I do.

| Project | Summary |
| :--- | :--- |
| **DIP (Deacon Independent Pitching)** | A pitching metric that predicts next-season ERA, built from a coach's brief: make a stat that predicts future ERA, with a correlation over .40. Bayesian Gamma regression on K%, BB%, and a custom contact-quality feature fit from an empirical exit-velocity and launch-angle wOBA grid, estimated across roughly 1,228 pitcher-seasons with conference-tier intercepts. Correlates .402 with next-season ERA, against .290 for ERA itself, .315 for cFIP, and .308 for xFIP. Shipped as a production R function, a Shiny app with percentile bars, and conference leaderboards the staff uses. |
| **Automated scouting infrastructure** | The system that turns raw tracking and charting data into the printable opponent reports the coaching staff works from. PostgreSQL through R Markdown and `gt` to PDF, rendered per opponent and per series, plus the hitter attack plans the pitching coach uses in game. |
| **Stuff+ and xRV rebuild** | Rebuilt our pitch-level xRV on ACC and SEC TrackMan data, with our internal Pitching+ and Stuff+ grades built on top of it. Coaches see pitch quality and results side by side, so the gap between the two is visible. |


### Other NBA work

Code is private for now.

| Project | Summary |
| :--- | :--- |
| **NBA Tradeability Index** | Two scores for every NBA contract: Asset Value (projected on-court value minus salary, from my own RAPM) and Movability (how many legal trade structures exist under the 2023 CBA, from a trade engine that replays every 2026-27 trade so far as legal). The test was written down before any result existed, and the main idea failed: Movability scored .483 and .495 where .500 is no signal, likely because some legal structure almost always exists. Salary, years left, and age alone predict who gets traded better than Asset Value does. |

### In progress

| Project | Summary |
| :--- | :--- |
| **NBA game simulator** | A possession-level Monte Carlo simulator (5,000 sims per game) scored against closing lines, with every test declared before scoring. The one-time 2025-26 holdout failed most of them: margin MAE was 11.78 against 10.82 for the closing spread, with no evidence that the sim adds information beyond the close, although its win probabilities were calibrated. It now logs live 2026-27 forecasts before tip, which get rescored at season end. |
| **NBA lineup matchups** | Do lineup style and opponent style predict possession outcomes beyond additive player ratings, out of sample? Pre-registered against frozen RAPM as the null. A planted-effect power analysis came back at a 2% false positive rate but only 32% power at 3 points per 100, implying the test can only detect large effects. Test seasons 2022-25 are not scored yet. |

---

Reach me at [huffjc22@wfu.edu](mailto:huffjc22@wfu.edu), [jackhuffardiii@gmail.com](mailto:jackhuffardiii@gmail.com) or on [LinkedIn](https://www.linkedin.com/in/jack-huffard).
