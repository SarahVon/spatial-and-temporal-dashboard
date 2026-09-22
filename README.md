# Global Surface Temperature Change Dashboard

This **Tableau** dashboard examines how average surface temperatures changed around the world between **1901 and 2016**. It combines a country-level choropleth map, a global time series, summary indicators, and a monthly comparison table so viewers can explore the same long-term pattern from spatial and temporal perspectives.

The central comparison uses two 30-year periods, **1901–1930** and **1987–2016**, rather than relying on a single average across the full 115-year record. This makes the direction and magnitude of long-term temperature differences easier to interpret while reducing the influence of individual-year variability.

## Project goals

- Compare long-term average surface temperatures between an early and recent 30-year period.
- Show how temperature change varies geographically across countries.
- Place those spatial differences within the full 1901–2016 global time series.
- Compare changes by month to determine whether the overall pattern is consistent throughout the year.
- Use a 1960–1990 reference period to provide historical context for the time series.
- Design a dashboard that communicates a complex global pattern without requiring specialized climate-science knowledge.

## Dashboard

![Global surface temperature change dashboard](spatial-and-temporal-dashboard.png)

*Static export of the Tableau dashboard showing country-level temperature differences, the global annual time series, change-category counts, and monthly comparisons.*

## Data source and scope

The analysis uses historical climate data from the [World Bank Group Climate Change Knowledge Portal](https://climateknowledgeportal.worldbank.org/), a platform providing access to global historical and projected climate information. The dashboard focuses on average surface temperature observations from **1901 through 2016**.

The data was summarized into several related measures:

| Measure | Purpose in the dashboard |
| --- | --- |
| 1901–1930 average | Establishes the early-period temperature baseline |
| 1987–2016 average | Represents the most recent 30-year period available in the source used for this project |
| Difference between the two periods | Drives the country map and increase/decrease classification |
| Annual global average, 1901–2016 | Shows the longer-term temporal pattern without reducing the record to two periods |
| 1960–1990 average | Provides the reference line for interpreting the annual time series |
| Monthly temperature differences | Shows how the early-to-recent change varies across the calendar year |

The repository contains the final dashboard image and project documentation, not the original source tables or Tableau workbook. Current climate data can be accessed through the portal's [download page](https://climateknowledgeportal.worldbank.org/download-data).

## Tools and methods

I built the dashboard in **Tableau** using the following techniques:

- Data preparation and temporal aggregation
- Calculated fields for period-to-period temperature differences
- Country-level choropleth mapping
- Diverging color encoding
- Annual time-series visualization
- Custom reference-line calculation
- Monthly comparison table
- Summary counts by direction of change
- Dashboard filters and layout design

## Dashboard design

### Country-level temperature map

The choropleth map is the dashboard's main visual anchor. Each country is colored according to the difference between its **1901–1930** and **1987–2016** average temperatures. Blue represents a decrease and orange-red represents an increase, allowing the direction of change to be understood before reading individual values.

The map is paired with a country-selection control for more focused exploration in the original Tableau dashboard. A summary panel also counts countries by direction of change, providing a concise complement to the geographic pattern.

### Global time series

The line chart displays annual global average temperature across the full 1901–2016 record. A custom reference line marks the **1960–1990 average**, making it easier to see when annual values fall below or rise above that historical benchmark.

The line color follows the same cool-to-warm visual language as the map. This connects the temporal and spatial views while making the more recent concentration of above-reference values immediately visible.

### Monthly comparison

The table compares monthly averages from 1901–1930 with those from 1987–2016. Showing all twelve months separately adds detail that an annual average would conceal and makes it possible to assess whether the change is concentrated in one season or appears throughout the year.

The supporting temperature scale also identifies the 1960–1990 average as its midpoint, maintaining a consistent reference across the dashboard.

## Key findings

The dashboard shows a broad increase in average surface temperature across the available countries and time periods:

- **190 countries** were classified as having an increase between the two 30-year periods, compared with **5 countries** showing a decrease.
- The mapped country-level differences range from approximately **-0.30°C to +1.77°C**.
- Every month shows a positive difference between the early and recent periods.
- Monthly changes range from **+0.77°C in September** to **+1.04°C in April**.
- The annual time series shows recent values consistently above the 1960–1990 reference average, with the highest values appearing near the end of the record.

Together, the views show that the observed increase is geographically widespread, visible across the annual record, and present in every month. The dashboard describes these patterns but does not attempt to attribute them to individual causes or project future temperatures.

## Design development

The project changed substantially from its initial version. My first approach used a single 115-year average, but that measure obscured meaningful differences between the beginning and end of the record. Replacing it with two comparable 30-year averages produced a clearer and more defensible long-term comparison.

I applied the same period structure to the map and monthly table, then added the 1960–1990 reference line to strengthen the time-series context. I also simplified the original interaction model. The map initially filtered the other views, but separating the components allowed each one to communicate its own level of analysis without causing the global charts to shift unexpectedly after a country selection.

These revisions made the dashboard more focused and reinforced an important design lesson: interactivity is most useful when it supports the analytical question, not simply because the software makes it available.

## Interpretation and limitations

- The dashboard presents descriptive historical comparisons; it is not a forecasting or climate-attribution model.
- Country-level averages can conceal substantial variation within national boundaries.
- The two 30-year periods summarize long-term conditions but do not capture every short-term fluctuation or extreme event.
- Results depend on the countries, coverage, processing, and definitions in the source data used for the project.
- The choropleth gives large countries more visual prominence because of their land area, not because their temperature change is necessarily greater.
- The repository image is static, so the original Tableau selection controls, tooltips, and underlying values are not available.

The dashboard is best interpreted as an exploratory visualization of historical surface-temperature patterns and a demonstration of spatial, temporal, and multiview dashboard design.

## Repository contents

```text
spatial-and-temporal-dashboard.png   Static Tableau dashboard export
README.md                            Project overview, methods, and interpretation
```

Exact reproduction would require the original source extract, transformation steps, geographic matching choices, calculated fields, and Tableau workbook. With those materials, the project can be rebuilt by calculating the two 30-year climatologies, joining the country-level results to geographic boundaries, reconstructing the annual and monthly views, and applying the shared reference periods and color encodings.
