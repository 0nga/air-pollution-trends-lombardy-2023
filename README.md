# Air Pollution Trends in Lombardy (Italy) – 2023

Comprehensive data analysis of air quality in the Lombardy region (Italy) for the year 2023, based on official public datasets provided by **ARPA Lombardia** (Regional Environmental Protection Agency).

This project investigates pollutant concentrations, evaluates compliance with Italian and European air quality standards, computes Air Quality Indices (AQI), and visualizes spatial and temporal patterns across all 12 provinces of Lombardy.

---

## Project Overview

Air pollution is one of the most critical environmental and public health challenges in Northern Italy. Lombardy, due to its geographical characteristics and high industrialization, frequently records pollutant concentrations among the highest in Europe.

This study aims to:

- Analyze annual and monthly trends of major atmospheric pollutants
- Assess compliance with regulatory limits
- Compute province-level Air Quality Index (AQI)
- Explore correlations among pollutants
- Identify the most and least polluted provinces
- Produce spatial visualizations using georeferenced monitoring station data

---

## Pollutants Analyzed

The analysis includes the following substances:

- PM10  
- PM2.5  
- NO2  
- NOx  
- NO  
- O3 (Ozone)  
- SO2  
- CO  
- Benzene (C6H6)  
- Ammonia (NH3)  
- Black Carbon  
- Lead (Pb)  
- Arsenic (As)  
- Cadmium (Cd)  
- Nickel (Ni)

---

## Data Source

Data were obtained from:

**ARPA Lombardia – Open Data Portal**  
Official regional monitoring stations (2023 datasets)

All rights belong to ARPA Lombardia.

---

## Methodology

The project workflow consists of:

### 1. Data Import & Cleaning
- Removal of duplicates  
- Handling of missing values and failed detections  
- Standardization of pollutant units  

### 2. Exploratory Data Analysis
- Monthly and annual averages  
- Province-level aggregation  
- Trend visualization  

### 3. Regulatory Compliance Assessment
- Comparison with Italian and EU legal limits  
- Identification of exceedances (annual and daily thresholds)

### 4. Air Quality Index (AQI) Calculation
- Monthly AQI computation  
- Province ranking  

### 5. Correlation Analysis
- Pearson correlation matrices  
- Seasonal behavior analysis  

### 6. Spatial Visualization
- Monitoring station mapping  
- Density maps by province  

---

## Key Findings

- Most pollutants comply with legal thresholds, with important exceptions:

  - **Ozone (O3)** exceeded limits in every province, with the highest levels in Lecco (LC).
  - **PM10** daily limit exceeded (>35 days) in Brescia (BS), Cremona (CR), and Mantova (MN).
  - **Lead (Pb)** annual limit exceeded in Sondrio (SO).

- Ozone shows a strong negative correlation with most primary pollutants, confirming its photochemical behavior and summer peak.

- Most polluted provinces (based on AQI and particulate matter):
  - Cremona (CR)
  - Brescia (BS)
  - Mantova (MN)

- Least polluted provinces:
  - Lecco (LC)
  - Sondrio (SO)
  - Como (CO)

- Worst month overall: February  
- Best month overall: May  

---

## Tools & Libraries

The project was developed in **R** using:

- tidyverse  
- dplyr  
- ggplot2  
- sf  
- osmdata  
- ggmap  

Data manipulation, geospatial analysis, and visualization were performed entirely in R.

---

## Limitations

- **Temporal scope**: The analysis is restricted to data from the year 2023. Therefore, results do not capture long-term trends or interannual variability in pollutant concentrations.

- **Spatial heterogeneity of monitoring stations**: Not all pollutants are monitored uniformly across the 12 provinces. Differences in station density and pollutant coverage may affect inter-provincial comparability.

- **AQI aggregation level**: The Air Quality Index (AQI) was computed using monthly average concentrations. This approach smooths short-term peaks and may underestimate acute exposure risks related to daily exceedances.

- **Exclusion of meteorological variables**: Meteorological factors (e.g., temperature, wind speed, humidity, atmospheric pressure) were not included in the analysis. As a result, the study does not explicitly model pollutant dispersion dynamics or seasonal meteorological influences.

## Future Improvements
- Multi-year comparison (time-series analysis)
- Integration of meteorological variables
- Predictive modeling of pollutant levels
- Machine learning clustering of provinces
- Interactive dashboard (Shiny / Power BI)

## License

This project is released for educational and research purposes.

All environmental data used in this analysis are publicly available and remain the property of **ARPA Lombardia – Regional Environmental Protection Agency**.  
This repository does not redistribute raw datasets unless explicitly permitted.

If you reuse parts of this project, please provide appropriate attribution.

---

## Author

**Andrea Ongarini**  
February 2024  

GitHub: https://github.com/0nga



