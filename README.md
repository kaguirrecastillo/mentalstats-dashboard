# Mentalstats Dashboard (OWID Suicide Rates)

A small end-to-end data project that cleans and summarizes suicide-rate time series from Our World in Data (OWID) for quick analysis and dashboarding.

## Data
- Source: Our World in Data (OWID) Grapher — "Reported suicide rates (WHO Mortality Database)"
- Dataset: `suicide-rate-who-mdb.csv`

## What’s inside
### Pipeline
- `notebooks/01_clean.ipynb` loads the OWID CSV, cleans it, and exports outputs to `reports/`.

### Outputs (CSV)
- `reports/cleaned.csv` — cleaned dataset (country, iso3, year, suicide_rate)
- `reports/suicide_rate_year_country.csv` — main table for trend lines and filters
- `reports/suicide_rate_top_countries_latest.csv` — ranking for the latest available year (global max year)
- `reports/suicide_rate_summary_latest.csv` — latest value per country + change vs previous available year

## How to run
1) Create/activate your environment (optional)
2) Run the notebook:
   - Open Jupyter and run `notebooks/01_clean.ipynb`

## Notes on interpretation
- Countries may have different “latest available years” depending on reporting coverage.
- The “Top countries (latest year)” file uses the maximum year available in the dataset overall.

## Next steps (optional)
- Add `notebooks/02_eda.ipynb` with charts (trend, top 10, distribution).
- Build a Looker Studio dashboard using `reports/suicide_rate_year_country.csv` and add the public link here.
