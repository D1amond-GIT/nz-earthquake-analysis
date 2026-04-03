# Hidden Faults: Uncovering New Zealand's Seismic Story Through Data

A spatial-temporal GIS analysis of 25 years of New Zealand earthquake data (2001–2026), covering 74,000+ recorded events of magnitude 3.0 or greater.

Built in Python using Jupyter Notebook as a portfolio project exploring spatial analysis, kernel density estimation, and temporal trend modelling from scratch.

---

## Key Findings

**1. The Fault Nobody Knew About**
KDE analysis revealed a clear seismic hotspot beneath Christchurch — a location with no entry in the GNS Science Active Faults Database. Cross-referencing confirmed the database is current and maintained; the fault simply has no surface expression. It only became known to geologists when it ruptured in 2010–2011. The earthquake data independently fingerprinted its location without prior knowledge of its existence.

**2. A Fault Holding Its Breath**
The Alpine Fault — one of New Zealand's most dangerous, capable of a magnitude 8+ rupture — appears almost silent on both the KDE and trend maps. This absence is not reassurance. It reflects a locked fault accumulating stress, with the last major rupture in 1717 and a 75% estimated probability of another M8+ event before 2068 (GNS Science AF8 programme).

**3. Frequency vs Energy — Two Different Stories**
Frequency-based KDE and magnitude-weighted KDE produce meaningfully different maps. A handful of large events (Dusky Sound Mw7.8, 2009; Canterbury sequence, 2010–2011) dominate the energy map while frequent low-magnitude zones become less prominent. Neither map is wrong — they answer different questions.

---

## Methods

| Method | Purpose |
|---|---|
| Kernel Density Estimation (KDE) | Spatial heatmap of earthquake density |
| Magnitude-weighted KDE | Energy-weighted version using seismic moment formula |
| Moran's I (spatial autocorrelation) | Quantify and confirm clustering significance |
| Per-cell linear regression | Detect increasing/decreasing activity over 25 years |
| Temporal animation | Visualise how seismic patterns evolve year by year |

**Moran's I result:** I = 0.6695, p = 0.001, Z = 141.06 — confirming strong, statistically significant spatial clustering.

---

## Repository Structure

```
hidden-faults/
│
├── data/
│   ├── earthquakes-2001-2004.csv
│   ├── earthquakes-2004-2010.csv
│   ├── earthquakes-2010-2016.csv
│   └── earthquakes-2016-2026.csv
│
├── outputs/
│   ├── kde_heatmap.png
│   ├── magnitude_weighted_kde.png
│   ├── trend_analysis.png
│   ├── temporal_animation.gif
│   └── summary.json
│
├── hidden_faults_analysis.ipynb
├── Hidden_Faults_Report.pdf
└── README.md
```

> **Note:** Raw data sourced from the [GeoNet catalogue](https://www.geonet.org.nz/). Fault reference data from the [GNS Science New Zealand Active Faults Database](https://data.gns.cri.nz/af/).

---

## Requirements

```
geopandas
scipy
numpy
matplotlib
libpysal
esda
shapely
pandas
```

Install with:

```bash
pip install geopandas scipy numpy matplotlib libpysal esda shapely pandas
```

---

## How to Run

1. Clone the repository
2. Install dependencies (see above)
3. Open `hidden_faults_analysis.ipynb` in Jupyter Notebook
4. Run cells sequentially — each section builds on the previous

---

## Data Source

Earthquake data: [GeoNet](https://www.geonet.org.nz/) — New Zealand's geological hazard monitoring system, operated by GNS Science.

Active fault reference: [GNS Science New Zealand Active Faults Database (NZAFD)](https://data.gns.cri.nz/af/)

---

## Author

https://github.com/D1amond-GIT

*This project was completed as a self-directed portfolio piece. All analysis, interpretation, and writing are my own. Python and AI tools were used for debugging and problem-solving throughout.*
