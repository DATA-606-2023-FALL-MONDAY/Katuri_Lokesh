# Title and Author

| **Project Title**                    | Uncovering Influential Factors and Predictive Modeling of Area Deprivation Index |
|-------------------------------------|------------------------------------------------------------------------------------|
| **Prepared for**                     | UMBC Data Science master’s degree Capstone by Dr. Chaojie (Jay) Wang             |
| **Author Name**                      | Lokesh Katuri                                                                      |
| **Link to the author’s GitHub profile** | [Lokesh926 GitHub Profile](https://github.com/Lokesh926)                            |

# Background

The Area Deprivation Index (ADI) is a well-established tool for identifying areas of deprivation and affluence within a community. Comprising 17 indicators drawn from the American Community Survey (ACS), the ADI has been extensively researched in peer-reviewed literature since 2003 and has been employed by the Health Resources and Services Administration (HRSA) for two decades. High levels of deprivation, as measured by the ADI, have been associated with adverse health outcomes, including increased 30-day hospital readmission rates, cardiovascular disease deaths, cervical cancer incidence, overall cancer mortality, and all-cause mortality. These 17 indicators within the ADI encompass various aspects of income, education, employment, and housing conditions, all assessed at the Census Block Group level.

**Project Objective:**

The primary objective of this project is to identify and assess the key factors that have the most significant influence on the Area Deprivation Index (ADI).

**Why It Matters:**

Identifying influential factors for the Area Deprivation Index (ADI) is vital for targeted interventions, efficient resource allocation, healthcare planning, evidence-based policymaking, promoting social equity, and advancing research in addressing socio-economic disparities and health outcomes.

**Research Questions:**

1. Which specific socio-economic and demographic factors contribute most significantly to variations in the Area Deprivation Index (ADI)?
2. How do these influential factors interact and affect the ADI at different geographic scales?
3. Can predictive models be developed to forecast changes in ADI based on these key factors, enabling proactive policy and intervention planning?

# Data

The ADI dataset, accessible via BigQuery for the years 2018-2020, is reported as percentiles ranging from 0% to 100%, with 50% representing the midpoint of socioeconomic status nationally. This dataset offers insights at the county, ZIP code, and Census Block Group levels, making it a versatile tool for examining socio-economic disparities. It highlights neighborhood and racial inequalities, with higher ADI percentiles indicating greater deprivation and lower ones indicating affluence. The dataset provides raw ADI scores and additional statistics, and it offers data visualization options through the ADI story on BroadStreet, accessible with a free account. This resource is invaluable for understanding and addressing disparities within communities.

**Data Sources:** [BigQuery Public Data: BroadStreet ADI](https://console.cloud.google.com/marketplace/product/broadstreet-public-data/adi?project=kubernates-296012)

**Data Size:** 

| **Table Name**                      | **Data Volume**           | **Storage Size**  |
|-------------------------------------|---------------------------|--------------------|
| area_deprivation_index_by_census_block_group | 653,217 rows x 10 columns | 79.29 MB           |
| area_deprivation_index_by_county     | 9,426 rows x 8 columns   | 654.53 KB          |
| area_deprivation_index_by_zipcode    | 98,967 rows x 5 columns  | 4.71 MB            |

**Target/Label for ML Model:** `area_deprivation_index_percent`

**Potential Features/Predictors for ML Models:** Other indicators in the three tables
