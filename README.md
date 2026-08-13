# Exploring the Albany Airbnb Market

> End-to-end data importing, cleaning, exploratory analysis and visualization of Airbnb listings in Albany, New York.

## Project Overview

This project analyzes the Albany Airbnb market using listing, calendar, review and neighbourhood data. The workflow demonstrates a practical Data Analyst process: ingest raw data, validate data quality, clean and transform fields, perform exploratory analysis, create visualizations, and communicate evidence-based findings.

## Business Questions

- How many Airbnb listings are available in Albany?
- Which neighbourhoods have the most listings?
- Which room types dominate the market?
- How do nightly prices vary by neighbourhood and room type?
- Which listings have the highest availability?
- How active are listings based on reviews?
- How concentrated are listings among hosts?
- What relationships exist between price, reviews and availability?

## Data Sources

The project uses Airbnb data published through **Inside Airbnb**. The downloaded files used for this project are Albany, New York data, including listings, calendar, reviews and neighbourhood resources.

Source: https://insideairbnb.com/get-the-data/

Raw source files are kept separate from processed outputs. If redistribution of the original files is not appropriate, keep them locally and commit only the data dictionary and analysis outputs.

## Analytical Workflow

```text
Raw Airbnb Data
      ↓
Data Import & Profiling
      ↓
Data Quality Checks
      ↓
Cleaning & Type Conversion
      ↓
Feature Preparation
      ↓
Exploratory Data Analysis
      ↓
Visualization / Dashboard
      ↓
Business Insights
```

## Dataset Structure

### Listings

Core listing-level fields include listing ID, host information, neighbourhood, coordinates, room type, price, minimum nights, reviews, review recency, host listing count and annual availability.

### Calendar

Daily availability and price information can be used for deeper availability and pricing analysis.

### Reviews

Review-level records support review-volume and activity analysis.

### Neighbourhoods

Neighbourhood labels and geographic boundaries support location-based analysis.

## Data Cleaning

The cleaning process is designed to:

- Standardize text fields
- Convert numeric columns safely
- Parse review dates
- Remove duplicate listing IDs
- Remove invalid or non-positive prices
- Validate minimum-night values
- Validate annual availability from 0–365 days
- Validate latitude and longitude ranges
- Preserve the original raw dataset

## Analysis Areas

### Market Overview

- Total listings
- Listing distribution by neighbourhood
- Room-type mix
- Average and median nightly price

### Pricing

- Price distribution
- Price by room type
- Price by neighbourhood
- Outlier analysis

### Availability

- Average availability
- High-availability listings
- Availability by neighbourhood and room type

### Reviews

- Review counts
- Review activity by neighbourhood
- Reviews versus price / availability

### Host Analysis

- Hosts with multiple listings
- Listing concentration
- Professional versus single-listing host patterns

## Visualizations

The completed analysis should include:

- Listings by neighbourhood
- Room-type distribution
- Average price by room type
- Median price by neighbourhood
- Price distribution
- Availability distribution
- Price versus review activity
- Host listing concentration
- Geographic listing map

## SQL

The `sql/` directory contains SQL versions of the main analytical questions so the project demonstrates both Python and SQL workflows.

## Dashboard Plan

A professional dashboard should contain four views:

**1. Market Overview** — KPIs, listings by neighbourhood and room-type mix.

**2. Pricing Analysis** — average/median price, price distribution and neighbourhood comparison.

**3. Availability & Reviews** — availability, review activity and listing engagement.

**4. Geographic Analysis** — Albany listing map with neighbourhood and room-type filters.

## Reproducibility

1. Download the Albany dataset from Inside Airbnb.
2. Place the raw files under `data/raw/`.
3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run the cleaning pipeline.
5. Run the exploratory analysis.
6. Review generated tables and visualizations.
7. Load the prepared data into Power BI/Tableau if building the interactive dashboard.

## Important Data Integrity Rule

The project uses **Albany, New York** data. It must not be described as New York City data. Keeping the repository title, README, dataset and conclusions aligned is essential for a credible portfolio.

## Limitations

- Airbnb data is a market snapshot and does not represent every accommodation in Albany.
- Listing price is not the same as final booking price.
- Listing availability does not guarantee actual occupancy.
- Review counts are influenced by guest behaviour and listing age.
- Correlation does not establish causation.

## Skills Demonstrated

**Python · Pandas · NumPy · Data Cleaning · EDA · Data Visualization · SQL · Data Quality · Business Analysis · Reproducible Analytics**

## Author

**Nithesh S**  
GitHub: https://github.com/nitheshstech-dev

## License

MIT
