# Hospital Readmission Rate Dashboard — Tableau

This project delivers an **interactive Tableau dashboard** for executive leaders to explore and analyze patient readmission rates across a hospital dataset. The dashboard provides a multi-dimensional view of readmission patterns across geographic, demographic, clinical, hospitalization, and patient survey dimensions — enabling data-driven decisions to reduce readmissions and improve patient outcomes.

A consistent red–blue color scheme is used throughout the dashboard:
- **Red** = Readmission rate above the overall benchmark (36.69%)
- **Blue** = Readmission rate below the overall benchmark (36.69%)

> **Note on Dataset Availability**
> The underlying patient dataset has been removed from this repository as it contains sensitive medical information and is proprietary and non-shareable. The Tableau workbook (`.twbx`) with all visualizations is retained for presentation and reference purposes.

---

## Dashboard Overview

The dashboard contains **5 interactive visualizations** and a **KPI panel**, all linked by shared filters for Age, Gender, and State.

| ![main](Screenshots/main.png) |

### 1. Geographic Distribution (Map)
A U.S. map showing readmission patterns by location. A dropdown lets you switch between Zip, City, County, or State granularity. Dot size reflects patient count; dot color reflects position relative to the benchmark.

| Map View |
|---|
| ![Map](Screenshots/Map.png) |

### 2. Readmission by Patient Demographics (Bar Chart)
Compares readmission rates across demographic segments. A dropdown lets you switch between Age, Area, Income, Marital Status, and Gender. Includes a filtered average line that updates dynamically based on active filters.

| Demographics Chart |
|---|
| ![Demographic](Screenshots/Demographic.png) |

### 3. Readmission by Medical Condition (Bar Chart)
Compares readmission rates between patients with and without specific conditions (e.g., Diabetes, Stroke, Asthma, Anxiety, Back Pain, Overweight). Includes a filtered average line.

| Conditions Chart |
|---|
| ![Condition](Screenshots/Condition.png) |

### 4. Readmission by Hospitalization Information (Bar Chart)
Breaks down readmission rates by hospital stay details such as Initial Admission type, Case Order, Services, Total Charges, and Vitamin D levels. Includes a filtered average line.

| Hospitalization Chart |
|---|
| ![HospitalizationInfo](Screenshots/HospitalizationInfo.png) |

### 5. Readmission by Patient Survey Responses (Line Chart)
Explores how patients' self-reported priorities relate to readmission likelihood. The x-axis shows importance ranking (1 = most important, 8 = least important); the y-axis shows readmission rate. A dropdown lets you select from 8 survey items (e.g., Timely Admission, Courteous Staff, Hours of Treatment).

| Survey Response Chart |
|---|
| ![Survey](Screenshots/Survey.png) |

---

## KPIs (Right Panel)

| KPI | Description |
|---|---|
| Overall Readmission Rate | Fixed benchmark across the full dataset: **36.69%** |
| Filtered Readmission Rate | Rate adjusted to reflect currently active filters |
| Readmitted / Total Patients | Absolute counts — important for assessing sample reliability |
| Avg. Patient Priority on Survey Item | Mean importance score (1–8) for the selected survey question |

---

## How to Use the Dashboard

### Requirements
- **Tableau Desktop** or **Tableau Reader** (free) must be installed.
- If neither is installed, ask your IT team to install [Tableau Reader](https://www.tableau.com/products/reader).

### Steps
1. Open the `.twbx` file by double-clicking it in Tableau Desktop or Reader.
2. Use the **right-side filter panel** to narrow by Age, Gender, or State.
3. Use **dropdown menus** above each chart to switch between variables.
4. **Interpret colors:** Red = above benchmark; Blue = below benchmark.
5. **Hover** over any bar, dot, or data point to see exact statistics in the tooltip.

> **Privacy reminder:** This workbook contains patient data. Only open or share it on authorized, secure devices.

---

## Project Structure

```
project/
├── dashboard/
│   └── readmission_dashboard.twbx    # Tableau workbook — open this
├── Screenshots/                      # Dashboard screenshots for presentation
└── README.md
```
