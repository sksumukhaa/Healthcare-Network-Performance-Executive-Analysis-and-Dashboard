# Healthcare Network Performance: Executive Analysis & Dashboard

An interactive, single-file HTML dashboard for hospital leadership, built from a Python analysis of a healthcare admissions dataset. It turns the analysis into a short set of KPIs, charts and management takeaways.

## What's in this repo

| File | Purpose |
|---|---|
| `hospital_executive_dashboard.html` | The executive dashboard. Open it directly in a browser. |
| `hospital_executive_dashboard.ipynb` | The Jupyter notebook with the data cleaning and analysis behind the dashboard. |
| `README.md` | This file. |

## Tech stack

- Python, pandas, NumPy, Matplotlib (analysis)
- HTML, CSS, JavaScript and Chart.js (dashboard)


[Dashboard preview]
<img width="2846" height="1698" alt="image" src="https://github.com/user-attachments/assets/a0644274-3fe0-4181-8bfb-a3be78eadd27" />

<img width="2832" height="1706" alt="Screenshot 2026-11-18 160747" src="https://github.com/user-attachments/assets/82e1422a-d2ec-4477-8818-48f509474a86" />

<img width="2708" height="1682" alt="Screenshot 2026-11-18 160759" src="https://github.com/user-attachments/assets/2c9e325f-cf3c-42d4-9050-3c01323ad833" />

<img width="2380" height="1670" alt="Screenshot 2026-11-18 160812" src="https://github.com/user-attachments/assets/c6a823af-787e-4ff5-8722-974f3274f6ec" />

## Dashboard overview

- **KPI cards:** total admissions, total billing, average billing, insurance providers, median patient age, emergency admissions.
- **Executive summary:** five management-level findings.
- **Key business insights:** patients by condition, patients by age group, average billing by age group, patients by insurance provider, average billing over time.
- **Additional insights:** emergency admissions by month, high-cost cases, emergencies with abnormal test results.
- **Management takeaways:** what is happening, why it matters, what to watch.

### Interactivity

- Multi-select filters for **medical condition**, **insurance provider** and **age group**. Charts highlight the selection and the KPI cards update.
- A **date range** (month from / month to, May 2019 – May 2024) that filters the billing-over-time chart.
- Hover tooltips on all charts.
- **Reset filters** button.
- Responsive layout with automatic light and dark mode.

## Key findings

- Demand is evenly spread: each of the six conditions has 9,095–9,218 patients (Arthritis highest).
- Average billing is about **$25,595** per admission and varies by only about 4% across age groups.
- Five insurers each cover 19.7%–20.3% of patients; Cigna is highest at 20.3%.
- **18,102** admissions (about 33%) are emergencies, peaking in July (1,573) and lowest in February (1,452).
- **6,038** emergency admissions (33.4% of emergencies) had abnormal test results.
- **5,497** admissions (10%) fall above the 90th percentile of billing.

## Data

- **Source:** [Healthcare Dataset on Kaggle](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)
- **Records:** 55,500 raw, 54,966 after cleaning
- **Period:** May 2019 – May 2024
- **Columns:** Name, Age, Gender, Blood Type, Medical Condition, Date of Admission, Doctor, Hospital, Insurance Provider, Billing Amount, Room Number, Admission Type, Discharge Date, Medication, Test Results

### Cleaning applied in the notebook

- Removed 534 duplicate rows (0.96%).
- Standardised patient names to title case.
- Replaced 106 negative billing amounts with the mean of the positive amounts ($25,594.63).
- Converted admission and discharge dates to dates and derived stay duration and 10-year age groups.

## Running the dashboard

1. Download `hospital_executive_dashboard.html`.
2. Open it in any modern browser. No build step or server is needed.

## License

MIT License
