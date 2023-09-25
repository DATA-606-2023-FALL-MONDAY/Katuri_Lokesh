# Project Title and Author

- **Project Title:** "Uncovering Influential Factors and Predictive Modeling of Area Deprivation Index"
- **Prepared:** for UMBC Data Science Master's Degree Capstone by Dr. Chaojie (Jay) Wang
- **Author Name:** Lokesh Katuri
- **Author's GitHub Profile:** [Lokesh Katuri GitHub](https://github.com/Lokesh926)

# Background

The Area Deprivation Index (ADI) is a powerful tool used to identify areas of deprivation and affluence within communities. It comprises 17 indicators from the American Community Survey (ACS) and has been widely studied since 2003. The Health Resources and Services Administration (HRSA) has employed ADI for two decades. High ADI values are associated with adverse health outcomes, including increased hospital readmission rates, cardiovascular disease deaths, and overall cancer mortality. The 17 ADI indicators cover aspects like income, education, employment, and housing conditions, assessed at the Census Block Group level.

## Project Objective

This project aims to identify key factors influencing the Area Deprivation Index (ADI).

## Why It Matters

Understanding influential factors in ADI is essential for targeted interventions, efficient resource allocation, healthcare planning, evidence-based policymaking, and promoting social equity.

## Research Questions

1. Which socio-economic and demographic factors most significantly contribute to ADI variations?
2. How do these factors interact and affect ADI at different geographic scales?
3. Can predictive models forecast ADI changes based on these factors, enabling proactive policy and intervention planning?

# Data

- **Data Sources:** [BigQuery Public Data - BroadStreet ADI](https://console.cloud.google.com/marketplace/product/broadstreet-public-data/adi?project=kubernates-296012)

**Data Size:**

1. **Table:** bigquery-public-data.broadstreet_adi.area_deprivation_index_by_census_block_group
   - Data Volume: 653,217 rows x 10 columns
   - Storage Size: 79.29 MB

2. **Table:** bigquery-public-data.broadstreet_adi.area_deprivation_index_by_county
   - Data Volume: 9,426 rows x 8 columns
   - Storage Size: 654.53 KB

3. **Table:** bigquery-public-data.broadstreet_adi.area_deprivation_index_by_zipcode
   - Data Volume: 98,967 rows x 5 columns
   - Storage Size: 4.71 MB

## Target/Label for ML Model

- The target/label is the `area_deprivation_index_percent` column.

## Features/Predictors for ML Models

- Other indicators in the three tables serve as predictors.
