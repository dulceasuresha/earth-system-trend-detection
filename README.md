# Earth System Trend Detection

Detecting climate trends using NASA / NOAA data (2000-2024)
NASA Space Apps Challenge

This project analyzes 25 years of Earth observation data to detect long-term climate trends and validate whether the observed warming is statistically significant.

## What This Project Addresses

NASA Earth system data covers multiple interacting components: atmosphere, oceans, land surface, and cryosphere. Changes in one component affect the others, but long-term trends are often difficult to separate from year-to-year variability.

This project addresses that problem by:

1. Quantifying long-term warming trends from global temperature records.
2. Separating a persistent climate signal from short-term natural variation.
3. Validating trends with statistical tests so results are not based on visual interpretation alone.
4. Providing a reproducible workflow for analyzing Earth system time-series data.

The focus is on global surface temperature anomaly as a primary indicator of Earth system change.

## Results

| Metric | Result |
| --- | --- |
| Dataset | NASA GISTEMP and NOAA Global Climate Data (2000-2024) |
| Warming trend | +0.18 °C per decade |
| Total warming (2000-2024) | +0.45 °C |
| Statistical significance | p < 0.001 |
| Hottest year in dataset | 2024 |
| Methods | Linear Regression, Mann-Kendall Trend Test |

## Models Used

### 1. Linear Regression

Used to estimate the rate of change in temperature over time.

- Input: Year as independent variable, temperature anomaly as dependent variable
- Output: Slope representing warming per year, converted to per decade
- Purpose: Quantifies how fast the Earth system is warming

### 2. Mann-Kendall Trend Test

Used to validate whether the trend is statistically significant.

- Non-parametric test, does not assume normal distribution
- Tests for monotonic increasing or decreasing trend
- Output: p-value and trend direction
- Purpose: Confirms the warming trend is real and not random variation

### 3. Decadal Averaging and Anomaly Analysis

Used to reduce short-term noise and compare long-term behavior.

- Groups data into 10-year periods
- Compares 2000-2009, 2010-2019, and 2015-2024
- Purpose: Shows acceleration and long-term Earth system change

## Methodology

1. Data collection: Monthly global temperature anomalies from NASA GISS and NOAA.
2. Data cleaning: Handled missing values and normalized anomalies to the 1951-1980 baseline.
3. Exploratory analysis: Examined anomalies, seasonal patterns, and decadal averages.
4. Trend detection: Applied linear regression to estimate the warming rate.
5. Statistical validation: Applied the Mann-Kendall test to confirm trend significance.
6. Visualization: Produced time-series plots, heatmaps, and anomaly charts.

## Tech Stack

- Python 3.10+
- Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy
- Google Colab
- Data sources: NASA GISTEMP, NOAA NCEI

## Project Structure

    earth-system-trend-detection/
        earth_system_trend_detective.ipynb
        README.md

## How to Run

1. Open earth_system_trend_detective.ipynb
2. Open in Google Colab or run locally with Jupyter
3. Run all cells: Runtime > Run All
4. All charts will generate automatically

## Key Findings

- Global temperature shows a consistent warming signal since 2000.
- Warming in 2015-2024 was faster than in the previous 15 years.
- 2024 is the hottest year in the dataset.
- The Mann-Kendall test confirms the trend is significant (p < 0.001), indicating it is not random variation.

## Author

Dulcea Suresha
GitHub: https://github.com/dulceasuresha
Project submitted for NASA Space Apps Challenge

## License

MIT License
