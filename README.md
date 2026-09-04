# F1 Pit Strategy Analysis: Does the Undercut Actually Work?

An analysis of 2,790 pit stops across the 2011–2017 F1 seasons, testing whether
pitting early (the "undercut") reliably improves finishing position compared to
pitting late (the "overcut") or staying in line with the field.

**[Live dashboard →](https://rhughes33.github.io/F1StrategyUndercutVSOvercut/)**
**[Kaggle notebook →](https://www.kaggle.com/code/rhodrimorganhughes/f1strategycode)**

## Headline finding

Across the full dataset, the undercut shows a small **net loss** on average
(-0.46 positions per attempt) — and the overcut outperformed it in every single
season from 2011 to 2017. The raw number is misleading on its own though:
backmarker teams like Marussia and Caterham show the largest undercut gains,
most likely because they were pitting into clean air with little midfield
traffic to defend against, not because of superior strategy calling.

## Method

- Classified each driver's first pit stop per race as an **undercut**,
  **overcut**, or **inline** call, relative to that race's median first-stop lap
  (±2 laps as the threshold)
- Measured positions gained/lost as grid position minus classified finishing
  position
- Scoped to 2011–2017 — the earliest seasons with complete pit stop timing data
  in this dataset

## Data

[Formula 1 Race Data 1950-2017](https://www.kaggle.com/datasets/cjgdev/formula-1-race-data-19502017)
(Kaggle, Ergast-based)

## Tools

Python (pandas, Plotly) for the analysis · HTML/CSS/JS for the dashboard

## Caveats

Field median stop lap is a simplification of "expected strategy" and doesn't
account for safety car periods, which can distort optimal pit windows
independent of a team's strategic skill.
