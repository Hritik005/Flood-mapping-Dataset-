# Flood-mapping-Dataset-
This repository contians the necessary files for creating the Flood related input features and output labels using which we can train a model for Flood mapping task.

The repository provides different geospatial and hydrometeorological datasets which can be combined to generate meaningful features for flood detection and prediction.

The below is the link for a google drive which contain the necessary features by which we can build an input feature for a flood mapping task and also by which we can create a output labels for the respective case .
https://drive.google.com/drive/folders/1H-6k0tp3iLPie3wXbRpFILZl3G-riPOA?ths=true

The repository focuses on three key data sources:

# 1.Sentinel-1 SLC SAR Imagery
Sentinel-1 Synthetic Aperture Radar (SAR) imagery is used for flood detection because it can operate under all-weather conditions and during both day and night. SAR data is highly effective for identifying water surfaces during flood events.

# 2. GPM (Global Precipitaion Measurement)- IMERG Final Run
GPM IMERG data provides high-resolution precipitation measurements, which are essential for understanding extreme rainfall events that lead to flooding.

# 3. ERA5-Land Reananlysis Data
ERA5-Land provides land surface and hydrometeorological variables such as:
  
  (a)Soil moisture
  
  (b)Surface temperature
  
  (c) Runoff proxies
  
  (d) Other land surface parameters

These variables help capture the environmental conditions that influence flood occurrence.

# Additional Geospatial Features
To improve the flood mapping feature set, we have also included terrain and land-surface related information.
# DEM (Digital Elevation Model)
A Digital Elevation Model (DEM) has been included to represent the elevation of the terrain in the study region. Terrain elevation plays a crucial role in determining water flow direction and flood-prone areas.
# Slope (Derived frim DEM)
Using the DEM, we extracted the slope of the terrain, which represents the rate of elevation change.
Areas with steeper slopes tend to allow faster water flow.
Areas with lower slopes tend to accumulate water, making them more vulnerable to flooding.

The workflow included in this repository aims to:

Organize and preprocess heterogeneous datasets into a consistent spatial and temporal framework.

Generate physically meaningful and learning-ready input features for flood mapping.

Promote reproducibility, scalability, and extensibility for future flood events and study regions.

# Example Notebooks
Example Jupyter notebooks have been included to demonstrate how to work with the datasets.
# gpm.ipynb
Here we have also uploaded an example gpm.ipynb file in which we have shown how to read and process GPM precitation files (.HDF formate) and also for our work we have currently downloaded the Imerge Final result file. For any perticular event we have first downloaded the sentinel 1 SLC data for that day and we have also downloaded the gpm data of last 24 hours (wrt the time of which we have the sentinel 1 SLC images) with a temporal resolution of 30 mins.
In order to read more about the gpm Api one can visit the site https://gpm-api.readthedocs.io/en/latest/tutorials/tutorial_02_IMERG.html

# ERA5-Land Data processing
Here we have also uploaded an exmple era5_land_tutorial_commented.ipynb file where we have read the files which we have downloaded from ERA5Land site.
To study more about the Era5Land one can visit the site https://confluence.ecmwf.int/display/CKB/ERA5-Land%3A+data+documentation

# For rest of data (.tif file)
In order to process rest of the .tif files we can use rasterio library .
we can study about rasterio library we can visit the site
https://pypi.org/project/rasterio/

# About the Google drive
In Initial stages we have collected the data related to the Flood events in Kolkata.
# Flood Event Identification
In order to collect flood-related datasets, we followed two different approaches to identify potential flood events.
# Approach 1: Social Media and Official Reports
In the first approach, we identified flood events by analyzing reliable social media pages and reports from official authorities such as police departments and local administrative pages.
For example, in the case of Kolkata, several waterlogging and urban flood events were reported by official police accounts and trusted information sources. Based on these reports, we collected the corresponding satellite and climate datasets for those specific dates.

The Google Drive dataset contains a folder named kolkata, which includes the data collected using this approach.
Inside the kolkata folder, the data is organized into the following subfolders:
DEM – Digital Elevation Model used for terrain analysis and slope extraction.
ERA5_land – ERA5-Land reanalysis data providing hydrometeorological variables such as soil moisture, temperature, and evaporation.
Global Precipitation – GPM IMERG precipitation data capturing rainfall conditions during the event.
Sentinel 1 SLC – Sentinel-1 SAR imagery used for detecting water surfaces and flood extent.
These datasets together provide multi-source information required to analyze and model flood events.

# Approach 2:Rainfall Threshold-Based Flood Event Selection
In the second approach, flood events were identified using precipitation-based criteria.
We analyzed daily rainfall data for multiple cities over the last five years. Whenever the total rainfall on a particular day exceeded 50 mm, that day was considered a potential flood event.
The rationale behind this approach is that heavy rainfall events are often strongly associated with urban flooding and waterlogging, especially in densely populated cities with limited drainage capacity.

The Google Drive dataset therefore contains another folder named:
precipitation on any particular day more than 50 mm

This folder contains data corresponding to the dates where the rainfall threshold condition was satisfied.

# Dataset Organization

The dataset provided in the Google Drive link is structured as follows:

Project

│

├── kolkata

│   ├── DEM

│   ├── ERA5_land

│   ├── Global Precipitation

│   └── Sentinel 1 SLC

│

└── precipitation on any particular day more than 50 mm

Both approaches together help build a more comprehensive flood dataset for training and evaluating flood mapping models.
