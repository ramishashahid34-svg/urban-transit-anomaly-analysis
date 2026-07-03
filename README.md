# 🚇 Urban Transit Anomaly Investigation

## Overview

This project investigates an unusual drop in subway activity at station **STN_003** and determines whether the anomaly was caused by a **hardware malfunction** or by **real-world environmental conditions**.

Using subway turnstile data, scooter mobility data, and city weather signals, I performed an end-to-end data analysis workflow including cleaning inconsistent datasets, integrating multiple data sources, and building visual evidence to support conclusions.

---

## Problem Statement

On **Day 15**, station **STN_003** experienced a significant decline in recorded subway entries between:

**14:00 – 20:00**

The key question:

> Was this caused by a station hardware failure, or did external factors influence rider behavior?

---

## Dataset Description

This project combines three independent datasets:

### 🚉 Subway Turnstile Data
Contains:

- Station ID
- Timestamp
- Hourly entry counts

### 🛴 Scooter Ride Data
Contains:

- Ride IDs
- Start time
- Geographic coordinates
- Ride activity around STN_003

### 🌧 City Heartbeat Data
Contains:

- Weather conditions
- Precipitation measurements
- Traffic and civic activity indicators

---

## Data Cleaning & Preprocessing

Several real-world inconsistencies were handled:

### Subway Dataset
- Standardized station IDs
- Converted timestamps into datetime format
- Cleaned corrupted entry values

### Scooter Dataset
- Filtered rides near STN_003 using geographic bounds
- Extracted hourly ride patterns
- Corrected coordinate formatting issues

### City Heartbeat Dataset
- Flattened nested JSON structure
- Cleaned precipitation values:
  - `"none"` → `0`
  - `"0mm"` → `0`
  - `"1mm"` → `1`
- Extracted Day 15 weather conditions

---

## Analysis Workflow

1. Cleaned and transformed all datasets
2. Extracted Day 15 observations
3. Aggregated subway entries by hour
4. Calculated nearby scooter ride activity
5. Integrated weather data
6. Built a multimodal visualization dashboard

---

## Visualization

### Three-panel dashboard:

- Subway entries at STN_003
- Scooter ride counts near STN_003
- Day 15 precipitation levels

![Dashboard](images/dashboard.png)

---

## Key Findings

### Observations

- Subway entries dropped sharply between **14:00–20:00**
- Heavy rainfall recorded on Day 15:
  **59.4 mm precipitation**
- Scooter activity continued rather than disappearing entirely

### Conclusion

The evidence suggests:

> STN_003 likely did not experience a hardware failure.

Instead, the anomaly appears to reflect broader transportation disruptions caused by severe weather conditions.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter / Google Colab

---

## Repository Structure

```text
urban-transit-anomaly-analysis/
│
├── notebooks/
│   └── Urban_Transit_Analysis.ipynb
│
├── data/
│   ├── subway_turnstile.csv
│   ├── scooter_rides.csv
│   └── city_heartbeat.json
│
├── images/
│   └── dashboard.png
│
├── README.md
└── requirements.txt
```

---

## Future Improvements

- Add interactive dashboards using Plotly
- Integrate anomaly detection models
- Build predictive transit disruption analysis
- Deploy as a Streamlit application

---

## Author

**Ramisha Shahid**

Python | Data Analysis | Machine Learning Enthusiast
