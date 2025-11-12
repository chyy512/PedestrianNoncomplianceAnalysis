# PedestrianNoncomplianceAnalysis

This repository contains all datasets, Python scripts, and resources used for the honours thesis titled **"To Cross, or Not to Cross: Pedestrian Non-Compliance Modelling at Signalised Intersections in Sydney"**. The project investigates pedestrian non-compliant behaviour at signalised intersections using statistical and machine learning methods, including Multiple Logistic Regression (MLR) and Hazard-Based Modelling (HBM).

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Python Scripts](#python-scripts)
- [Results and Figures](#results-and-figures)
- [Requirements](#requirements)
- [Usage](#usage)
- [Acknowledgements](#acknowledgements)

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

---

## Python Scripts

All Python scripts used in the project are included:

1. `site_selection.ipynb` – Script for site selection process, used in conjunction with Transport for NSW datasets: NSW Road Crash Data - 2019-2023 - CRASH, NSW Road Crash Data - 2019-2023 - TRAFFIC UNIT. (https://opendata.transport.nsw.gov.au/data/dataset/nsw-crash-data)
2. `walk_count_surveys.ipynb` – Script for pedestrian volume checks, used in conjunction with City of Sydney Walking Count dataset (https://data.cityofsydney.nsw.gov.au/datasets/cityofsydney::walking-count-surveys/about ) 
3. `signal_vehicle_detection.ipynb` – Script for YOLO vehicle detection and signal detection, to apply to video surveys.
4.  `bytetrack.yaml` – Bytetrack configuration for pedestrian detection.
5. `pedestrian_detection_trial.ipynb` – Script for YOLO pedestrian detection, to apply to video surveys.
6. `datapostprocess.ipynb` – Script for creating datasets for Multiple Logistic Regression and hazards based modelling and conducting various descriptive statistical analysis - (refer to csv files for regression modelling and hazard based modelling for thesis results).
7. `mlr_hbm_modelling.ipynb` – Variable correlation analysis, Multiple Logistic Regression (MLR) modelling for non-compliance and Cox proportional hazards modelling for temporal analysis - (refer to csv files for regression modelling and hazard based modelling for thesis results).

**Note: ** Remove and update file paths as required.

## Methods

- **Computer Vision**: YOLOv11 object detection with ByteTrack tracking.
- **Statistical Modelling**:
  - Multiple Logistic Regression (MLR) to identify predictors of non-compliance.
  - Cox Proportional Hazards Model (HBM) to capture temporal dynamics and wait time effects.
- **Data Analysis**: Python libraries including `pandas`, `numpy`, `statsmodels`, `scikit-learn`, and `matplotlib`.

---

## Requirements

- Python 3.9.2
- Required Python packages:

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

## Usage
1. Clone repository
```bash
git clone https://github.com/your-username/pedestrian-noncompliance.git
cd pedestrian-noncompliance
```

2. Run scripts in the following order:
```bash
python site_selection_yolo.py
python data_extraction_yolo.py
python data_post_processing.py
python regression_analysis.py
python hazard_modeling.py
python figures_and_visualisation.py
```

---

## Acknowledgements
Ultralytics YOLO for object detection framework.
Python and its open-source libraries for data analysis.
Transport for New South Wales for providing NSW crash data.
AI tools used for code structure, statistical clarification, and grammar assistance are acknowledged in the thesis.

