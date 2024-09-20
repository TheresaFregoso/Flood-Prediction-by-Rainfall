# Project Proposal

## Visual Flooding Model of the San Lorenzo River Incorporating QGIS and ETL Processes

**Prepared by:** Theresa Fregoso
**Date:** 09/19/24

---

## Table of Contents

1. Introduction  
2. Problem Statement  
3. Objectives  
4. Methodology  
   - 4.1 Data Extraction (ETL - Extract)  
   - 4.2 Data Transformation (ETL - Transform)  
   - 4.3 Data Loading (ETL - Load)  
   - 4.4 Exploratory Data Analysis (EDA)  
   - 4.5 Machine Learning Model Development  
   - 4.6 Flood Inundation Mapping  
   - 4.7 Visualization and User Interface  
5. Data Sources  
6. Technologies to Be Used  
7. Project Timeline  
8. Expected Outcomes  
9. Conclusion  
10. References  

---

## 1. Introduction

Flooding is a significant natural hazard that poses risks to life, property, and the environment. The San Lorenzo River in California has experienced numerous flooding events that have impacted local communities and ecosystems. With climate change potentially increasing the frequency and severity of such events, there is an urgent need for tools that can help predict and visualize flood scenarios.

This project aims to develop a visual flooding model of the San Lorenzo River using machine learning techniques and geospatial data analysis, incorporating **ETL processes** and **QGIS** for enhanced data handling and visualization. The model will serve as a valuable tool for local authorities, planners, and residents to understand and prepare for potential flood events.

---

## 2. Problem Statement

Current flood prediction models and maps may lack real-time predictive capabilities and interactive features essential for effective decision-making. The primary challenge is to create an accurate and user-friendly visual model that simulates flood scenarios for the San Lorenzo River. This model should integrate various factors such as river flow rates, rainfall, terrain elevation, and land use to predict flood extents and visually present this information in an accessible manner.

---

## 3. Objectives

- **Develop a Machine Learning Model:** Utilize historical hydrological and meteorological data to predict flood levels and extents.

- **Implement ETL Processes:** Establish a clear and efficient ETL pipeline for data extraction, transformation, and loading.

- **Enhance Spatial Analysis with QGIS:** Incorporate QGIS for advanced geospatial data processing and analysis.

- **Create a Visual Flooding Model:** Build an interactive map that visualizes potential flood scenarios based on machine learning predictions and spatial analysis.

- **Utilize Appropriate Technologies:** Employ Scikit-learn for machine learning, Python Pandas for data manipulation, Matplotlib or Plotly for visualization, and QGIS for geospatial analysis.

- **Meet Project Requirements:** Ensure the project aligns with specified requirements by using at least two of the required technologies.

---

## 4. Methodology

### 4.1 Data Extraction (ETL - Extract)

- **Hydrological Data Extraction:**
  - Use APIs or web scraping techniques to extract historical river flow rates, water levels, and discharge data from the **USGS National Water Information System**.

- **Meteorological Data Extraction:**
  - Retrieve rainfall and weather data from **NOAA** or local weather stations using API calls or data downloads.

- **Spatial Data Extraction:**
  - Download DEMs and land cover data from the **USGS National Map** and **NLCD**.

- **Database Connectivity (Optional):**
  - Connect to databases (SQL/MongoDB) if data is stored remotely.

### 4.2 Data Transformation (ETL - Transform)

- **Data Cleaning:**
  - Handle missing values, duplicates, and anomalies using **Python Pandas**.
  - Standardize data formats, units, and timestamps.

- **Data Integration:**
  - Merge datasets based on common keys (e.g., date, location).

- **Data Enrichment:**
  - Calculate additional attributes like cumulative rainfall, moving averages, and lagged variables.

- **Spatial Data Processing with QGIS:**
  - Reproject spatial datasets to a common Coordinate Reference System (CRS).
  - Clip and mask spatial data to focus on the study area.

### 4.3 Data Loading (ETL - Load)

- **Data Storage:**
  - Load transformed data into a centralized storage system or database for easy access.
  - For spatial data, save processed layers in formats like GeoPackage or Shapefile using QGIS.

- **Data Accessibility:**
  - Ensure that both the machine learning models and visualization tools can access the cleaned and transformed data.

### 4.4 Exploratory Data Analysis (EDA)

- **Statistical Analysis:**
  - Use **Pandas** and **Matplotlib** to perform statistical analysis and visualize data distributions.

- **Spatial EDA with QGIS:**
  - Analyze spatial patterns and relationships.
  - Generate heat maps and overlay analysis to identify flood-prone areas.

### 4.5 Machine Learning Model Development

- **Model Selection:**
  - Implement regression algorithms like **Random Forest** or **Gradient Boosting** using **Scikit-learn**.

- **Training and Testing:**
  - Split data into training and testing sets.
  - Train the model using historical data.

- **Hyperparameter Tuning:**
  - Optimize model performance using techniques like Grid Search.

