
# Predicting Flood Potential for the San Lorenzo River Basin, California

This project focuses on predicting flood potential based on rainfall data for the San Lorenzo River Basin, located in California. The data is derived from stream gage and rainfall measurements collected from various sources over a 10-year period, from 09/01/2014 to 09/01/2024.

## Data Sources

- **Stream Gage Data**: Downloaded from the [USGS monitoring station 11160500](https://waterdata.usgs.gov/monitoring-location/11160500/#parameterCode=00065&period=P7D&showMedian=false), this dataset provides river height (in feet) and streamflow (in cubic feet per second) recorded every 15 minutes.
  
- **Precipitation Data**: Extracted from the [California Data Exchange Center (CDEC)](https://cdec.water.ca.gov/dynamicapp/wsSensorData). Four rainfall monitoring stations in the San Lorenzo Watershed were selected:
  
  | Location            | Code | Elevation | Latitude  | Longitude    | County     | Agency                              |
  |---------------------|------|-----------|-----------|--------------|------------|-------------------------------------|
  | BEN LOMOND (CDF)     | BLO  | 2630      | 37.132000 | -122.169998  | SANTA CRUZ | CA Dept of Forestry and Fire Protection |
  | SCHULTIES RD         | SCH  | 1400      | 37.132999 | -121.969002  | SANTA CRUZ | Santa Cruz County                   |
  | BOULDER CREEK        | BDC  | 800       | 37.141998 | -122.163002  | SANTA CRUZ | Santa Cruz County                   |
  | BEN LOMOND           | BLN  | 365       | 37.092999 | -122.074997  | SANTA CRUZ | Santa Cruz County                   |

## Interactive Map

If you want to explore a map of the area, navigate to the `Interactive-Web` directory and run `index.html` in your local browser. This will provide a web-based interactive map of the San Lorenzo River Basin area.
"""

## Required Libraries

Below is the required set of libraries needed to run the code. The notebook checks if the libraries are installed and installs any that are missing:

- `pandas`, `matplotlib`, `geopandas`, `openpyxl`, `bokeh`, `plotly`, `seaborn`, `scikit-learn`, `imbalanced-learn`, and `xgboost`.

For compatibility, use Python 3.10 or lower as the notebook may not work with Python 3.13 due to known issues with Pandas as of October 2024.

## Notebook Outline

### 1. **ETL (Extract, Transform, Load)**
   - Extracting data from the USGS stream gage and precipitation datasets for the San Lorenzo River Basin.
   - Cleaning and formatting the data to ensure it is suitable for analysis.

### 2. **Exploratory Data Analysis (EDA)**
   - Visualizing data trends using libraries like `matplotlib`, `plotly`, and `seaborn`. Key visualizations include rainfall over time, streamflow trends, and peak gage height comparisons.
   - Summary statistics and distribution checks to understand the structure of the data.

### 3. **Data Engineering**
   - Preparing features and labels for the modeling process.
   - Creating new features like cumulative rainfall, peak river gage height, and lagged variables that help with predicting flood events.

### 4. **Modeling Flood Potential with Machine Learning**
   - Using `scikit-learn` and `xgboost` to create machine learning models for flood prediction.
   - Models are trained using historical rainfall and streamflow data to predict potential flood events.
   
## Setup

### Prerequisites
Ensure you have the following Python packages installed:

```bash
pip install pandas matplotlib geopandas openpyxl bokeh plotly seaborn scikit-learn imbalanced-learn xgboost
```

### How to Use

1. Clone the repository and navigate to the directory containing the notebook.
2. Open the `Predicting Flood Potential.ipynb` notebook.
3. Run the cells sequentially to load data, perform EDA, process data, and run machine learning models to predict flood potential.

## Results

- The notebook produces visualizations of rainfall, streamflow, and river height.
- Machine learning models predict flood potential based on rainfall and river gage data.
- Insights can be used to identify high-risk flood periods in the San Lorenzo River Basin.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
