# Urban Mobility & Economic Productivity

**Data Analytics Portfolio Project | Python · Pandas · NumPy · Matplotlib · Seaborn**

> An exploratory analysis of traffic congestion and economic productivity across **15 Latin American cities in 7 countries**, using **2024** data.

## Project Overview

This project explores whether higher urban traffic congestion is associated with lower economic productivity, measured using GDP per capita. It also identifies cities that may warrant further assessment for transportation infrastructure investment.

**Main questions**
- Is traffic congestion associated with GDP per capita?
- How closely are different mobility indicators related?
- Which cities combine above-average congestion with below-average GDP per capita?
- What further evidence would be needed to support infrastructure decisions?

## Data & Tools

The project integrates traffic indicators from **TomTom Traffic Index** and economic indicators from **OECD Cities**, using a common city-year level for the 2024 analysis.

- **Python and Pandas:** cleaning, standardization, aggregation, merging and correlation analysis
- **NumPy:** numerical analysis
- **Matplotlib and Seaborn:** exploratory charts and comparisons
- **Jupyter Notebook:** documented analytical workflow

## Methodology

1. Reviewed and standardized date formats, column names and numerical values.
2. Filtered records to 2024 and aggregated traffic data by city and year.
3. Combined traffic and economic data using an **INNER JOIN** to retain matching cities.
4. Examined distributions, potential outliers and city-level differences.
5. Evaluated linear correlations between traffic indicators, travel times and GDP per capita.

## Key Findings

| Relationship | Pearson correlation (r) | Interpretation |
|---|---:|---|
| Congestion delay vs. GDP per capita | **0.28** | Weak positive linear association |
| Traffic index vs. GDP per capita | **0.06** | Negligible linear association |
| Travel time per 10 km vs. GDP per capita | **0.09** | Negligible linear association |
| Traffic index vs. travel time | **0.84** | Strong positive linear association |

**Interpretation:** The sample did **not** show a strong negative linear relationship between traffic congestion and GDP per capita. Mobility indicators were more strongly associated with one another than with the economic indicator.

The analysis also revealed different city profiles: **Mexico City** combined relatively high GDP per capita with high congestion, while **Montevideo** showed comparatively strong economic indicators with lower congestion.

### Bogotá: Candidate for Further Assessment

Within the analyzed sample, **Bogotá** combined above-average congestion with below-average GDP per capita. This makes it a candidate for **additional infrastructure assessment**, not an automatic investment recommendation.

## Recommendations & Limitations

- Evaluate infrastructure priorities using additional factors, including population, employment, existing transportation networks and project feasibility.
- Extend the analysis across multiple years to test whether observed patterns persist.
- Validate source coverage, comparability and possible outliers before drawing policy conclusions.
- **Correlation does not imply causation.** This exploratory analysis cannot establish that traffic congestion causes lower economic productivity.

## Project Resources

- **[View the Jupyter Notebook](urban_mobility_analysis.ipynb)** — Full documented analytical workflow, including data preparation, visualizations and findings.
- **[Explore the Cleaned Dataset](data/processed/ladb_mobility_economy_2024_clean.csv)** — Final integrated city-level dataset for 2024.
- **[Python Dependencies](requirements.txt)** — Packages used in the analysis.

### Reproducibility Note

The notebook uses the original TomTom and OECD source CSV files in `data/raw/`, which are not included in this repository. The published processed CSV supports inspection of the final analytical dataset but does **not** by itself reproduce the full data preparation pipeline. The original traffic file is approximately 142 MB.

## Project Context

Completed as an **academic project** during the **TripleTen Data Analytics Bootcamp (2026)**.

**Clara Herrera**  
Electromechanical Engineer | Data Analytics  
[GitHub Profile](https://github.com/claraherrera1)
