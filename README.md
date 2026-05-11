# Acute Malnutrition Early Warning System

A district-level Streamlit application for acute malnutrition risk monitoring and short-term forecasting in Uganda.

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

## Quick Start

1. Clone the repository.

```bash
git clone https://github.com/YOUR-USERNAME/acute-malnutrition-early-warning.git
cd acute-malnutrition-early-warning
```

2. Create a Python environment.

```bash
python -m venv .venv
source .venv/bin/activate
```

3. Install dependencies.

```bash
pip install -r requirements.txt
```

4. Run the app.

```bash
streamlit run streamlit_app.py
```

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

## Privacy

Do not commit sensitive health data. Keep full datasets in `data/private/`, which is ignored by Git.

## Repository Structure

```text
acute-malnutrition-early-warning/
├── streamlit_app.py
├── app/
│   └── streamlit_app.py
├── docs/
│   └── TECHNICAL_DOCUMENTATION.md
├── demo/
│   └── DEMO_VIDEO_GUIDE.md
├── impact_metrics/
│   └── IMPACT_METRICS.md
├── data/
│   ├── sample/
│   └── private/
├── assets/
│   └── screenshots/
├── requirements.txt
└── README.md
```

## Author

Sarah Awino

