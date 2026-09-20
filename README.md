# Spatial and Temporal Dashboard

## Purpose
A static visualization examining how average surface temperatures changed across world regions between 1901 and 2016.

## Methods
A choropleth map provides the geographic overview, while a time-series view and monthly temperature-difference table add temporal context. The final design compares 30-year averages, including a 1960–1990 reference period, rather than relying on a single long-run average. Red indicates higher temperatures and blue indicates lower temperatures relative to the comparison shown.

## Output
- `spatial-and-temporal-dashboard.png` — final static dashboard image.
- `project-notes.md` — concise project narrative and provenance notes.

## Visualization

![Spatial and temporal temperature dashboard](spatial-and-temporal-dashboard.png)

*Static dashboard comparing regional temperature patterns, time series, and monthly differences.*

## Data sources and permissions
The underlying climate data were sourced from the World Bank Group Climate Change Knowledge Portal. This repository contains the final visualization and a sanitized narrative, not the original source tables. Check the current portal terms and attribution guidance before reuse.

## Limitations
The image is a static export and does not preserve the original dashboard interactions. Country-level aggregation can conceal local variation, missing values, and methodological differences. The display is descriptive and does not establish causes of temperature change.

## Reproducibility
The original dashboard build environment and source data are not included. Reproduction requires obtaining the relevant portal data, documenting the download date and transformations, computing comparable 30-year averages, and rebuilding the map, time series, and monthly comparison table.
