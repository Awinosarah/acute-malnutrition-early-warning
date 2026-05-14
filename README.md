# Acute Malnutrition Early Warning System

A district-level machine learning and analytics platform for monitoring, classifying, and forecasting acute malnutrition risk in Uganda.

The system integrates nutrition surveillance data, climate indicators, forecasting models, and geospatial visualizations to support early warning and decision-making for public health programs.

---

# Project Overview

Acute malnutrition remains a major public health concern in vulnerable populations. Early identification of high-risk districts is critical for preparedness, resource allocation, and timely intervention.

This platform was developed as a prototype decision-support system to:

- Monitor district-level malnutrition trends
- Classify nutrition risk severity
- Forecast future malnutrition burden
- Visualize spatial and temporal patterns
- Support evidence-based planning

The application is built using Streamlit and machine learning techniques for interactive analytics and forecasting.

---

# Key Features

## 1. District Risk Classification

The system classifies districts into risk categories:

- Normal
- Alert
- Alarm
- Emergency

Risk classification is based on:
- Historical malnutrition burden
- Percentile thresholds
- Trend behavior
- District-level comparisons

---
## 2. Forecasting Module

The forecasting module predicts short-term acute malnutrition trends using machine learning.

### Forecasting Features
- 3-month forecasting
- Random Forest Regression
- Trend visualization
- District-level projections

---

## 3. Machine Learning Classification

The classification component predicts district risk levels using engineered indicators and surveillance trends.

### Classification Features
- Random Forest Classification
- Risk prediction probabilities
- Performance evaluation metrics
- Feature importance analysis

---

## 4. Geospatial Risk Mapping

Interactive district-level maps are used to visualize nutrition risk patterns across Uganda.

### Mapping Features
- GeoJSON district boundaries
- District comparison views
- Regional distribution analysis

---

## 5. Trend Monitoring

The application supports longitudinal monitoring of malnutrition patterns.

### Trend Features
- Historical case trends
- Regional comparison charts
- District-level progression analysis
- Risk transition monitoring

---

## 6. Correlation Analysis

The platform explores relationships between nutrition outcomes and associated indicators.

### Analytics Included
- Spearman correlation analysis
- Radial/radar visualization
- Variable association monitoring
- Comparative indicator analysis

---

# System Architecture

The application follows a modular workflow:

1. Data Loading
2. Data Cleaning
3. Feature Engineering
4. Risk Classification
5. Forecasting
6. Visualization
7. Reporting

---

# Machine Learning Models

## Random Forest Regressor

Used for:
- Forecasting future acute malnutrition cases

Advantages:
- Handles non-linear relationships
- Suitable for complex public health data

---

## Random Forest Classifier

Used for:
- Predicting district risk levels

Advantages:
- Handles mixed variable types
- Supports feature importance analysis
- Performs well with complex interactions

---

# Data Sources

The system integrates multiple datasets including:

- Acute malnutrition surveillance data
- Climate indicators
- District metadata
- Historical nutrition trends


# Model Evaluation

The current prototype demonstrates functional workflows for:
- Risk classification
- Forecasting
- Visualization
- Monitoring


### Important Note

This system is intended as:
- An early warning prototype
- A decision-support tool
- A surveillance enhancement platform

---

# Intended Users

The platform may support:
- Ministry of Health programs
- Nutrition surveillance teams
- Humanitarian organizations
- Public health analysts
- District health offices


The app combines:

- district-based acute malnutrition risk classification;
- within-district and between-district percentile risk thresholds;
- Random Forest regression for 3-month case forecasting;
- Random Forest classification for risk evaluation;
- Spearman correlation analysis using radial visualizations;
- district and region comparison charts;
- historical risk trend monitoring;
- district GeoJSON risk maps.

## App Screens

- Data overview and Spearman correlation portrait
- District/region comparison against national reference
- Historical risk trends
- 3-month forecasts
- District-level risk maps
- Model evaluation metrics

## Data Requirements

The CSV should include:

| Column | Description |
|---|---|
| `Region_District` | Region and district, for example `Acholi|Agago District` |
| `District` | District name |
| `Region` | Region name |
| `time_period` | Monthly date, for example `2020-01` |
| `Acut_Malnutrition` | Acute malnutrition case count |
| `mean_temperature` | Mean temperature |
| `rainfall` | Rainfall |
| `mean_relative_humidity` | Relative humidity |
| `average_gpp` | Vegetation productivity |
| `malaria_confirmed` | Confirmed malaria cases |
| `pneumonia_cases` | Pneumonia cases |
| `pregnant_women_with_Anaemia` | Anaemia cases among pregnant women |
| `diarrhea_acute` | Acute diarrhoea cases |
| `low_birth_weight_babies` | Low birth weight babies |
| `diarrhea_persistent` | Persistent diarrhoea cases |
| `population` | District population |

## GeoJSON Requirements

Upload a district GeoJSON in the sidebar. Select the GeoJSON column containing district names. The app matches those names to the CSV district names.



## Author

Sarah Awino
