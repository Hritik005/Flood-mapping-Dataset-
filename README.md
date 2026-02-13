# Flood-mapping-Dataset-
This repository contians the necessary files for creating the Flood features as input data and output labels using which we can build a model which can be used for Flood mapping task 

The below is the link for a google drive which contain the necessary features by which we can build an input create an input for a flood mapping task and also by which we can create a output labels for the respective case .
https://drive.google.com/drive/folders/1H-6k0tp3iLPie3wXbRpFILZl3G-riPOA?ths=true

The repository focuses on three key data sources:

Sentinel-1 SLC SAR imagery for the selected flood events, enabling robust flood detection under all-weather and day-night conditions.

GPM (Global Precipitation Measurement) data to capture spatio-temporal precipitation dynamics associated with extreme rainfall events.

ERA5-Land reanalysis data to represent land-surface and hydrometeorological conditions such as soil moisture, temperature, and surface runoff proxies.

The workflow included in this repository aims to:

Organize and preprocess heterogeneous datasets into a consistent spatial and temporal framework.

Generate physically meaningful and learning-ready input features for flood mapping.

Promote reproducibility, scalability, and extensibility for future flood events and study regions.

Here we have also uploaded a example .ipynb file in which we have done some work with the gpm file whose extension is .hfd5 and also for our work we have currently downloaded the Imerge Final result file 
In order to read more about the gpm Api one can visit the site https://gpm-api.readthedocs.io/en/latest/tutorials/tutorial_02_IMERG.html

Here we have also uploaded a exmple .ipynb file where we have read the files which we have downloaded from ERA5Land site.
To study more about the Era5Land one can visit the site https://confluence.ecmwf.int/display/CKB/ERA5-Land%3A+data+documentation

Important Libraries which we have installed in our virtual environment in order to 
