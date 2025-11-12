# PedestrianNoncomplianceAnalysis

This repository contains all datasets, Python scripts, and resources used for the honours thesis titled **"To Cross, or Not to Cross: Pedestrian Non-Compliance Modelling at Signalised Intersections in Sydney"**. The project investigates pedestrian non-compliant behaviour at signalised intersections using statistical and machine learning methods, including Multiple Logistic Regression (MLR) and Hazard-Based Modelling (HBM).

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Python Scripts](#python-scripts)
- [Methods](#methods)
- [Results and Figures](#results-and-figures)
- [Requirements](#requirements)
- [Usage](#usage)
- [Citation](#citation)
- [Acknowledgements](#acknowledgements)
- [License](#license)

---

## Project Overview

Pedestrian non-compliance at intersections can contribute to pedestrian-vehicle conflicts and increased risk of injuries. This project leverages automated computer vision techniques (YOLOv11 and ByteTrack) and statistical modelling to:

- Analyse pedestrian behaviour across multiple Sydney intersections.
- Identify key predictors of non-compliant crossings.
- Understand the effect of contextual factors such as phone usage, group behaviour, and waiting times.
- Provide insights for improving intersection design and traffic signal timing.

---

## Dataset

The dataset includes:

- **Pedestrian observations** (n = 2,004 pedestrians) from video recordings at three signalised intersections.
- **Variables**: Gender, age, group size, phone usage, actuator use, running/jogging behaviour, crossing type, accepted gap, wait time, next vehicle type, and hard compliance indicator.

> **Note:** Personal identifiers have been removed to protect privacy. Only anonymised and aggregated behavioural data is included.

---

## Python Scripts

All Python scripts used in the project are included:

1. `site_selection_yolo.py` – Setup for YOLO detection at intersections.
2. `data_extraction_yolo.py` – Automated extraction of pedestrian coordinates, timestamps, and signals.
3. `data_post_processing.py` – Cleaning, transforming, and merging YOLO outputs for analysis.
4. `regression_analysis.py` – Multiple Logistic Regression (MLR) modelling for non-compliance.
5. `hazard_modeling.py` – Cox proportional hazards modelling for temporal analysis.
6. `figures_and_visualisation.py` – Generates figures, heatmaps, and plots for the thesis.

---

## Methods

- **Computer Vision**: YOLOv11 object detection with ByteTrack tracking.
- **Statistical Modelling**:
  - Multiple Logistic Regression (MLR) to identify predictors of non-compliance.
  - Cox Proportional Hazards Model (HBM) to capture temporal dynamics and wait time effects.
- **Data Analysis**: Python libraries including `pandas`, `numpy`, `statsmodels`, `scikit-learn`, and `matplotlib`.

---

## Requirements

- Python 3.9.2
- Required Python packages (install via pip):

```bash
pip install -r requirements.txt
pandas
numpy
matplotlib
seaborn
statsmodels
scikit-learn
torch
opencv-python
ultralytics
```

---

