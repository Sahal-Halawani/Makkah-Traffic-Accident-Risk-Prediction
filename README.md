# Makkah Traffic Accident Risk Prediction

## Predicting High-Risk Traffic Accident Areas in the Makkah Administrative Region Using Predictive Modeling and Spatial Analysis

### Project Overview

Traffic accidents represent a major public safety challenge, particularly in rapidly growing urban regions. This project aims to identify and predict high-risk traffic accident areas within the Makkah Administrative Region using machine learning and spatial analysis techniques.

Unlike traditional approaches that focus only on accident frequency, this project introduces a severity-based Risk Score that considers the seriousness of accidents when estimating risk levels. This allows a more realistic assessment of dangerous locations and supports proactive traffic safety planning.

The study area includes Makkah, Jeddah, Taif, and surrounding regions using traffic accident records collected between 2023 and 2025.

---

## Project Objectives

- Analyze historical traffic accident data in the Makkah Administrative Region.
- Identify high-risk accident locations using spatial analysis.
- Develop a severity-based Risk Score for each spatial grid.
- Train and compare multiple machine learning models.
- Predict accident risk levels across different geographic areas.
- Support traffic safety authorities in proactive decision-making.

---

## Dataset Description

The project uses traffic accident records from 2023–2025 covering:

- Makkah
- Jeddah
- Taif
- Surrounding areas

The dataset contains:

- Geographic coordinates
- Accident type
- Accident severity
- Spatial grid information

Files included:

```text
data/
├── 2023-2025.csv
├── grid_data_output.csv
```

---

## Methodology

The project follows a grid-based spatial machine learning framework:

1. Data Collection
2. Data Cleaning and Preprocessing
3. Coordinate Validation and Filtering
4. Spatial Grid Generation
5. Risk Score Calculation
6. Feature Engineering
7. Machine Learning Model Training
8. Model Evaluation
9. Spatial Risk Visualization

Each accident is assigned to a spatial grid based on its geographic coordinates.

---

## Risk Score Calculation

Instead of predicting accident count only, the project predicts a severity-based Risk Score.

Severity weights:

- Fatal Accident = 10
- Injury Accident = 3
- No-Injury Accident = 1

Formula:

```text
Risk Score =
(10 × Fatal Accidents)
+ (3 × Injury Accidents)
+ (1 × No-Injury Accidents)
```

This approach provides a more realistic representation of traffic risk because areas with fewer but more severe accidents may be more dangerous than areas with many minor accidents.

---

## Machine Learning Models

The following regression models were evaluated:

- XGBRegressor
- RandomForestRegressor
- KNeighborsRegressor
- DecisionTreeRegressor
- PoissonRegressor

---

## Evaluation Metrics

Model performance was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Results

### Best Performing Model: XGBRegressor

| Metric | Value |
|----------|----------|
| MAE | 3.91 |
| RMSE | 5.15 |
| R² | 0.733 |

The XGBRegressor achieved the lowest prediction error and the highest explanatory power among all tested models.

The model successfully explained approximately 73% of the variation in grid-level traffic accident risk across the study area.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Folium
- Matplotlib
- Power BI
- Jupyter Notebook

---

## Repository Structure

```text
Makkah-Traffic-Accident-Risk-Prediction/

├── data/
│   ├── 2023-2025.csv
│   └── grid_data_output.csv
│
├── notebooks/
│   └── Project.ipynb
│
├── dashboard/
│   └── Project.pbix.zip
│
├── requirements.txt
└── README.md
```

---

## Installation

Install required packages:

```bash
pip install -r requirements.txt
```

---

## Future Enhancements

Future work may include:

- Weather data integration
- Traffic density information
- Road infrastructure characteristics
- Road type classification
- Temporal analysis (hour, day, season, holidays)
- Real-time accident risk monitoring
- Advanced spatio-temporal prediction models

---

## Authors

- Sahal Ahmad Halawani
- Aseel Abdulfatah Al-Maghrabi
- Abdulrahman Al-Harbi
- Zyad Ahmed Al-Ghamdi
- Abdullah Faisal Al-Zahrani

---

## Supervisor

Dr. Waleed Abunomi Alsharif

---

## University

Department of Data Science  
College of Computing  
Umm Al-Qura University  
Bachelor of Science in Data Science

Academic Year 2025–2026
