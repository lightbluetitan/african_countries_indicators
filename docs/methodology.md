# Methodology

This document describes the systematic process used to create the **African Countries: A Curated Dataset on Africa Indicators for Education and Data Science**.

## 1. Data Acquisition

Indicators for all 54 sovereign African countries were individually researched using official and recognized sources. The following references were consulted:

- [World Bank Group – Surface area (sq. km)](https://data.worldbank.org/indicator/AG.SRF.TOTL.K2)
- [World Bank Group – Population, total](https://data.worldbank.org/indicator/SP.POP.TOTL)
- [World Atlas – Landlocked Countries in Africa](https://www.worldatlas.com/articles/landlocked-countries-in-africa.html)
- [Google Developers – Latitude and Longitude](https://developers.google.com/public-data/docs/canonical/countries_csv)
- [Countries of the World – List of African Capitals](https://www.countries-ofthe-world.com/capitals-of-africa.html)
- [Countries of the World – List of Countries in Africa](https://www.countries-ofthe-world.com/countries-of-africa.html)
- [World Atlas – Regions of Africa](https://www.worldatlas.com/geography/regions-of-africa.html)
- [ISO Online Browsing Platform (OBP) – Country Codes (iso_alpha3)](https://www.iso.org/obp/ui/#search)

## 2. Data Curation and Normalization

To ensure geographic accuracy and technical interoperability, the following criteria were applied:

- **Geographic Integrity:** Country names, capital cities, and regional classifications follow internationally recognized nomenclature, using official ISO 3166-1 alpha-3 codes for standardized country identification.
- **Header Standardization:** All variable names were defined using `snake_case` (e.g., `country_name`, `area_km2`, `population`) to ensure seamless compatibility with Python, R, and SQL environments.
- **Regional Classification:** Countries were assigned to one of five African sub-regions (Northern, Western, Central, Eastern, and Southern Africa) following the United Nations geoscheme for Africa.
- **Data Currency:** The variables `area_km2` and `population` reflect the most recent data available from the World Bank Group, updated to **2023** and **2024** respectively.
- **Encoding:** All files were saved using **pure ASCII encoding**, fully compatible with UTF-8 environments across Windows, macOS, and Linux.

## 3. Quality Control (QA)

The final dataset underwent a multi-step validation process:

1. **Completeness Check:** Verified the presence of exactly 54 records, one per sovereign African nation, confirming full continental coverage.
2. **Schema Validation:** Ensured that all data types matched the definitions in the `data_dictionary.csv` — 5 String columns and 5 numeric columns.
3. **Null Value Check:** Confirmed zero null values across all 10 variables and 54 records.
4. **Cross-Source Validation:** Each record was cross-checked against multiple sources to verify the accuracy of country names, capitals, coordinates, regional classifications, and demographic figures.
5. **Encoding Verification:** Files were tested using `readr::guess_encoding()` in R, confirming pure ASCII encoding (confidence = 1.0).

## 4. Compatibility Testing

Both dataset formats were successfully imported in R and Python without errors or warnings:

- **R:** `.xlsx` loaded via `readxl::read_excel()` and `.csv` via `readr::read_csv()`, correctly parsing all 54 rows and 10 columns.
- **Python:** Both files imported via `pandas.read_csv()` and `pandas.read_excel()`, yielding identical DataFrames.

## 5. Geospatial Validation

The `latitude` and `longitude` variables were validated through interactive map generation:

- **R:** Interactive maps successfully generated using the `leaflet` package, correctly plotting all 54 African countries.
- **Python:** Equivalent maps produced using the `folium` library, yielding identical geospatial results.

Both libraries confirmed the accuracy and integrity of the coordinate data for mapping workflows.

## 6. Software and Tools

- **Data Processing:** Microsoft Excel / CSV
- **Validation:** R 4.x (`readr`, `readxl`, `leaflet`) and Python 3.x (`pandas`, `folium`)
- **Documentation:** Markdown 
- **Version Control:** Git / GitHub