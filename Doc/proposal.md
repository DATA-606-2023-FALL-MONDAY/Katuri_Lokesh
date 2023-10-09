# Title and Author

| **Project Title**                   | Gas sensor array under dynamic gas mixtures Index |
|-------------------------------------|-----------------------------------------------------------------------------------|
| **Prepared for**                    | UMBC Data Science master’s degree Capstone by Dr. Chaojie (Jay) Wang              |
| **Author Name**                     | Lokesh Katuri                                                                     |
| **Link to the author’s GitHub profile**| https://github.com/Lokesh926                   |

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

There are two data files: "ethylene_CO.txt" and "ethylene_methane.txt," each containing recordings from sensors exposed to gas mixtures. Each file has 19 columns. The first column represents time (in seconds), the second column is Methane (or CO) concentration in ppm, the third column is Ethylene concentration in ppm, and the remaining 16 columns contain sensor readings. The sensor order is: TGS2602, TGS2602, TGS2600, TGS2600, TGS2610, TGS2610, TGS2620, TGS2620, TGS2602, TGS2602, TGS2600, TGS2600, TGS2610, TGS2610, TGS2620, TGS2620. Each file includes a header with column information.

**Data Sources:** [Gas sensor array under dynamic gas mixtures]
(https://archive.ics.uci.edu/dataset/322/gas+sensor+array+under+dynamic+gas+mixtures)

**Data Size:** 
| **Table Name**                      | **Data Volume**           | **Storage Size**  |
|-------------------------------------|---------------------------|--------------------|
|  ethylene_CO.txt                    | 4,208,261 rows x 19 column| 613.16 MB           |
| ethylene_methane.txt                | 4,178,504 rows x 19 columns| 608.74 MB          |



### Table 1: `ethylene_CO.txt`

| Column Name         | Description                                      | Data Type |
|---------------------|--------------------------------------------------|-----------|
| Time (seconds)     | Time in seconds at which the data was recorded.   | Float     |
| CO2 conc (ppm)      | Concentration of CO2 in parts per million (ppm). | Float     |
| Ethylene conc (ppm)| Concentration of Ethylene in parts per million (ppm).| Float  |
| Sensor1             | Reading from Sensor 1.                           | Float     |
| Sensor2             | Reading from Sensor 2.                           | Float     |
| Sensor3             | Reading from Sensor 3.                           | Float     |
| Sensor4             | Reading from Sensor 4.                           | Float     |
| Sensor5             | Reading from Sensor 5.                           | Float     |
| Sensor6             | Reading from Sensor 6.                           | Float     |
| Sensor7             | Reading from Sensor 7.                           | Float     |
| Sensor8             | Reading from Sensor 8.                           | Float     |
| Sensor9             | Reading from Sensor 9.                           | Float     |
| Sensor10            | Reading from Sensor 10.                          | Float     |
| Sensor11            | Reading from Sensor 11.                          | Float     |
| Sensor12            | Reading from Sensor 12.                          | Float     |
| Sensor13            | Reading from Sensor 13.                          | Float     |
| Sensor14            | Reading from Sensor 14.                          | Float     |
| Sensor15            | Reading from Sensor 15.                          | Float     |
| Sensor16            | Reading from Sensor 16.                          | Float     |


### Table 2: `ethylene_methane.txt`

| Column Name         | Description                                      | Data Type |
|---------------------|--------------------------------------------------|-----------|
| Time (seconds)     | Time in seconds at which the data was recorded.   | Float     |
| CO2 conc (ppm)      | Concentration of CO2 in parts per million (ppm). | Float     |
| Ethylene conc (ppm)| Concentration of Ethylene in parts per million (ppm).| Float  |
| Sensor1             | Reading from Sensor 1.                           | Float     |
| Sensor2             | Reading from Sensor 2.                           | Float     |
| Sensor3             | Reading from Sensor 3.                           | Float     |
| Sensor4             | Reading from Sensor 4.                           | Float     |
| Sensor5             | Reading from Sensor 5.                           | Float     |
| Sensor6             | Reading from Sensor 6.                           | Float     |
| Sensor7             | Reading from Sensor 7.                           | Float     |
| Sensor8             | Reading from Sensor 8.                           | Float     |
| Sensor9             | Reading from Sensor 9.                           | Float     |
| Sensor10            | Reading from Sensor 10.                          | Float     |
| Sensor11            | Reading from Sensor 11.                          | Float     |
| Sensor12            | Reading from Sensor 12.                          | Float     |
| Sensor13            | Reading from Sensor 13.                          | Float     |
| Sensor14            | Reading from Sensor 14.                          | Float     |
| Sensor15            | Reading from Sensor 15.                          | Float     |
| Sensor16            | Reading from Sensor 16.                          | Float     |

**Target/Label for ML Model:** The Goal is to understand the anomalies in the sensor behavior. 

**Potential Features/Predictors for ML Models:** All the sensor data will be considered.
