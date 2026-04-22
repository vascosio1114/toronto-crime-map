# 🗺️ Toronto Crime Map

> **Course project for GGR376H5 — Spatial Data Science**
> University of Toronto Mississauga · Winter 2026
> **Vasco Sio (Kei Chon)**

An end-to-end spatial data science project applying concepts from GGR376H5 to real-world crime data sourced from the Toronto Police Service Open Data Portal. The project covers exploratory spatial analysis, interactive mapping, heatmap visualisation, and statistical modelling — reflecting the full arc of the course from spatial thinking to integrated modelling.

---

## 📊 Output Preview

### Crime Type Distribution, Yearly Trend & Monthly Seasonality

![Crime Statistics](output/crime_stats.png)

> *Fig 1: Left — distribution of Major Crime Indicators (MCI) categories (2020–2024). Centre — yearly trend showing total reported crimes. Right — monthly seasonality pattern.*

---

### Interactive Maps

| Map | Description |
|-----|-------------|
| [🔴 Cluster Map](output/crime_cluster_map.html) | MarkerCluster map coloured by crime type — click any point for offence details |
| [🌡️ Heatmap](output/crime_heatmap.html) | Kernel density heatmap showing spatial concentration of all MCI incidents |

> *Note: HTML maps require downloading and opening locally in a browser.*

---

## 🎓 GGR376H5 Course Connections

This project was built as a capstone demonstration of skills developed across the Winter 2026 course schedule. Each analytical component maps directly to a module in the course:

| Week | Topic | Applied in This Project |
|------|-------|------------------------|
| **Week 1** | Spatial thinking, dependence & modelling assumptions | Framing crime as a spatially dependent phenomenon — incidents are not random in space |
| **Week 2** | Spatial data representations, coordinate systems & measurement bias | Handling WGS84 lat/lon coordinates from TPS Open Data; understanding geocoding precision limits |
| **Week 3** | Exploratory spatial data analysis & visualisation as diagnostic tools | Crime type bar charts, yearly trend lines, monthly seasonality plots (`crime_stats.png`) |
| **Week 4** | Global spatial autocorrelation & spatial structure | Identifying city-wide clustering patterns visible in the heatmap (e.g., Downtown core, Scarborough) |
| **Week 5** | Local spatial structure, clustering tendencies & spatial heterogeneity | MarkerCluster map revealing local hotspots at neighbourhood scale |
| **Week 6** | Regression with spatial data: diagnostics, bias & misspecification | Basis for understanding why OLS would be misspecified for crime counts with spatial structure |
| **Week 8** | Spatial regression models & interpretation | Extension opportunity: Spatial Lag / Spatial Error model by neighbourhood |
| **Week 9** | Unsupervised learning under spatial constraints | Neighbourhood-level clustering of crime profiles as an extension |
| **Week 10** | Spatial prediction, interpolation & uncertainty | Heatmap as a kernel density estimate (KDE) — a form of spatial interpolation |
| **Week 12** | Machine learning with spatial data: validation, leakage & generalisation | Avoiding spatial leakage in any predictive model through spatial cross-validation |
| **Week 13** | Integrated spatial modelling, ethics & project synthesis | Reflecting on ethical use of public crime data, stigmatisation risk, and data limitations |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| `pandas` | Data loading, cleaning, filtering |
| `geopandas` | Spatial data handling |
| `folium` | Interactive map generation (Leaflet.js) |
| `folium.plugins.HeatMap` | Kernel density heatmap |
| `folium.plugins.MarkerCluster` | Aggregated point clustering |
| `matplotlib` + `seaborn` | Statistical charts |
| Toronto Open Data CKAN API | Live data source (no manual download needed) |

---

## 📁 Project Structure

```
toronto-crime-map/
├── notebooks/
│   └── crime_map.ipynb       ← Main analysis notebook
├── output/
│   ├── crime_stats.png       ← Statistical charts (Fig 1)
│   ├── crime_cluster_map.html ← Interactive cluster map
│   └── crime_heatmap.html    ← Interactive heatmap
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/vascosio1114/toronto-crime-map.git
cd toronto-crime-map

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install pandas geopandas folium matplotlib seaborn jupyter requests

# Launch notebook
jupyter notebook notebooks/crime_map.ipynb
```

> **Data**: The notebook fetches the latest MCI dataset automatically via the Toronto Open Data API (no manual download required). Dataset is refreshed quarterly by Toronto Police Services.

---

## 📌 Data Source

**Toronto Major Crime Indicators (MCI) / Community Safety Indicators**
- Publisher: Toronto Police Services
- Portal: [City of Toronto Open Data](https://open.toronto.ca/dataset/major-crime-indicators/)
- Licence: Open Government Licence – Toronto
- Last refreshed: Feb 20, 2026
- Coverage: 2014 – present · 158 Neighbourhoods

---

## 🔭 Future Extensions

- [ ] Spatial autocorrelation analysis using Moran's I (Week 4–5)
- [ ] Spatial lag regression model by neighbourhood (Week 8)
- [ ] K-means clustering of neighbourhood crime profiles (Week 9)
- [ ] Choropleth map of crime rates per capita by neighbourhood

---

## 👤 Author

**Vasco Sio (Kei Chon)**
Year 4 · Statistics & GIS · University of Toronto
[GitHub](https://github.com/vascosio1114)
