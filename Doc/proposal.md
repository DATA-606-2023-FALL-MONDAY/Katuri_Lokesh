# Title and Author

| **Project Title**                    | Gas sensor array under dynamic gas mixtures Index |
|-------------------------------------|------------------------------------------------------------------------------------|
| **Prepared for**                     | UMBC Data Science master’s degree Capstone by Dr. Chaojie (Jay) Wang             |
| **Author Name**                      | Lokesh Katuri                                                                      |
| **Link to the author’s GitHub profile** | https://github.com/Lokesh926                           |

# Background

This dataset contains time series data from 16 chemical sensors exposed to gas mixtures with varying concentrations. It was collected at the ChemoSignals Laboratory at the University of California San Diego. The sensors operated at 5V and recorded data at 100 Hz. Concentration levels changed randomly, with various transitions, and predefined patterns were also included. The gases in the mixtures were Ethylene (0-20 ppm), CO (0-600 ppm), and Methane (0-300 ppm).

**Project Objective:**

The primary objective of this project is to develop algorithms for continuous monitoring, study sensor variability, assess sensor failures, and explore calibration transfer possibilities.

**Why It Matters:**

Identifying influential factors for the Area Deprivation Index (ADI) is vital for targeted interventions, efficient resource allocation, healthcare planning, evidence-based policymaking, promoting social equity, and advancing research in addressing socioeconomic disparities and health outcomes.

**Research Questions:**

Algorithm Development: How can we develop more accurate algorithms for interpreting sensor data and detecting changes in gas concentrations over time?

Sensor Variability: What is the extent of variability among sensors of the same type in the array, and how can this variability be accounted for in data analysis?

Sensor Failure Prediction: Can we predict when and how sensors might fail, and what are the implications for system performance?

Calibration Transfer: Is it possible to extend models developed for one sensor to other sensors in the array, and what are the limitations and benefits of doing so?

Pattern Recognition: How can we efficiently recognize and classify different concentration transitions and predefined patterns within the dataset?

Optimal Sampling Frequency: What is the optimal sampling frequency for sensor data acquisition to balance accuracy and resource usage?

Real-world Applications: How can the findings and models derived from this dataset be applied to real-world scenarios, such as environmental monitoring or industrial process control?

# Data

The ADI dataset, accessible via BigQuery for the years 2018-2020, is reported as percentiles ranging from 0% to 100%, with 50% representing the midpoint of socioeconomic status nationally. This dataset offers insights at the county, ZIP code, and Census Block Group levels, making it a versatile tool for examining socio-economic disparities. It highlights neighborhood and racial inequalities, with higher ADI percentiles indicating greater deprivation and lower ones indicating affluence. The dataset provides raw ADI scores and additional statistics, and it offers data visualization options through the ADI story on BroadStreet, accessible with a free account. This resource is invaluable for understanding and addressing disparities within communities.

**Data Sources:** [BigQuery Public Data: BroadStreet ADI](https://console.cloud.google.com/marketplace/product/broadstreet-public-data/adi?project=kubernates-296012)

**Data Size:** 
| **Table Name**                      | **Data Volume**           | **Storage Size**  |
|-------------------------------------|---------------------------|--------------------|
| area_deprivation_index_by_census_block_group | 653,217 rows x 10 columns | 79.29 MB           |
| area_deprivation_index_by_county     | 9,426 rows x 8 columns   | 654.53 KB          |
| area_deprivation_index_by_zipcode    | 98,967 rows x 5 columns  | 4.71 MB            |


### Table 1: `area_deprivation_index_by_census_block_group`

| Column Name                     | Data Type   | Nullable | Description                                       |
|---------------------------------|-------------|----------|---------------------------------------------------|
| geo_id                          | STRING      | YES      | Geographic ID or code                            |
| state_fips_code                 | STRING      | YES      | FIPS code for U.S. states                        |
| county_fips_code                | STRING      | YES      | FIPS code for counties within states             |
| block_group_fips_code           | STRING      | YES      | FIPS code for block groups                      |
| description                     | STRING      | YES      | Descriptive information                          |
| county_name                     | STRING      | YES      | Name of the county                               |
| state_name                      | STRING      | YES      | Name of the state                                |
| state                           | STRING      | YES      | State identifier or abbreviation                  |
| year                            | INTEGER     | YES      | Year of the data                                 |
| area_deprivation_index_percent   | FLOAT       | YES      | Percentage-based area deprivation index          |

### Table 2: `area_deprivation_index_by_county`

| Column Name                     | Data Type   | Nullable | Description                                       |
|---------------------------------|-------------|----------|---------------------------------------------------|
| geo_id                          | STRING      | YES      | Geographic ID or code                            |
| state_fips_code                 | STRING      | YES      | FIPS code for U.S. states                        |
| county_fips_code                | STRING      | YES      | FIPS code for counties within states             |
| county_name                     | STRING      | YES      | Name of the county                               |
| state_name                      | STRING      | YES      | Name of the state                                |
| state                           | STRING      | YES      | State identifier or abbreviation                  |
| year                            | INTEGER     | YES      | Year of the data                                 |
| area_deprivation_index_percent   | FLOAT       | YES      | Percentage-based area deprivation index          |

### Table 3: `area_deprivation_index_by_zipcode`

| Column Name                     | Data Type   | Nullable | Description                                       |
|---------------------------------|-------------|----------|---------------------------------------------------|
| geo_id                          | STRING      | YES      | Geographic ID or code                            |
| zipcode                         | STRING      | YES      | ZIP code                                         |
| description                     | STRING      | YES      | Descriptive information                          |
| year                            | INTEGER     | YES      | Year of the data                                 |
| area_deprivation_index_percent   | FLOAT       | YES      | Percentage-based area deprivation index          |

**Target/Label for ML Model:** `area_deprivation_index_percent`

**Potential Features/Predictors for ML Models:** Other indicators in the after analysis from three tables.
