# Spatial and Temporal Dashboard

A static visualization examining average surface temperatures across world regions between 1901 and 2016.

## Contents

- [Purpose and questions](#purpose-and-questions)
- [Data and time periods](#data-and-time-periods)
- [Workflow](#workflow)
- [Visualization sequence](#visualization-sequence)
- [Results and interpretation](#results-and-interpretation)
- [Limitations](#limitations)
- [Reproducibility](#reproducibility)
- [Repository contents](#repository-contents)

## Purpose and questions

The dashboard asks how regional average surface temperatures compare across time and how a spatial overview, time series, and monthly comparison complement one another. It is descriptive rather than a causal climate model.

## Data and time periods

I use climate data from the World Bank Group Climate Change Knowledge Portal. The analysis spans **1901–2016** and emphasizes comparable 30-year averages, including a **1960–1990 reference period**. I provide the final image and a sanitized narrative, not the source tables or dashboard build environment.

## Workflow

1. Obtain and prepare regional temperature observations.
2. Compute comparable 30-year averages and retain the 1960–1990 reference period.
3. Build a choropleth for geographic comparison.
4. Build a time-series view for change through the available periods.
5. Build a monthly temperature-difference table to compare seasonal detail.
6. Compose the views into one static dashboard export.

## Visualization sequence

### Spatial overview

The choropleth establishes geographic context, using red for higher and blue for lower temperatures relative to the comparison shown.

### Time and monthly comparison

The time series adds temporal context to the period comparisons. The monthly table adds seasonal detail that a single annual or multi-year average cannot show.

![Spatial and temporal temperature dashboard](spatial-and-temporal-dashboard.png)

*Static dashboard comparing regional temperature patterns, time series, and monthly differences.*

## Results and interpretation

The dashboard is designed to support comparisons between regional 30-year averages, the 1960–1990 reference, and monthly differences. It shows descriptive patterns in the supplied data; the static artifact does not support interactive inspection of individual values or a causal explanation for change.

## Limitations

Country- or region-level aggregation can conceal local variation, missing values, and methodological differences. A static export does not preserve the original dashboard interactions. The display should not be treated as a forecast or attribution analysis.

## Reproducibility

Reproduction requires obtaining the relevant portal data under current terms, recording the download date and transformations, computing comparable 30-year averages, and rebuilding the map, time series, and monthly comparison table. Exact values and formatting cannot be regenerated from the available outputs alone because the source tables and build environment are not included.

## Repository contents

- `spatial-and-temporal-dashboard.png` — static dashboard export
- `project-notes.md` — concise provenance and design notes
- `README.md` — methods, interpretation, and reproducibility boundary
