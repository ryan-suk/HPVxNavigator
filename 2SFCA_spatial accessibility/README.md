# 📍 Spatial Accessibility to VFC Providers in Georgia (2SFCA Analysis)

**HPVx Navigator | ACS-Funded HPV Vaccination Project**

This repository contains geospatial analysis code, data, and visualizations for measuring spatial access to **Vaccines for Children (VFC) providers** across Georgia ZIP Code Tabulation Areas (ZCTAs). This effort supports equitable HPV vaccination strategies through data-driven mapping of healthcare availability.

---

## 🚀 What This Project Does

✔️ Uses the **Two-Step Floating Catchment Area (2SFCA)** method  
✔️ Computes accessibility scores for each ZCTA  
✔️ Incorporates real travel times via **OpenRouteService API**  
✔️ Maps VFC provider-to-population access within a 30-minute drive  
✔️ Highlights access deserts to inform outreach & resource planning  

---

## 📊 Why It Matters

Access to vaccination isn't just about the availability of a free vaccine—it's about reach. By modeling drive-time catchments and population needs, this analysis helps identify **underserved areas**, supporting more equitable vaccination coverage.

---

## 🧩 Data Inputs

- `zcta_score_data.csv` – Georgia ZCTA centroids + population under age 18  
- `vfc_providers_geocoded.csv` – Geocoded addresses of all active VFC providers in GA  
- `ACS2020_Demographic_SexAge_ZCTA.shp` – ZCTA boundary file for optional mapping

---

## 🧠 Methodology Summary

### Step 1: Compute Provider Ratios (Rj)
Each VFC provider's catchment includes all ZCTAs reachable within **30 minutes by car**. We calculate:


### Step 2: Compute ZCTA Accessibility (As)
Each ZCTA’s accessibility score sums all `Rj` values from providers reachable within 30 minutes:


---

## 🗺️ Outputs

- `2sfca_vfc_ga.csv` — ZCTA-level accessibility scores  
- `2sfca_vfc_map.html` — Interactive folium map  
- Heatmaps and scatter plots showing spatial trends

---

## 🔧 Dependencies
```bash
pandas
numpy
openrouteservice
folium
matplotlib
geopy
geopandas        # only needed for preprocessing shapefiles
```
---

## 💡 Usage
- Configure your OpenRouteService API key
- Run 2sfca_analysis.py (or batch script for large-scale runs)
- View results in Excel, CSV, or HTML map

## 👥 Contributors
Ryan Suk, PhD - Emory University (HPVx Navigator Principal Investigator)


## 📬 Contact
For questions or collaboration:

📧 ryan.suk@emory.edu

🔗 www.ryansuk.com 

## 🧭 Citation
If using this analysis or methodology in publications or presentations, please cite:

doi - coming soon..


---


