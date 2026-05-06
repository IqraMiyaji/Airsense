# Airsense
### Scalable Spatiotemporal Estimation of Particulate Matter via Multi-Source Data Fusion and Deep Learning

**First Prize — Project Exhibition and Competition, April 17, 2026**  
Usha Mittal Institute of Technology, SNDT Women's University

---

## Certificate of Appreciation

<p align="center">
  <img src="WhatsApp Image 2026-05-04 at 20.03.27.jpeg" alt="Certificate of Appreciation – First Prize, Intelligent Air Quality Mapping" width="700"/>
</p>

---

## Project Report

The full project report (Black Book) is available for reference:

[View Project Report on Google Drive](https://drive.google.com/file/d/1lUngdA_PhXZS2b3nrIjp-gfI-tj6sjpM/view?usp=sharing)

---

## Overview

**Airsense** is a hybrid deep learning framework for urban air quality monitoring and forecasting, focused on the Mumbai Metropolitan Region (MMR). It fuses geostationary satellite imagery, meteorological reanalysis variables, and ground-based Air Quality Index (AQI) observations to produce a spatially continuous and temporally dynamic representation of pollution patterns — addressing the limitations of sparse, ground-based sensor networks.

---

## Objectives

- Integrate heterogeneous datasets from the **INSAT-3DR Level-2G satellite** and the **Maharashtra Pollution Control Board (MPCB)** into a unified predictive pipeline.
- Develop a hybrid **CNN-LSTM architecture** (ResNet-18 backbone) that extracts spatial features from Aerosol Optical Depth (AOD) maps and models temporal sequences for high-accuracy forecasting.
- Build the **AirSense Mumbai web platform** providing real-time visualizations, age-specific health modes, and automated alert mechanisms.
- Investigate and quantify nature-based phytoremediation solutions for improving indoor air quality.

---

## System Architecture

```
Raw INSAT-3DR HDF5 Data
        │
        ▼
HDF5 → PNG Preprocessing Pipeline
        │  (Execution Time: ~3777s | Memory Spike: ~5 GB RAM)
        ▼
Geospatial Subsetting (Mumbai MMR Coordinates)
        │
        ▼
CNN Feature Extraction (ResNet-18 Backbone)
        │  Spatial Pollution Fingerprints
        ▼
LSTM Temporal Modeling
        │  Long-range dependencies, seasonal variation
        ▼
AQI / PM2.5 / PM10 Forecast  (Precision: ±19.1 AQI units)
        │
        ▼
AirSense Web Platform
  ├── 7-day AQI Forecast
  ├── Interactive Visualizations
  └── Personalized Health Advisories
```

---

## Data Sources

| Source | Description |
|--------|-------------|
| INSAT-3DR — MOSDAC/ISRO | Geostationary satellite providing Aerosol Optical Depth (AOD) imagery |
| MPCB — BKC Station | Ground-truth PM2.5 and PM10 AQI measurements |
| IMD Meteorological Reanalysis | Temperature, humidity, wind speed, and atmospheric variables |

**Temporal Scope:** January 2023 – October 2025 (approximately 2.5 years of continuous data)

---

## Model Performance

| Metric | Value |
|--------|-------|
| Prediction Precision | ±19.1 AQI units |
| Training Time per Epoch | ~63 minutes |
| Inference Speed | < 1 second per image |
| Satellite Captures per Day | 7–8 |
| GPU Environment | NVIDIA T4 with CUDA support |

---

## Technology Stack

**Core Programming and Machine Learning**
- Python, Google Colab
- TensorFlow, PyTorch
- Pandas, NumPy
- Matplotlib, Seaborn

**Data Acquisition and Management**
- WinSCP — bulk acquisition of MOSDAC satellite data
- Microsoft Excel — ground-truth record management

**Deployment and Documentation**
- GitHub Pages — web platform hosting
- Vernier LabQuest 2 — IoT sensor interface for indoor experiments
- Overleaf — research documentation

---

## Indoor Air Quality — Phytoremediation

In addition to outdoor pollution forecasting, the project validates nature-based indoor air quality solutions through controlled experiments. Measurable reductions in CO2 concentration were observed using the Areca Palm, Snake Plant, and Money Plant. A synergistic interaction between biological filtration (plants) and mechanical air purification systems was identified, presenting a sustainable and low-cost alternative for improving indoor air quality in densely populated urban households.

---

## Known Limitations

- Dense cloud cover during monsoon months causes Aerosol Optical Depth data gaps, addressed through forward and backward fill imputation strategies.
- Passive sensing by INSAT-3DR restricts data acquisition to daylight hours, creating gaps in diurnal cycle coverage.
- Regulatory restrictions on automated satellite data ingestion currently prevent fully real-time platform operation.
- The model is optimized for the Mumbai Metropolitan Region; extension to other cities requires region-specific retraining.
- Training is dependent on GPU acceleration and is not feasible on CPU-based environments.

---

## Future Work

- Transition to real-time forecasting via authorized, automated satellite data pipelines.
- Implement spatial downscaling techniques to generate street-level pollution maps.
- Develop IoT-integrated smart indoor air quality monitoring systems.
- Extend the framework to additional metropolitan regions using transfer learning.
- Optimize the model pipeline through pruning, quantization, and knowledge distillation for edge deployment.

---

## Team

| Name | 
|------|
| Dhwani Chheda | 
| Reshma Jaiswar | 
| Iqra Miyaji | 

**Faculty Guide:** Dr. Arundhati Mehendale  
**Department:** Data Science  
**Institution:** Usha Mittal Institute of Technology, SNDT Women's University, Mumbai  
**Academic Year:** 2025–2026

---

## Acknowledgements

The team acknowledges the guidance of Dr. Arundhati Mehendale, MOSDAC/ISRO for satellite data access, and CUNY for collaborative research insights.
