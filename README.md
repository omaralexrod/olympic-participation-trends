# olympic-participation-trends

Analyzing 120+ years of Olympic athlete data to understand how the Games have evolved.

## Overview

The modern Olympics have run since 1896, and the athletes competing, the countries represented, and the balance between men and women have all changed dramatically over that span. This project explores those shifts using athlete-level records from every Summer and Winter Games between 1896 and 2016, sourced from Kaggle: https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results

The resulting analysis can help:

- **Sports historians** track how participation and representation have changed over a century of competition
- **Federations/analysts** identify which countries and sports have historically dominated medal counts
- **General audiences** understand long-term trends in gender representation at the Games

## Data

One dataset was used:

- `athlete_events.csv` — one row per athlete per event per Games, including sex, age, country (NOC), sport, event, and medal outcome (Gold/Silver/Bronze/None), for 1896–2016.

Due to file size (~40MB), the raw CSV is not committed to this repo — download it from https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results and place it in this folder to run the notebook.

## Approach

1. **Data cleaning** — handled missing values (age, height, weight), standardized country codes (NOC), and filtered to relevant columns for each analysis question.
2. **Participation analysis** — grouped by year and sex to calculate the share of female athletes over time.
3. **Medal analysis** — aggregated medal counts by country (NOC) and by sport, ranking each to identify the top performers.
4. **Visualization** — built time-series and bar chart visualizations for each of the three core questions.

## Results

| Metric | Finding |
|---|---|
| Female participation | Grew steadily from 1896 onward, with the sharpest increase after 1980 — by 2016, the gender gap in athlete counts had narrowed considerably |
| Top medal-winning country | United States, by a wide margin — followed by the Soviet Union, Germany, and Great Britain |
| Top medal-awarding sport | Athletics, followed closely by Swimming — both driven by the large number of individual events each sport includes |

Female participation in the Olympics rose steadily across the 120-year span, with the most notable acceleration starting around 1980, closing much of the historical gap with male participation by 2016. On the medal side, the United States has maintained a consistent, dominant presence across decades, while medal counts by sport are shaped less by national dominance and more by structural factors — sports like Athletics and Swimming simply offer far more individual events, and therefore far more chances to medal, than sports with fewer events.

## Tech Stack

- Python, pandas, NumPy
- matplotlib, seaborn

## Future Improvements

- Break down participation trends by sport, not just overall
- Adjust medal counts for team events (currently each team member counts as a separate medal)
- Compare Summer vs. Winter Games trends separately
- Build an interactive dashboard (Plotly/Tableau) for exploring trends by country

## Author

Omar Rodriguez Arellano
