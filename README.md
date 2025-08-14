# gps-rinex_observables
## GPS RINEX Observable Data for Anomaly Detection
This dataset contains processed clean GPS RINEX (Receiver Independent Exchange Format) observational data specifically prepared for training anomaly detection models. The data has been extracted and converted from standard RINEX format to CSV for easier analysis and machine learning applications.


## Overview
This dataset contains processed clean GPS RINEX (Receiver Independent Exchange Format) observational data specifically prepared for training anomaly detection models. The data has been extracted and converted from standard RINEX format to CSV for easier analysis and machine learning applications.
Dataset Structure
## Two Data Formats Available:
### 1. Temporal Data (Time Series Analysis)
Files: 1,052 CSV files
Dimensions: 900 time steps × 16 features per file
Sampling Rate: 1 Hz continuous data
Duration: 15 minutes per file (900 seconds)
Coverage: 11 randomly selected days
Source: CDDIS (Crustal Dynamics Data Information System) Hatanaka 1Hz Dataset
### 2. Non-Temporal Data (Snapshots)
Files: 1 CSV file
Dimensions: ~43,840 snapshots × 16 features
Coverage: Daily snapshots across 5 years (2019-2024)
Sampling: 20 random snapshots per day from 2,192 days
Source: CDDIS Low Rate GNSS Dataset
Feature Description
Each data sample contains 16 features derived from 4 randomly selected GPS satellites, with 4 observables per satellite:



Feature Layout: For each sample, features are arranged as: [C1C_1, L1C_1, D1C_1, S1C_1, C1C_2, L1C_2, ..., S1C_4]

## Data Processing Pipeline
Source Data: Raw RINEX files from CDDIS archive
Satellite Selection: 4 GPS satellites randomly chosen per sample
Observable Extraction: C1C, L1C, D1C, S1C values extracted
Format Conversion: RINEX → CSV format
Quality Control: Data validation and consistency checks
## Use Cases
This dataset is designed for training models to identify GPS signal anomalies in the form of spoofing or jamming.
## Technical Specifications
File Format: CSV (Comma-separated values)
Encoding: UTF-8
Missing Values: Entries are 0s
Data Types: Float64 for all observables
Time Reference: GPS Time
## Citation & Acknowledgments
Data sourced from:
CDDIS: Crustal Dynamics Data Information System
## License
CC BY 4.0 (Creative Commons Attribution)

