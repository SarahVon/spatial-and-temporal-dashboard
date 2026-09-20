# Spatial and Temporal Dashboard

A static visualization examining how average surface temperatures changed across world regions between 1901 and 2016.

## Analysis sequence

1. **Establish geographic context.** A choropleth map provides the global overview, using red for higher and blue for lower temperatures relative to the comparison shown.
2. **Compare time periods.** The design compares 30-year averages, including a 1960–1990 reference period, rather than relying on a single long-run average.
3. **Add temporal detail.** A time-series view and monthly temperature-difference table add context to the map and support comparisons across periods.

## Visualization

![Spatial and temporal temperature dashboard](spatial-and-temporal-dashboard.png)

*Static dashboard comparing regional temperature patterns, time series, and monthly differences.*

## Data sources and permissions

The underlying climate data were sourced from the World Bank Group Climate Change Knowledge Portal. This repository contains the final visualization and a sanitized narrative, not the original source tables. Check the current portal terms and attribution guidance before reuse.

## Limitations

The image is a static export and does not preserve the original dashboard interactions. Country-level aggregation can conceal local variation, missing values, and methodological differences. The display is descriptive and does not establish causes of temperature change.

## Reproducibility

The original dashboard build environment and source data are not included. Reproduction requires obtaining the relevant portal data, documenting the download date and transformations, computing comparable 30-year averages, and rebuilding the map, time series, and monthly comparison table.
