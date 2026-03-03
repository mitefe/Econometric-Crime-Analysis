# Econometric Analysis of Regional Crime Drivers

## Executive Summary
Understanding the macroeconomic and demographic factors that influence crime rates is essential for effective public policy. This repository contains a cross-sectional econometric analysis of the 16 German states (Bundesländer). 

By utilizing Ordinary Least Squares (OLS) regression, this project isolates the statistical impact of per capita income, population size, and demographic makeup on regional crime rates. The objective is to move beyond raw exploratory data analysis (correlation) and establish mathematical causation, allowing for strictly data-driven law enforcement resource allocation.

## Data Sources & Tech Stack
* **Language & Libraries:** Python, Pandas, Statsmodels, Seaborn, Matplotlib
* **Data Engineering:** Self-contained data architecture embedded directly into the code for reproducibility.
* **Official Sources:**
  * Crime Rates (2024): Statista (Reported incidents per 100,000 population).
  * Socioeconomic Data (2023): Destatis - Federal Statistical Office of Germany.

## Econometric Methodology
To determine true statistical significance, a multiple linear regression model was constructed:
* **Dependent Variable (Y):** Crime Rate per 100,000 people.
* **Independent Variables (X):** Income per capita, Foreign population share, and Total population.
* **Diagnostics:** Multicollinearity checks via correlation heatmaps and comprehensive t-statistic/p-value evaluations via the Statsmodels API.

## Key Statistical Findings
The regression model successfully explained **53.9% of the variance** in state-level crime rates (R-squared = 0.539, P-value = 0.0219). The analysis revealed critical deviations from traditional assumptions:

1. **The Income Fallacy:** Per capita income proved statistically insignificant (P-value = 0.953) as a direct driver of crime rates when controlling for other variables.
2. **The "City-State Effect" (Stadtstaaten-Effekt):** Total population emerged as the most significant variable (P-value = 0.023) with a negative coefficient. This mathematically confirms that highly populous territorial states (e.g., Bavaria) experience lower per-capita crime, whereas smaller, densely packed city-states (Berlin, Bremen, Hamburg) suffer from exponentially amplified crime rates.
3. **Correlation vs. Causation:** Demographic metrics such as foreign population share, while showing high initial correlation, proved only marginally significant (P-value = 0.060) when strictly controlling for population density.

## Policy Implications
The mathematical evidence suggests that public safety budgets and tactical deployments should not be guided by regional wealth or raw demographic assumptions. Instead, federal law enforcement must prioritize extreme-density urban structures (city-states), as urban geography dictates crime probability far more heavily than economic indicators.
