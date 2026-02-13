# Air Pollution Trends – Lombardy 2023

Comprehensive data analysis of air quality in the Lombardy region (Italy) for the year 2023, based on public datasets provided by ARPA Lombardia.  
The project explores pollutant concentrations, compares them with legal limits, calculates Air Quality Indices (AQI), and visualizes spatial and temporal trends across all 12 provinces.

## Objectives
- Assess compliance with Italian and European air quality standards (PM10, PM2.5, NO2, O3, SO2, CO, Benzene, heavy metals, etc.).
- Plot monthly and annual trends for each pollutant and province.
- Generate density maps of annual averages by station and province.
- Compute correlation matrices to identify relationships among pollutants.
- Rank provinces using the Air Quality Index (AQI).

## Pollutants Analyzed
PM10, PM2.5, NO2, NOX, NO, O3, SO2, CO, Benzene (C6H6), Ammonia (NH3), Black Carbon, Lead (Pb), Arsenic (As), Cadmium (Cd), Nickel (Ni).

## Tools & Libraries
- **R** (tidyverse, dplyr, ggplot2, sf, osmdata, ggmap)
- Data merging, cleaning (failed detections, duplicates), manipulation
- GeoJSON mapping of monitoring stations
- AQI calculation based on monthly averages

## Key Findings
- Most pollutants respect legal limits, **except**:
  - **Ozone (O3)**: exceeded limits in **every province** – worst in Lecco (LC).
  - **PM10**: daily limit exceeded >35 days in **Brescia, Cremona, Mantova** – best in Como (CO).
  - **Lead (Pb)**: annual limit exceeded in Sondrio (SO).
- Ozone shows a strong **negative correlation** with other pollutants (increases in summer).
- **Most polluted provinces**: Cremona (CR), Brescia (BS), Mantova (MN) – especially for PM and NO2.  
  **Least polluted**: Lecco (LC), Sondrio (SO), Como (CO).
- **Worst month**: February; **Best month**: May (based on AQI).

## Repository Structure
├── data/ # Raw and processed datasets (or instructions to download)
├── scripts/ # R scripts for preprocessing, analysis, and visualization
├── outputs/ # Plots, maps, and summary tables
├── Report_HIS.pdf # Full report (Italian)
└── README.md # Project overview (this file)


## How to Reproduce
1. Clone the repository.
2. Download the original ARPA datasets from the links provided in the report.
3. Run the R scripts in order:
   - `01_import_clean.R`
   - `02_analysis_by_substance.R`
   - `03_analysis_by_zone.R`
   - `04_aqi_ranking.R`
4. All graphs and tables will be saved in the `outputs/` folder.

## License
This project is for educational and research purposes. Data belongs to ARPA Lombardia.

## Author
**Andrea Ongarini** – February 2024  
[GitHub profile link]

