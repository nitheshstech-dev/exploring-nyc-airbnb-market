# Exploring the NYC Airbnb Market

> A reproducible data-importing, cleaning and exploratory-analysis project using NYC Airbnb listing data from Inside Airbnb.

## Objective

Analyze the structure of the NYC short-term rental market by cleaning listing data and exploring listing distribution, room-type mix, nightly price patterns, availability, review activity and host listing concentration.

## Data Source

This project uses the **Inside Airbnb** NYC listings dataset. Inside Airbnb publishes city-level Airbnb data for research and analysis and provides New York City listings, calendar, reviews and neighbourhood resources.

Source: https://insideairbnb.com/get-the-data/

The source data is periodically updated, so this repository does not commit a fabricated dataset. Download the NYC `listings.csv` export and place it in `data/listings.csv`.

## Workflow

```text
Raw CSV
  ↓
Data Import
  ↓
Data Quality Checks
  ↓
Type Conversion & Standardization
  ↓
Duplicate / Invalid Record Handling
  ↓
Exploratory Data Analysis
  ↓
Visualization
  ↓
Business Interpretation
```

## Data Cleaning

The cleaning pipeline standardizes text fields, converts numeric columns safely, parses review dates, removes duplicate listing IDs, removes invalid/non-positive prices, removes invalid minimum-night values, validates availability values and validates latitude/longitude ranges while keeping the raw dataset unchanged.

Run:

```bash
python src/data_cleaning.py
```

## Exploratory Analysis

Run:

```bash
python src/eda_analysis.py
```

The analysis produces summary tables and charts covering:

1. Listing counts by borough
2. Room-type distribution
3. Average and median prices
4. Price distribution
5. Availability patterns
6. Host listing concentration
7. Relationships between price, reviews and availability

## SQL Analysis

`sql/analysis_queries.sql` provides SQL versions of the main analytical questions for a database workflow.

## Repository Structure

```text
exploring-nyc-airbnb-market/
├── data/
│   └── README.md
├── notebooks/
│   └── nyc_airbnb_analysis.md
├── src/
│   ├── data_cleaning.py
│   └── eda_analysis.py
├── sql/
│   └── analysis_queries.sql
├── visualizations/
├── docs/
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md
```

## Reproducibility

1. Download the current NYC listings data from Inside Airbnb.
2. Save it as `data/listings.csv`.
3. Install dependencies with `pip install -r requirements.txt`.
4. Run the cleaning script.
5. Run the EDA script.
6. Review the generated tables and charts.

## Analyst Notes

This project separates **data preparation** from **analysis** so the workflow can be repeated when the source dataset changes. Extreme prices are retained for analytical integrity; the visualization script clips only the upper tail for one chart to improve readability.

## Limitations

- Airbnb listing data is a market snapshot, not a complete record of New York housing or tourism activity.
- Prices and availability change over time.
- Listing presence does not guarantee actual booking activity.
- Observational relationships should not automatically be interpreted as causal effects.
- Review the source project's data policies and assumptions before making policy or commercial conclusions.

## Skills Demonstrated

Python • Pandas • NumPy • Data Cleaning • Exploratory Data Analysis • Data Visualization • SQL • Data Quality Checks • Reproducible Analytics

## Author

**Nithesh S**

GitHub: https://github.com/nitheshstech-dev

## License

MIT
