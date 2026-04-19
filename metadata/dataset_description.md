# Dataset Description: African Countries: A Curated Dataset on Africa Indicators for Education and Data Science

## 1. Overview

This curated dataset provides a comprehensive geographic, demographic, and administrative overview of all 54 sovereign nations on the African continent. The dataset is designed to serve as a foundational reference table for educators, students, researchers, and data scientists working on projects related to African countries and their indicators.

Each record corresponds to a single sovereign nation and documents its official name, ISO 3166-1 alpha-3 code, capital city, sub-regional classification, geographic coordinates, land area, landlocked status, and total population. The dataset covers all five African sub-regions: Northern Africa (6 countries), Western Africa (16 countries), Eastern Africa (18 countries), Central Africa (9 countries), and Southern Africa (5 countries), and correctly identifies 16 landlocked nations.

The dataset is provided in two interoperable formats — `.csv` and `.xlsx` — both validated for encoding, structural integrity, and cross-platform compatibility in R and Python.

## 2. Context and Rationale

Africa is the world's second-largest continent by both area and population, yet high-quality, ready-to-use datasets covering all 54 sovereign nations with clean and standardized indicators remain scarce in public repositories. Publicly available sources frequently suffer from common data quality issues: inconsistent country naming conventions, missing values, non-standardized column headers, and a lack of documented validation methodology.

This dataset was created to address those limitations. Rather than relying on automated data exports or web scraping, the records were manually researched and validated against official and recognized sources — including the World Bank, World Atlas, ISO, and Google Developers — ensuring that each entry reflects accurate and current information for every African country.

The rationale for curating this dataset in two formats (`.csv` and `.xlsx`) stems from the need to serve a broad audience: from researchers working in R and Python to analysts using spreadsheet-based tools. Both formats have been validated for encoding integrity (pure ASCII, fully UTF-8 compatible) and successfully imported across multiple platforms without errors or warnings.

This resource is intended to function as a clean, verified, and technically robust foundation for any analytical, educational, or research project involving African countries and their indicators.

## 3. Scope and Coverage

This dataset covers all 54 sovereign nations of the African continent, classified across five sub-regions following the United Nations geoscheme for Africa.

**In scope:**
- All 54 sovereign African nations
- Official country names and ISO 3166-1 alpha-3 codes
- Capital cities and sub-regional classifications (UN geoscheme)
- Geographic coordinates (latitude and longitude) for each country's centroid
- Total land area in square kilometers (World Bank, 2023)
- Total population estimates (World Bank, 2024)
- Landlocked status for all 54 countries

**Out of scope:**
- Subnational data such as provinces, states, or cities
- Economic indicators such as GDP, inflation, or trade data
- Social indicators such as literacy rate, life expectancy, or HDI
- Time-series or historical demographic data
- Data for African territories that are not sovereign nations

## 4. Methodology

The data was compiled through the following process:

1. **Research:** Indicators for all 54 African countries were individually researched using official and recognized sources, including the World Bank, World Atlas, ISO Online Browsing Platform, Google Developers, and Countries of the World.
2. **Curation:** Each record was manually reviewed to ensure geographic and demographic accuracy, with particular attention to the use of internationally recognized country names and ISO 3166-1 alpha-3 codes.
3. **Normalization:** All variable names were standardized using `snake_case` convention to ensure seamless integration with data science workflows in R, Python, and SQL.
4. **Validation:** The dataset was cross-checked record by record against official sources to verify the accuracy of all indicators, including coordinates, regional classifications, land area, and population figures.
5. **Encoding Verification:** Files were tested using `readr::guess_encoding()` in R, confirming pure ASCII encoding (confidence = 1.0), fully compatible with UTF-8 environments.
6. **Compatibility Testing:** Both `.csv` and `.xlsx` formats were successfully imported in R (`readxl`, `readr`, `leaflet`) and Python (`pandas`, `folium`) without errors or warnings across Windows, macOS, and Linux.

## 5. Maintenance

This dataset is maintained by its author, **Renzo Caceres Rossi** ([arenzocaceresrossi@gmail.com](mailto:arenzocaceresrossi@gmail.com)), as part of an independent research initiative. Periodic reviews are conducted to ensure the continued accuracy and integrity of the records.

Future updates will be incorporated as new versioned releases following Semantic Versioning conventions:

- **v1.x.x** — Minor updates, such as correcting existing records or updating demographic figures.
- **v2.0.0** — Major release, reserved for significant structural changes to the dataset (e.g., new variables or format changes).

All release history and version changes will be documented in the project's GitHub repository at [african_countries_indicators](https://github.com/lightbluetitan/african_countries_indicators).

## 6. Terms of Use

This documentation and the accompanying data are provided under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to share, copy, redistribute, and adapt the material for any purpose, provided that appropriate credit is given to the author, a link to the license is provided, and any changes made are indicated. Full license terms are available at [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/) and in the `LICENSE` file included in this repository.