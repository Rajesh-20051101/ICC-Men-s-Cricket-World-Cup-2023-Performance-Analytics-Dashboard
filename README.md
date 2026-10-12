# 🏏 ODI World Cup 2023 — Performance Analytics Dashboard

## 📌 Project Overview

This project analyzes the ICC Men's ODI Cricket World Cup 2023 using Microsoft Power BI Desktop.

The dashboard provides insights into team performance, player statistics, batting and bowling performance, and match trends through interactive visualizations.

The objective is to transform ball-by-ball cricket data into meaningful insights that help users compare teams, evaluate player performances, and explore tournament trends.

---

## 🎯 Project Objectives

- Analyze team-wise batting and bowling performance.
- Identify the top run scorers and wicket takers.
- Compare boundaries scored by different teams and players.
- Analyze batting run rates and match scoring patterns.
- Explore venue-wise scoring trends.
- Build an interactive, multi-page Power BI dashboard.

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — Dashboard development and data visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — Measures and analytical calculations
- **Microsoft Excel** — Source data handling

---

## 📊 Dashboard Pages

### 1. Overview
- Total matches
- Total runs
- Total wickets
- Total fours and sixes
- Top run scorers
- Top wicket takers

### 2. Team Performance
- Total runs by team
- Wickets by bowling team
- Batting run rate
- Average runs per match
- Fours and sixes by team
- Team performance comparison table

### 3. Player Performance
- Top 10 run scorers
- Top 10 wicket takers
- Player-wise fours and sixes
- Total boundaries
- Player performance details

### 4. Match Analysis
- Runs by match date
- Runs by venue or city
- Match-level performance analysis
- Date, venue, and team filters

---

## ⚙️ Data Preparation

The project uses ball-by-ball ODI cricket data for the 2023 World Cup.

Data preparation includes:
- Reviewing column names and data types
- Cleaning and transforming the source data
- Creating a calendar table
- Establishing date relationships
- Developing DAX measures for performance analysis

---

## 📐 Key DAX Measures

Examples of measures used in the dashboard:

### Total Matches

```dax
Total Matches =
DISTINCTCOUNT('ODI 2023'[match_id])
```

### Total Runs

```dax
Total Runs =
SUM('ODI 2023'[runs_off_bat]) +
SUM('ODI 2023'[extras])
```

### Total Wickets

```dax
Total Wickets =
COUNTROWS(
    FILTER(
        'ODI 2023',
        NOT ISBLANK('ODI 2023'[player_dismissed])
    )
)
```

### Total Boundaries

```dax
Total Boundaries =
[Total Fours] + [Total Sixes]
```

*Note: Measures depend on the model's relationships and filter context.*

---

## ✨ Key Features

- Interactive slicers and filters
- Four-page report navigation
- Team-wise colour coding
- DAX-based calculations
- Player and team comparisons
- Date-based analysis
- Interactive charts and tables

---

## 📁 Repository Structure

```text
ODI-World-Cup-2023-PowerBI-Analysis/
│
├── ODI WORLD CUP ANALYSIS PROJECT.pbix
├── dataset_odi.xlsx
├── README.md
└── screenshots/
    ├── overview.png
    ├── team-performance.png
    ├── player-performance.png
    └── match-analysis.png
```

*The dataset and screenshot files should be included only if they are available and permitted to be shared.*

---

## 🚀 How to Use

1. Download the `.pbix` file from this repository.
2. Install Microsoft Power BI Desktop.
3. Open the downloaded Power BI report.
4. If prompted, update the source-data path.
5. Refresh the data if required.
6. Explore the dashboard using the navigation buttons and slicers.

---

## 💡 Skills Demonstrated

- Data cleaning and transformation
- Data modelling and relationships
- DAX measures
- Data visualization
- Interactive dashboard development
- Analytical thinking
- Cricket performance analysis

---

## 👨‍💻 Author

**Rajesh M**

B.Sc. Computer Science | Aspiring Data Analyst
