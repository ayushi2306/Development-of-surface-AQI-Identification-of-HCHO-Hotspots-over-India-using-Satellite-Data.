# Why This Problem Is Challenging

At first glance, the problem appears straightforward: obtain satellite data, compute Air Quality Index (AQI), identify Formaldehyde (HCHO) concentrations, and visualize the results. However, the challenge is significantly more complex due to the nature of satellite observations and atmospheric science.

## 1. Satellites Do Not Measure Surface AQI

Satellites do not directly measure AQI. Instead, they observe atmospheric properties such as NO₂, CO, SO₂, HCHO, Aerosol Optical Depth (AOD), and other spectral information. AQI is a ground-level index designed to represent the air that humans breathe. Therefore, the primary challenge is to estimate surface-level air quality from atmospheric observations collected hundreds of kilometers above Earth.

---

## 2. Atmospheric Column vs Surface Concentration

Satellite instruments generally retrieve atmospheric column concentrations, representing the total amount of a gas through the atmosphere.

However, AQI depends on pollutant concentrations near the Earth's surface.

Converting atmospheric column measurements into surface concentrations requires statistical models, machine learning techniques, atmospheric correction methods, or data fusion with ground observations.

---

## 3. PM2.5 Cannot Be Directly Observed

PM2.5 is one of the most important pollutants contributing to AQI.

Most satellite missions do not directly observe PM2.5. Instead, they measure Aerosol Optical Depth (AOD), which indicates how much sunlight is scattered or absorbed by aerosols.

AOD is influenced by dust, humidity, smoke, clouds, and atmospheric conditions. Therefore, estimating PM2.5 from AOD is itself a challenging research problem.

---

## 4. Missing and Noisy Satellite Observations

Satellite observations are affected by:

* Cloud cover
* Rainfall
* Instrument noise
* Orbital revisit time
* Missing pixels

Consequently, preprocessing, filtering, interpolation, and quality assessment are essential before analysis.

---

## 5. Multi-Source Data Integration

Developing an accurate surface AQI model requires combining multiple datasets, including:

* Satellite observations
* Ground monitoring station data
* Meteorological parameters
* Fire detection datasets
* Land use and geographic information

Each dataset has different spatial resolutions, temporal resolutions, coordinate systems, and formats, making data integration a significant challenge.

---

## 6. Identifying HCHO Hotspots

Satellite products provide HCHO concentrations but do not identify pollution hotspots automatically.

A hotspot must be detected through spatial and temporal analysis by identifying regions where HCHO concentrations remain consistently or seasonally elevated relative to surrounding areas.

---

## 7. Attribution of Emission Sources

High HCHO concentrations do not necessarily indicate biomass burning.

Possible emission sources include:

* Agricultural residue burning
* Forest fires
* Industrial emissions
* Vehicular emissions
* Urban activities

Additional datasets such as active fire detections and meteorological observations are required to associate HCHO hotspots with biomass burning events.

---

## 8. Validation

Any estimated AQI model must be validated using ground-based monitoring stations.

Performance metrics such as RMSE, MAE, and R² are necessary to evaluate the reliability of the predictions.

---

## 9. Scalability

The objective is not simply to process a few satellite images but to build a system capable of generating daily air quality information over the entire country.

This requires designing an efficient and scalable processing pipeline that can handle large volumes of geospatial data.

---

## Summary

The primary challenge is not downloading satellite data. The real challenge is transforming atmospheric observations into meaningful ground-level air quality information through scientific analysis, data processing, statistical modeling, and geospatial intelligence.
