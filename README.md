# Visualization-CityofAustin311Calls README

## Overview

This project involves analyzing a dataset of service requests to identify trends, cluster service requests by category, and visualize the geographical distribution of specific categories of requests. The analysis covers data cleaning, exploration, visualization, and spatial analysis.

## Requirements

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - geopandas
  - folium
  - scikit-learn

## Installation

Ensure you have Python installed on your system. You can download Python from [the official website](https://www.python.org/downloads/).

Install the required Python libraries using pip:

```sh
pip install pandas numpy matplotlib geopandas folium scikit-learn
```

## Dataset 

The dataset is expected to be a CSV file containing service requests with various attributes such as service request number, description, method received, status, dates (created, last updated, status changed), latitude, and longitude coordinates, and a predicted category for the request. The predicted category column was creadted with SVM which is provided in repository "Semi-Supervised_SVM_Text_Classification" 

## Usage

### Data Loading and Cleaning:

- Load the dataset using pandas.
- Select relevant columns for the analysis.
- Convert date columns to datetime format.
- Clean and preprocess the data as necessary.

### Data Exploration and Visualization:

- Plot the number of service requests per month to identify trends over time.
- Analyze the distribution of service requests across different predicted categories.

### Spatial Analysis:

- Filter data for a specific category (e.g., Public Safety).
- Create a heatmap visualization of service requests for the category to identify hotspots.

## Code Snippets

### Data Loading:

```python
import pandas as pd
data = pd.read_csv("path_to_your_data.csv")
```
## Data Visualization:

```python
import matplotlib.pyplot as plt
# Example: Plotting service requests over time
plt.plot(date_column, count_column)
plt.show()
```
## Spatial Analysis with Folium:

```python
import folium
from folium.plugins import HeatMap
# Create a map and add a heatmap layer
map = folium.Map(location=[latitude, longitude], zoom_start=13)
HeatMap(data=[[lat, lon] for lat, lon in zip(latitudes, longitudes)]).add_to(map)
```
## Results:


