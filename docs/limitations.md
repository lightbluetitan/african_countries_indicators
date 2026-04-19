# Limitations

This document outlines the known limitations of the **African Countries: A Curated Dataset on Africa Indicators for Education and Data Science** to ensure its proper use in research and educational projects.

## 1. Scope of Coverage

This dataset is strictly limited to **geographic, demographic, and administrative indicators** for the 54 sovereign nations of the African continent.

- It does NOT include economic indicators such as GDP, inflation, unemployment, or trade data.
- It does NOT include social indicators such as literacy rate, life expectancy, or Human Development Index (HDI).
- Users requiring broader socioeconomic indicators should consult specialized sources such as the World Bank, UNDP, or the African Development Bank.

## 2. Statistical Granularity

This dataset focuses exclusively on **country-level indicators**, providing one record per sovereign nation.

- It does NOT include subnational data such as provinces, states, or cities.
- It does NOT include time-series data; each variable represents a single point-in-time measurement.
- Users requiring historical trends or subnational breakdowns should consult specialized databases.

## 3. Temporal Snapshot

The variables `area_km2` and `population` reflect the most recent data available from the World Bank Group, updated to **2023** and **2024** respectively.

- All remaining variables represent current internationally recognized values at the time of dataset creation (2026).
- Future demographic or geopolitical changes are not reflected in the current version (v1.0.0).
- Updates will be incorporated as new versioned releases following Semantic Versioning conventions.

## 4. Regional Classification

The variable `region` follows the **United Nations geoscheme for Africa**, grouping countries into five sub-regions: Northern Africa, Western Africa, Central Africa, Eastern Africa, and Southern Africa.

- Alternative regional classifications (e.g., African Union zones or World Bank regions) may differ from those used in this dataset.
- Users applying different regional frameworks will need to apply their own mapping or crosswalk table.

## 5. Non-Official Status

Although this dataset was built upon official and recognized sources (World Bank, World Atlas, ISO, Google Developers), this specific curated version is maintained by an **independent researcher**.

- It should be treated as a technical standardization for research and educational purposes, and not as an official publication of any international organization.
- Users are encouraged to verify critical figures against primary sources before use in formal publications.