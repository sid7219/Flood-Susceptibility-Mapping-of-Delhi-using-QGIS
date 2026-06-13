# 🌊 Flood Susceptibility Mapping of Delhi using GIS and MCDM

A GIS-based flood susceptibility assessment of Delhi using Multi-Criteria Decision Making (MCDM) and Weighted Overlay Analysis in QGIS. The study integrates elevation, slope, rainfall, land use/land cover (LULC), and river proximity to identify flood-prone zones across Delhi.

---

## 📖 Project Summary

Flooding is one of the major environmental hazards affecting urban areas. Delhi is particularly vulnerable due to the presence of the Yamuna River, rapid urbanization, increasing impervious surfaces, and changing rainfall patterns.

This project utilizes Remote Sensing, GIS, and Multi-Criteria Decision Making (MCDM) techniques to generate a Flood Susceptibility Map of Delhi. The final map classifies the study area into five flood susceptibility zones ranging from Very Low to Very High risk.

---

## 🎯 Objectives

- Identify flood-prone areas within Delhi.
- Generate flood conditioning factor layers using GIS techniques.
- Apply Multi-Criteria Decision Making (MCDM).
- Perform Weighted Overlay Analysis.
- Develop a Flood Susceptibility Map for disaster management and urban planning.

---

## 🗺️ Study Area

**Location:** Delhi, India

**Projection:** WGS 84 / UTM Zone 43N (EPSG:32643)

**Major River:** Yamuna River

**Area:** ~1484 km²

---

## 📊 Datasets Used

| Factor | Data Source |
|----------|----------|
| Distance from River | OpenStreetMap (OSM) Waterways |
| Elevation | SRTM DEM 30 m |
| Land Use/Land Cover (LULC) | ESA WorldCover 2021 |
| Rainfall | CHIRPS Rainfall Dataset |
| Slope | Derived from SRTM DEM |

---

## ⚙️ Methodology

### Workflow

```text
Data Collection
       ↓
Data Preprocessing
       ↓
Generation of Thematic Layers
       ↓
Reclassification
       ↓
Weight Assignment
       ↓
Weighted Overlay Analysis
       ↓
Flood Susceptibility Mapping
```

---

## 🧠 Multi-Criteria Decision Making (MCDM)

Weighted Linear Combination (WLC) was adopted for integrating all flood conditioning factors.

### Flood Susceptibility Index

FSI = Σ(Wi × Xi)

Where:

- Wi = Weight assigned to each factor
- Xi = Reclassified score of each factor

---

## 📈 Factor Weights

| Factor | Weight (%) |
|----------|----------:|
| Distance from River | 30 |
| Elevation | 25 |
| LULC | 20 |
| Rainfall | 13 |
| Slope | 12 |
| **Total** | **100** |

### Weighted Overlay Equation

```text
FSI =
(0.30 × River Distance)
+
(0.25 × Elevation)
+
(0.20 × LULC)
+
(0.13 × Rainfall)
+
(0.12 × Slope)
```

---

## 🚧 Drainage Density Analysis

Drainage density was initially explored as a flood conditioning factor using hydrological analysis and OpenStreetMap waterway data.

However, due to the relatively flat topography of Delhi and limitations associated with the 30 m SRTM DEM, the generated stream network produced unrealistic drainage patterns. Therefore, drainage density was excluded from the final susceptibility model.

---

## 📍 Results

The final flood susceptibility map classified Delhi into five categories:

| Class | Susceptibility |
|----------|----------|
| 1 | Very Low |
| 2 | Low |
| 3 | Moderate |
| 4 | High |
| 5 | Very High |

### Key Findings

- Very High susceptibility zones are concentrated along the Yamuna floodplain.
- Eastern Delhi exhibits the highest flood vulnerability.
- Central Delhi falls within moderate susceptibility zones.
- Southern and western Delhi show comparatively lower flood susceptibility.

---

## 🖼️ Final Flood Susceptibility Map

![Flood Susceptibility Map](Maps/flood_susceptibility_map.png)

**Figure:** Flood Susceptibility Map of Delhi generated using GIS-based Multi-Criteria Decision Making (MCDM) and Weighted Overlay Analysis.

---

## 🛠️ Software Used

- QGIS
- Google Earth Engine
- Microsoft Excel

---

## 📂 Repository Structure

```text
Flood-Susceptibility-Delhi
│
├── Data
│   ├── DEM
│   ├── Rainfall
│   ├── LULC
│   └── River
│
├── Maps
│   ├── study_area_map.png
│   ├── elevation_map.png
│   ├── slope_map.png
│   ├── rainfall_map.png
│   ├── lulc_map.png
│   ├── river_distance_map.png
│   └── flood_susceptibility_map.png
│
├── QGIS_Project
│   └── Flood_risk_map.qgz
│
├── Report
│   └── Flood_Susceptibility_Report.pdf
│
└── README.md
```

---

## 🚀 Applications

- Flood Risk Assessment
- Urban Planning
- Disaster Management
- Climate Resilience Planning
- Sustainable Development

---

## 👨‍💻 Author

**Siddharth Gupta**  
B.Tech Geoinformatics  
Netaji Subhas University of Technology (NSUT)

---
