# 🌍 Satellite PM2.5 Estimation using AI/ML

This project estimates **surface-level particulate matter (PM2.5)** concentrations using:
- **Satellite-based AOD (Aerosol Optical Depth)**
- **Ground-based pollution station data**
- **Atmospheric reanalysis meteorological data**
- **Machine learning models**

It combines **remote sensing** and **AI/ML** to enable spatial air quality monitoring, especially in regions with sparse ground coverage.

---

## 📌 Objectives

- Predict PM2.5 levels using INSAT AOD and ERA5/MERRA-2 meteorological parameters.
- Fuse ground station data from CPCB with satellite and reanalysis sources.
- Generate high-resolution PM maps across selected Indian regions.
- Evaluate prediction accuracy using regression metrics.

---

## 🛰️ Data Sources

| Dataset         | Source                                                      |
|----------------|-------------------------------------------------------------|
| AOD (Aerosol Optical Depth) | INSAT-3D/3DR/3DS (via [MOSDAC](https://www.mosdac.gov.in/))   |
| PM2.5 Ground Truth         | CPCB India (https://app.cpcbccr.com/)           |
| Meteorological Variables   | [ERA5](https://cds.climate.copernicus.eu/) or [MERRA-2](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/) |

---

## 🧠 Methodology

1. **Data Collection**
   - Download AOD, meteorological, and PM2.5 datasets
2. **Preprocessing**
   - Reproject, resample, interpolate datasets to common grid
3. **Feature Engineering**
   - Merge AOD + met features for ground station locations
4. **Model Training**
   - Use Random Forest / XGBoost / Deep Learning models
5. **Prediction & Mapping**
   - Generate PM2.5 raster maps for entire regions
6. **Evaluation**
   - Validate predictions against held-out CPCB stations

---

## 🧰 Tech Stack

- Python, Pandas, NumPy, Scikit-learn
- XGBoost / LightGBM / TensorFlow
- xarray, netCDF4, Rasterio, GeoPandas
- Matplotlib, Seaborn, Plotly
- Jupyter Notebooks
- (Optional) Streamlit for visualization

---

## 📊 Example Outputs

- PM2.5 vs AOD scatter plots  
- Time series plots per station  
- Spatial PM prediction maps (GeoTIFF/PNG)  

*Sample visualizations coming soon...*

---

## 🚀 Future Plans

- Add LSTM-based temporal modeling  
- Extend to PM10 and AQI classification  
- Deploy a Streamlit dashboard for real-time querying  
- Open data API endpoint for developers

---

## 📁 Project Structure (tentative)

```

satellite-pm2.5-estimation/
│
├── data/               # Raw & processed datasets
├── notebooks/          # Jupyter notebooks for EDA, modeling
├── src/                # Python scripts for preprocessing, training
├── models/             # Saved model files
├── outputs/            # Maps, plots, reports
├── README.md
└── requirements.txt

```

---

## 📜 License

[MIT License](LICENSE)

---

## 🙌 Acknowledgements

- ISRO MOSDAC team for satellite data
- CPCB for pollution datasets
- ERA5/MERRA-2 for atmospheric data
- Open-source tools and contributors
