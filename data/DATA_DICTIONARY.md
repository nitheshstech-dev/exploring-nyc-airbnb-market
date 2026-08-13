# Albany Airbnb Data Dictionary

## Listings

| Field | Meaning | Typical use |
|---|---|---|
| `id` | Unique listing identifier | Listing counts / joins |
| `name` | Listing name | Descriptive analysis |
| `host_id` | Host identifier | Host analysis |
| `host_name` | Host display name | Host-level profiling |
| `neighbourhood_group` | Higher-level geographic area when provided | Geographic comparison |
| `neighbourhood` | Albany neighbourhood/ward label | Location analysis |
| `latitude` | Listing latitude | Mapping |
| `longitude` | Listing longitude | Mapping |
| `room_type` | Room/accommodation type | Market segmentation |
| `price` | Nightly listed price | Pricing analysis |
| `minimum_nights` | Minimum nights required | Booking constraints |
| `number_of_reviews` | Total reviews | Listing activity |
| `last_review` | Date of most recent review | Recency analysis |
| `reviews_per_month` | Average monthly review rate where available | Activity analysis |
| `calculated_host_listings_count` | Listings associated with host | Host concentration |
| `availability_365` | Days available in a year | Availability analysis |

## Calendar

Calendar data can be used for date-level availability and price analysis. Keep the calendar source separate because it can be much larger than the listing table.

## Reviews

Review records contain listing/date/reviewer-level information and can be aggregated to understand review activity and recency.

## Neighbourhoods

Neighbourhood files support geographic grouping and mapping.

## Data Quality Checks

Before analysis, check:

- duplicate IDs
- missing price values
- non-positive prices
- invalid coordinates
- availability outside 0–365
- invalid dates
- missing room types
- inconsistent neighbourhood labels
