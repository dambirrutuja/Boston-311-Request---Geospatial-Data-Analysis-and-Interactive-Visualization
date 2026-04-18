# 🗺️ Boston 311 Service Requests — Geospatial Analysis
### IE6600 Computation and Visualization for Analytics | Spring 2026 | Project 3

> Interactive geospatial analysis of **114,413 citizen-reported service requests** across Boston in 2024, built with Python and Plotly.

🌐 **[View Live Website](https://dambirrutuja.github.io/Boston-311-Request---Geospatial-Data-Analysis-and-Interactive-Visualization/)**

---

## 👥 Team — Group 4

| Name | 
|------|
| Rutuja Dambir |
| Praniti Kale |
| Hiral Rana |

---

## 📌 Project Overview

This project analyzes the Boston 311 Service Request dataset sourced from [data.boston.gov](https://data.boston.gov). The goal is to uncover geographic patterns, temporal trends, and service performance gaps through interactive visualizations using the Plotly library.

All visualizations are saved as standalone HTML files and hosted on a live project website.

---

## 📊 Interactive Visualizations

| File | Description |
|------|-------------|
| `complaints_map.html` | Scatter map — all complaints colored by Open/Closed status |
| `density_heatmap.html` | Kernel density heatmap of complaint concentration |
| `top_complaints.html` | Bar chart of top 10 complaint categories |
| `resolution_time.html` | Histogram of days-to-resolution distribution |
| `delay_hotspots.html` | Map of highest-delay complaints (top 25%) |
| `trend.html` | Monthly complaint volume line chart (2024) |
| `clusters.html` | K-Means geospatial cluster map — 5 service zones |
| `resolution_by_neighborhood.html` | Average resolution time per neighborhood |
| `sla_by_department.html` | On-time vs overdue by department (SLA compliance) |

---

## 🗂️ Repository Structure

```
├── IE6600_Geospatial_Project.ipynb     # Main analysis notebook
├── index.html                          # Project website
├── complaints_map.html
├── density_heatmap.html
├── top_complaints.html
├── resolution_time.html
├── delay_hotspots.html
├── trend.html
├── clusters.html
├── resolution_by_neighborhood.html
├── sla_by_department.html
├── IE6600_Project3_Report.pdf          # Full project report (PDF)
├── IE6600_Project3_Report.docx         # Full project report (Word)
└── README.md
```

---

## ⚙️ How to Run the Notebook

**1. Clone the repository**
```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

**2. Install dependencies**
```bash
pip install pandas numpy plotly geopandas scikit-learn
```

**3. Download the dataset**

Download the Boston 311 Service Requests CSV from [data.boston.gov](https://data.boston.gov) and place it in the project folder as `boston_311.csv`.

**4. Run the notebook**
```bash
jupyter notebook IE6600_Geospatial_Project.ipynb
```

Running all cells will generate all 9 HTML visualization files in the same directory.

---

## 🧹 Data Cleaning Summary

| Column | Issue | Action |
|--------|-------|--------|
| `latitude` / `longitude` | 925 missing | Dropped rows — required for maps |
| `closed_dt` | 15,937 missing | Left as NaN — case still open |
| `sla_target_dt` | 9,135 missing | Left as NaN — no SLA target set |
| `location_zipcode` | 23,697 missing | Filled with `'Unknown'` |
| `neighborhood` | 86 missing | Filled with `'Unknown'` |
| `case_title` | 41 missing | Filled with `'Not Specified'` |
| `resolution_time` | Negative values | Removed — data entry errors |

---

## 🔍 Key Insights

- **📍 Geographic concentration** — Dorchester, Roxbury, and South End generate the highest complaint volumes
- **☀️ Seasonal surge** — Summer months see ~30% more complaints than the annual average
- **⏰ Long-tail resolution** — Most cases close in under 3 days, but the top 10% take over 3 weeks
- **⚖️ Neighborhood equity gap** — Some neighborhoods wait 5–8× longer than others for the same service
- **📋 SLA non-compliance** — Certain departments consistently miss SLA targets
- **🤖 Cluster-based routing** — 5 K-Means zones align with Boston's natural neighborhood geography

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

- **Python** — data processing and analysis
- **Plotly Express** — all interactive visualizations and maps
- **Pandas / NumPy** — data manipulation
- **scikit-learn** — K-Means geospatial clustering
- **GeoPandas** — geospatial data handling
- **GitHub Pages** — website hosting

---

## 📄 Report

The full project report is available in the repository:
- [`IE6600_Project3_Report.pdf`](./IE6600_Project3_Report.pdf)
- [`IE6600_Project3_Report.docx`](./IE6600_Project3_Report.docx)

---

*IE6600 Project 3 | Boston 311 Service Requests Analysis | Spring 2026*