- **Model Validation:**
  - Evaluate the model using metrics like Mean Squared Error (MSE) and R-squared values.

### 4.6 Flood Inundation Mapping

- **Flood Modeling in QGIS:**
  - Use QGIS to simulate flood scenarios by applying predicted water levels to the DEM.
  - Perform raster calculations and generate inundation maps.

- **Geospatial Analysis:**
  - Analyze the impact on land use, infrastructure, and population.

- **Data Export:**
  - Export inundation layers for use in web applications and further analysis.

### 4.7 Visualization and User Interface

- **Interactive Mapping:**
  - Utilize **qgis2web** to export maps to interactive web formats.
  - Alternatively, use **Folium** in Python for interactive mapping.

- **Web Application Development:**
  - Build a web interface using **HTML/CSS/Bootstrap**.
  - Integrate visualizations and provide user controls for scenario selection.

---

## 5. Data Sources

- **USGS National Water Information System:**  
  https://waterdata.usgs.gov/nwis

- **NOAA National Centers for Environmental Information:**  
  https://www.ncei.noaa.gov/

- **USGS National Map (DEM Data):**  
  https://viewer.nationalmap.gov/basic/

- **National Land Cover Database (NLCD):**  
  https://www.usgs.gov/core-science-systems/national-geospatial-program/national-map

- **FEMA Flood Map Service Center:**  
  https://msc.fema.gov/portal/home

---

## 6. Technologies to Be Used

- **ETL Tools:**
  - **Python Pandas:** For data extraction and transformation.
  - **SQL/MongoDB:** For data loading and storage.

- **Machine Learning:**
  - **Scikit-learn:** For model development.

- **Data Visualization:**
  - **Matplotlib/Seaborn:** For static plots.
  - **Plotly:** For interactive visualizations.

- **Geospatial Tools:**
  - **QGIS:** For spatial data processing and mapping.
  - **GeoPandas:** For geospatial data manipulation in Python.

- **Web Development:**
  - **HTML/CSS/Bootstrap:** For front-end design.
  - **Flask/Django:** For back-end development.
  - **Leaflet.js/qgis2web:** For interactive web maps.

---

## 7. Project Timeline

### Week 1: Data Extraction and Transformation

- **Day 1-2:**
  - Extract data from all sources.
  - Set up database connections if necessary.

- **Day 3-5:**
  - Transform data using Pandas and QGIS.
  - Perform data cleaning and integration.

- **Day 6-7:**
  - Load transformed data into storage systems.
  - Begin exploratory data analysis.

### Week 2: Model Development and Validation

- **Day 8-10:**
  - Develop initial machine learning models.

- **Day 11-12:**
  - Perform hyperparameter tuning.

- **Day 13-14:**
  - Validate and finalize the model.

### Week 3: Mapping and Visualization

- **Day 15-16:**
  - Create flood inundation maps in QGIS.

- **Day 17-19:**
  - Develop interactive maps using qgis2web or Folium.

- **Day 20-21:**
  - Design and develop the web application interface.

### Week 4: Integration and Deployment

- **Day 22-24:**
  - Integrate the ML model, maps, and web interface.

- **Day 25-26:**
  - Perform testing and debugging.

- **Day 27:**
  - Prepare documentation and user guides.

- **Day 28:**
  - Final review and project submission.

---

## 8. Expected Outcomes

- **Efficient ETL Pipeline:**
  - A well-documented ETL process for data management.

- **Predictive Machine Learning Model:**
  - An accurate model for predicting flood levels.

- **Interactive Visual Flooding Model:**
  - A user-friendly web application with interactive maps.

- **Data Insights:**
  - Comprehensive analysis of factors affecting flooding.

- **Project Documentation:**
  - Detailed reports on methodology, findings, and recommendations.

---

## 9. Conclusion

By establishing a clear ETL process and incorporating advanced geospatial analysis through QGIS, this project aims to create a robust visual flooding model of the San Lorenzo River. The integration of machine learning and interactive visualizations will provide valuable tools for stakeholders to assess and mitigate flood risks.

---

## 10. References

- **USGS National Water Information System**
- **NOAA National Centers for Environmental Information**
- **USGS National Map**
- **National Land Cover Database**
- **FEMA Flood Map Service Center**
- **QGIS Documentation:**  
  https://www.qgis.org/en/docs/index.html
- **Python Libraries Documentation:**
  - Pandas: https://pandas.pydata.org/
  - Scikit-learn: https://scikit-learn.org/
  - Matplotlib: https://matplotlib.org/
  - GeoPandas: https://geopandas.org/
  - Rasterio: https://rasterio.readthedocs.io/
  - Folium: https://python-visualization.github.io/folium/
  - qgis2web Plugin: https://github.com/tomchadwin/qgis2web

---

**Prepared by:**  
Theresa Fregoso

**Date:**  
9/19/24
---



---
