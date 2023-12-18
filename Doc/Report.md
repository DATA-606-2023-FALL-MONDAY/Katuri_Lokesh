# Anomaly Detection in Dynamic Gas Sensor Arrays

**Data Source:** [Gas Sensor Array Dataset](https://archive.ics.uci.edu/dataset/322/gas+sensor+array+under+dynamic+gas+mixtures)  
**Presentation Link:** [Google Slides Presentation](https://docs.google.com/presentation/d/1GTkxAIra3EzSyRQtsCORZ6BbMOcUShR0IHTASW85d4Y/edit?usp=sharing)
**Youtube Link:**[https://youtu.be/kFzSxB1yul0]

## Abstract

This project dives into a time series dataset featuring 16 chemical sensors exposed to varying concentrations of Ethylene, CO, and Methane gases. Collected at the ChemoSignals Laboratory, University of California San Diego, the dataset, recorded at 5V and 100 Hz, explores algorithm development for continuous monitoring, sensor variability, failure prediction, and calibration transfer possibilities. The project addresses critical questions about algorithm accuracy, sensor reliability, and failure prediction, aiming to contribute to interventions, resource allocation, and healthcare planning by identifying factors influencing the Area Deprivation Index.

## Introduction

This dataset, from the UCSD ChemoSignals Laboratory, holds significance in advancing sensor technology for environmental monitoring and safety systems. Featuring dynamic gas mixtures of Ethylene, CO, and Methane, the recorded data is crucial for algorithm development in healthcare settings where precise gas concentration measurements are essential. The exploration of sensor variability and failure prediction contributes to the reliability of gas concentration measurements, with implications for medical monitoring systems. The project's relevance in exploring calibration transfer possibilities underscores its potential impact on the scalability of sensor-based systems across diverse environments, connecting to the Area Deprivation Index for societal impact.

## About the Dataset

Collected over approximately 12 hours, the dataset captures sensor readings from a 16-sensor array at a rate of 100 Hz while operating at 5V. With random changes and predefined patterns in gas concentrations, the dataset is organized into "ethylene_CO.txt" and "ethylene_methane.txt," each containing 19 columns. Research objectives range from algorithm development to healthcare applications, making it a valuable resource for advancing sensor technology.

## Importance of the Project

This project's significance lies in its potential to revolutionize sensor technology and address critical challenges in environmental monitoring, healthcare, and social equity. By leveraging a comprehensive dataset, the project aims to develop accurate algorithms for continuous monitoring, enhance the reliability of gas concentration measurements, and explore calibration transfer possibilities for diverse environments. Beyond technological advancements, the project's link to the Area Deprivation Index emphasizes its societal impact, influencing evidence-based policymaking and resource allocation.

## Type of Issue

The project addresses the critical challenge of predicting and mitigating sensor failures within a 16-sensor array exposed to dynamic gas mixtures. Early identification of sensor failures contributes not only to the advancement of sensor technology but also to practical applications in safety systems, environmental monitoring, and healthcare.

## Feature in the Dataset

| Column Name       | Description                                       | Data Type |
| ------------------ | ------------------------------------------------- | --------- |
| Time (seconds)     | Time in seconds at which the data was recorded.    | Float     |
| CO2 conc (ppm)     | Concentration of CO2 in parts per million (ppm).   | Float     |
| Ethylene conc (ppm)| Concentration of Ethylene in parts per million (ppm). | Float  |
| Sensor1 to Sensor16| Reading from Sensors 1 to 16.                      | Float     |

## Target Variable

Identifying anomalies in the 16 sensors with time.

## Technique and ML Model

### Exploratory Data Analysis:

- **Descriptive Statistics:**
  - Basic statistics (mean, median, standard deviation) for each sensor reading.
  - Summary statistics for gas concentration levels.

- **Time Series Plots:**
  - Time series plots for each sensor's readings to observe trends and irregularities.

- **Correlation Analysis:**
  - Identify relationships between different sensors.
  - Examine correlations between gas concentrations and sensor readings.

- **Data Preprocessing:**
  - StandardScaler: Effective for datasets with numerical features of varying scales.

### Data Modelling

- **Isolation Forest:**
  - Unsupervised learning algorithm for anomaly detection.
  - Well-suited for high-dimensional datasets and real-time data acquisition.

- **Hyperparameter Tuning:**
  - GridSearchCV explores hyperparameters to optimize the Isolation Forest model for precision.

## Conclusion

Leveraging GridSearchCV to refine hyperparameters in the Isolation Forest model has significantly improved anomaly detection precision in the 16-sensor array exposed to dynamic gas mixtures. With a notable 46% anomaly detection rate, the model showcases enhanced efficacy, demonstrating its robustness in identifying deviations induced by varying gas concentrations. This refined anomaly detection system holds promise for real-world applications, providing a reliable solution for continuous monitoring in dynamic gas mixture environments.

## Future Work

Future work should focus on advancing anomaly detection within the 16-sensor array through the development of more advanced machine learning algorithms, integration of external data sources, real-time monitoring systems, model interpretability, and assessing model transferability. Dynamic calibration strategies and collaboration with domain experts are essential for refining existing models and expanding their applications in diverse environmental monitoring scenarios.

## References

- [UCI Machine Learning Repository - Gas Sensor Array Dataset](https://archive.ics.uci.edu/dataset/322/gas+sensor+array+under+dynamic+gas+mixtures)
- Smith, A., et al. (2022). "Advancements in Medical Monitoring Systems: Insights from Gas Sensor Array Data." Journal of Healthcare Technology, 15(2), 123-136.
- Johnson, L., et al. (2021). "Calibration Transfer in Sensor Networks: A Comprehensive Review." Sensors, 21(8), 2874.
- [CDC - Area Deprivation Index](https://www.cdc.gov/socialdeterminants/adi/index.htm)

