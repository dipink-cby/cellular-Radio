# 📊 cellular-Radio Dataset

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

## 📖 Introduction
The **cellular-Radio Dataset** is a hybrid dataset tailored for 3D Radio Environment Map (REM) construction which combines collaborative air-ground empirical measurements with Ray-Tracing (RT) simulations conducted over identical real-world topography.

## 🛠️ Data Acquisition & Simulation Setup

### 1. Empirical Measurements
* **Scenario**: Yunnan University (Chenggong Campus), representing a typical suburban propagation environment.
* **Measurement Platform**: A DJI Air 3S utilized as the aerial platform for high-altitude spatial sampling.
* **Receiver Equipment**: A commercial smartphone equipped with a Snapdragon X70 5G modem (Qualcomm Incorporated, San Diego, CA, USA) was deployed to continuously record RSRP variations via the Cellular Pro application (alibaba1126, Beijing, China).
* **Center carrier frequency**: 3.45 GHz
* **Channel bandwidth**: 100 MHz
* **Sampling speed**: 3 m/s
* **Sampling interval**: 0.5 s

### 2. Ray-Tracing Simulation
**Environment Modeling**: 3D building meshes and topography were reconstructed utilizing Esri World Imagery and JAXA AW3D30 DEM.
* **Coordinate Reference System**: The dataset uses WGS 84 (EPSG:4326) for global coordinates and is projected to UTM Zone 48N (EPSG:32648) for local 3D simulations.
* **Simulation engine**: NVIDIA Sionna (v2.0.1)
* **Antenna Pattern**: Compliant with 3GPP TR 38.901 specifications.
* **Grid resolution**: 1 m
* **Maximum Depth**: 5 reflections / diffractions

## 📁 Repository Structure

```text
├── Dataset/
│   ├── 3D-VRM/
│   └── Joint-REM/
├── Sionna/
│   ├── REM/               # Jupyter Notebook for data simulation
│   └── YNU/
│       ├── meshes/        # 3D Geometry Mesh include  (.ply)
│       └── YNU_scene/     # Scene Description (.xml)          
└── README.md
