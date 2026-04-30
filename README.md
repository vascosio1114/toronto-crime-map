# 🗺️ Toronto Crime Spatial Analysis

> Applied spatial data science project — built after completing **GGR376H5 (Spatial Data Science)** at the University of Toronto Mississauga.

Using real Toronto Police Open Data, I applied concepts from the course — spatial dependence, kernel density estimation, coordinate reference systems, and exploratory spatial analysis — to build a set of interactive crime visualisations for 2020–2024.

---

## 📌 What I Built

**Interactive Cluster Map**
Every crime incident plotted as a colour-coded marker by offence type (Assault, Auto Theft, Robbery, Break & Enter, etc.), with clickable popups showing offence details and neighbourhood.

**KDE Heatmap**
Kernel density estimation visualised on a dark basemap — reveals where crime actually concentrates across the city rather than just where incidents are reported.

**Statistical Charts**
- Crime type distribution
- Year-over-year trend (2020–2024)
- Monthly seasonality pattern

---

## 🧠 Course Concepts Applied

GGR376H5 taught me to think spatially about data — that crime incidents cluster in space and can't be treated as independent observations. This project put that into practice:

| Concept | How I applied it |
|---|---|
| Spatial data handling | Loaded and cleaned WGS84 coordinate data from the Toronto Police Open Data API |
| Exploratory spatial analysis | Plotted distributions and trends before mapping to understand the data |
| Kernel density estimation | Used as the basis for the heatmap to reveal spatial concentration |
| Coordinate reference systems | Worked with lat/lon data in the correct CRS rather than raw numbers |
| Spatial ethics | Considered how publicly visualising crime data can reinforce neighbourhood stigma |

---

## 🛠️ Tech Stack

pandas · GeoPandas · Folium · Matplotlib · Seaborn · Toronto Open Data API

---

## 🚀 Run It

**In Google Colab** — click the badge at the top of the notebook. No setup needed.

**Locally:**
```bash
git clone https://github.com/vascosio1114/toronto-crime-map.git
cd toronto-crime-map
pip install pandas geopandas folium matplotlib seaborn jupyter requests
jupyter notebook notebooks/crime_map.ipynb
```

Data is fetched automatically from the Toronto Open Data Portal — no manual download needed.

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

**Vasco Sio (Kei Chon)** · Year 4 · GIS & Statistics · University of Toronto Mississauga
📫 keichonsio1114@gmail.com
