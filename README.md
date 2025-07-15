# 🏏 IPL Data Analysis Dashboard - Power BI

This repository contains a Power BI dashboard project built to analyze **IPL (Indian Premier League)** data. The dashboard provides interactive insights into team performances, player statistics, and match outcomes across multiple IPL seasons. It is designed as a **portfolio project** for data analysis roles, especially for beginners and freshers.

---

## 📊 Dashboard Overview

The Power BI dashboard is divided into **3 main pages**, each with a clear focus:

### 1. IPL Overview
- Total Matches, Seasons, and Teams
- Match wins by each team
- Matches played per season
- Toss decision trends

### 2. Batsman Performance
- Top 10 batsmen with runs, boundaries, and strike rates
- Runs by top 5 batsmen
- Strike rate comparison chart

### 3. Bowler Performance & Wickets Analysis
- Top 10 bowlers with wickets, economy, and runs conceded
- Wickets by top 5 bowlers
- Types of dismissals (bowled, caught, etc.)

---

## 📁 Dataset

The dashboard uses two main datasets:

- `Matches.csv`: Contains match-level information such as season, teams, toss, and winner.
- `Deliveries.csv`: Contains ball-by-ball data including batsman, bowler, runs, and dismissal info.

> 📌 The datasets are publicly available from Kaggle or other cricket data sources. You can also upload your own cleaned CSV files.

---

## 🧮 DAX Measures (Simple & Beginner Friendly)

Some of the custom measures used:

```DAX
Total Matches = DISTINCTCOUNT(Matches[match_id])

Total Runs = SUM(Deliveries[batsman_runs])

Wickets = CALCULATE(COUNTROWS(Deliveries), NOT(ISBLANK(Deliveries[player_dismissed])))

Strike Rate = DIVIDE([Total Runs], COUNTROWS(Deliveries)) * 100

Economy = DIVIDE(SUM(Deliveries[total_runs]), COUNTROWS(Deliveries)) * 6

Built By Utsav Shrivastava 
https://www.linkedin.com/in/utsav-shrivastava-71248b315