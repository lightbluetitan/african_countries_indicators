[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19647480.svg)](https://doi.org/10.5281/zenodo.19647480)

# African Countries: A Curated Dataset on Africa Indicators for Education and Data Science

## Description

This **curated dataset** provides a comprehensive geographic, demographic, and socioeconomic overview of all 54 sovereign nations on the African continent.

Unlike raw data exports, this resource is the result of a meticulous process of **research and data selection**. It captures key indicators for every African country, including geographic identifiers, regional classification, spatial coordinates, land area, and population figures, making it suitable for educational analysis, data visualization, and applied data science projects.

The purpose of this resource is to serve as a **foundational reference table** for educators, students, and researchers, providing a clean, verified, and technically robust starting point for any project involving African countries and their indicators.

## Language and Encoding

To ensure maximum technical compatibility and international reach, this dataset follows these standards:

1. **Metadata in English:** All variable names (column headers) are in English (e.g., `country_name`, `region`, `population`), facilitating seamless integration with global data science libraries in R and Python.
2. **Data Integrity:** The records maintain their geographic and demographic accuracy, using international nomenclature for countries, regions, and ISO 3166-1 alpha-3 codes.
3. **Encoding:** The files were validated using `readr::guess_encoding()` in R, which detected **pure ASCII encoding (confidence = 1.0)**. Since ASCII is a strict subset of UTF-8, the dataset is fully compatible with UTF-8 environments across Windows, macOS, and Linux without risk of character corruption.
4. **Cross-Platform Compatibility (R and Python):** Both formats were successfully imported in R and Python without errors or warnings. In **R**, the `.xlsx` and `.csv` files were loaded using `readxl::read_excel()` and `readr::read_csv()` respectively, correctly parsing all 54 rows and 10 columns — 5 character (`country_name`, `iso_alpha3`, `capital`, `region`, `landlocked`) and 5 numeric (`id`, `latitude`, `longitude`, `area_km2`, `population`). In **Python**, both files were imported via `pandas.read_csv()` and `pandas.read_excel()`, yielding identical DataFrames. The dataset is ready for immediate use in standard data science workflows across Windows, macOS, and Linux.
5. **Geospatial Validation (R and Python):** The `latitude` and `longitude` variables were validated beyond simple import testing. In **R**, interactive maps were successfully generated using the `leaflet` package, correctly plotting all 54 African countries. In **Python**, equivalent maps were produced using the `folium` library, yielding identical geospatial results. Both libraries confirmed the accuracy and integrity of the coordinate data for mapping workflows.

## Data Structure

The dataset is provided in `.csv` and `.xlsx` formats, containing the following variables:

| Variable | Type | Description |
| :--- | :--- | :--- |
| `id` | Integer | Unique numeric identifier for each country (1 to 54). |
| `country_name` | String | Full official name of the African country. |
| `iso_alpha3` | String | ISO 3166-1 alpha-3 three-letter country code (e.g., `DZA`, `AGO`, `KEN`). |
| `capital` | String | Name of the country's capital city. |
| `region` | String | African sub-region classification (e.g., Northern Africa, Western Africa). |
| `latitude` | Float | Geographic latitude coordinate of the country's centroid (decimal degrees). |
| `longitude` | Float | Geographic longitude coordinate of the country's centroid (decimal degrees). |
| `landlocked` | Boolean | Indicates whether the country is landlocked (`TRUE`) or has coastal access (`FALSE`). |
| `area_km2` | Integer | Total land area of the country in square kilometers. |
| `population` | Integer | Estimated total population of the country. |

## Data Curation

1. **Data Source:** Information validated against official records from the following sources:
   - [World Bank Group – Surface area (sq. km)](https://data.worldbank.org/indicator/AG.SRF.TOTL.K2)
   - [World Bank Group – Population, total](https://data.worldbank.org/indicator/SP.POP.TOTL)
   - [World Atlas – Landlocked Countries in Africa](https://www.worldatlas.com/articles/landlocked-countries-in-africa.html)
   - [Google Developers – Latitude and Longitude](https://developers.google.com/public-data/docs/canonical/countries_csv)
   - [Countries of the World – List of African Capitals](https://www.countries-ofthe-world.com/capitals-of-africa.html)
   - [Countries of the World – List of Countries in Africa](https://www.countries-ofthe-world.com/countries-of-africa.html)
   - [World Atlas – Regions of Africa](https://www.worldatlas.com/geography/regions-of-africa.html)
   - [ISO Online Browsing Platform (OBP) – Country Codes (iso_alpha3)](https://www.iso.org/obp/ui/#search)

2. **Normalization:** Column names use `snake_case` for easy calling in Python, R, and SQL functions.

3. **Interoperability:** Both `.csv` and `.xlsx` formats were tested in R and Python without errors. See *Language and Encoding, item 4* for full details.

4. **Purpose:** This dataset was created to provide a **valuable digital asset** for end users of R, Python, and SQL, offering a clean and ready-to-use resource that can be immediately integrated into data analysis, visualization, and educational workflows.

5. **Data Currency:** The variables `area_km2` and `population` reflect the most recent data available from the World Bank Group, with `area_km2` updated to **2023** and `population` updated to **2024**, ensuring the dataset represents current figures for all 54 African countries.

## License

This dataset is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to share and adapt the material as long as appropriate credit is given.

## Author

**Renzo Caceres Rossi**
- **ORCID:** [0009-0005-0744-854X](https://orcid.org/0009-0005-0744-854X)
- **GitHub:** [lightbluetitan](https://github.com/lightbluetitan)