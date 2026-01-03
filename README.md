# AgriVuln-A

AgriVuln-A is a geospatial machine learning project that estimates agricultural and social vulnerability in Kenya by combining satellite data (Sentinel 2) with environmental and socio-economic indicators.

The project focuses on transforming complex geospatial data into clear vulnerability scores and visual insights that can support research and decision-making.

---

## What the Project Does

The system analyzes multiple types of data that describe environmental conditions and human exposure, then uses machine learning to estimate how vulnerable different regions are.

In simple terms:
- satellite data describes vegetation, rainfall, air quality, and water availability
- socio-economic data describes population exposure
- a machine learning model learns patterns associated with vulnerable areas

---

## Data Sources (High-Level Explanation)

The project integrates the following data types:

- **Vegetation indices (NDVI, EVI)**  
  Indicators derived from satellite images that reflect vegetation health and stress.

- **Precipitation data (CHIRPS)**  
  Used to capture rainfall patterns and anomalies.

- **Air quality indicators (PM2.5, CAMS aerosols)**  
  Represent environmental stress factors affecting agricultural productivity.

- **Hydrological layers (Water Occurrence)**  
  Describe long-term water availability and stability.

- **Socio-economic data (WorldPop 2020)**  
  Population density data used to estimate human exposure.

These datasets are spatially aligned and processed into a unified feature set.

---

## Machine Learning Approach

A supervised machine learning model (LightGBM classifier) was trained on **4,925 labeled geospatial data points**.

The model learns relationships between environmental conditions and observed vulnerability levels and produces vulnerability predictions for new regions.

---

## Outputs and Results

The system produces:

- A continuous **vulnerability index** (0–1 scale)
- Four vulnerability categories: Low, Medium, High, Very High
- Maps and plots that visually highlight vulnerable regions

These outputs are designed to be interpretable and usable by non-technical users.

---

## Interactive Dashboard

An interactive dashboard allows users to explore results visually.

Key features include:
- a map colored by vulnerability level
- filtering by vulnerability category
- summary statistics for selected regions

The dashboard is implemented using Streamlit and interactive plotting libraries.

---

## Project Structure
AgriVuln-A/
├── dashboard_app.py
├── modeling.py
├── preprocess.py
├── data_pipeline.py
├── data/
├── results/
└── README.md

---

## Notes

This project was developed in an educational and research context and focuses on clarity, interpretability, and applied geospatial analysis.

