# 🗺️ Toronto Crime Map

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vascosio1114/toronto-crime-map/blob/main/notebooks/crime_map.ipynb)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![License](https://img.shields.io/badge/License-MIT-green)

A hands-on spatial data science project built after completing **GGR376H5 (Spatial Data Science)** at the University of Toronto. I used what I learned in the course — spatial thinking, exploratory analysis, coordinate systems, and kernel density estimation — to analyse real Toronto crime data and turn it into interactive maps.

---

## 📊 Preview

![Crime Statistics](https://raw.githubusercontent.com/vascosio1114/toronto-crime-map/main/output/crime_stats.png)

*Crime type distribution, yearly trend (2020–2024), and monthly seasonality*

---

## 🔍 What I Built

- **Interactive Cluster Map** — every crime incident plotted as a colour-coded marker by type (Assault, Auto Theft, Robbery, etc.), with clickable popups showing offence details and neighbourhood
- **Heatmap** — kernel density visualisation on a dark basemap to clearly show where crime concentrates across the city
- **Statistical Charts** — crime type distribution, year-over-year trend, and monthly seasonality pattern

---

## 🧠 What I Applied from the Course

After GGR376H5 I understood that crime data has strong **spatial dependence** — incidents cluster in space and can't be treated as independent observations. This project put that thinking into practice:

- **Spatial data handling** — loaded and cleaned WGS84 coordinate data from the Toronto Police Open Data API
- **Exploratory spatial analysis** — plotted distributions and trends to understand the data before mapping
- **Kernel density estimation** — used as the basis for the heatmap to reveal spatial concentration patterns
- **Coordinate systems** — worked with lat/lon data in the correct CRS rather than just plotting raw numbers
- **Spatial ethics** — considered how publicly visualising crime data can reinforce neighbourhood stigma

---

## 🛠️ Tech Stack

`pandas` · `geopandas` · `folium` · `matplotlib` · `seaborn` · Toronto Open Data API

---

## 🚀 Run in Google Colab

Click the badge at the top — no setup needed, runs entirely in the browser.

Or clone locally:

```bash
git clone https://github.com/vascosio1114/toronto-crime-map.git
cd toronto-crime-map
pip install pandas geopandas folium matplotlib seaborn jupyter requests
jupyter notebook notebooks/crime_map.ipynb
```

> Data is fetched automatically from the [Toronto Open Data Portal](https://open.toronto.ca/dataset/major-crime-indicators/) — no manual download needed.

---

## 📁 Structure

```
toronto-crime-map/
├── notebooks/
│   └── crime_map.ipynb
├── output/
│   ├── crime_stats.png
│   ├── crime_cluster_map.html
│   └── crime_heatmap.html
└── README.md
```

---

## 👤 Author

**Vasco Sio (Kei Chon)**
Year 4 · Statistics & GIS · University of Toronto
[GitHub](https://github.com/vascosio1114)
