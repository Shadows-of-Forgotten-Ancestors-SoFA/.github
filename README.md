# NASA space app challenge 2024 team SoFA

## The challenge 
A geographic information system (GIS) can create, manage, analyze, and map many types of data. With GIS and other mapping technologies, you can create a map of an area and layer open data over it spatially to reveal new, enriching insights. Your challenge is to create a map that incorporates open science data to explore how an issue in your community is shaped by the surrounding physical geography. Maybe you’re concerned about food deserts and want to analyze the locations of grocery stores in your neighborhood? Or perhaps you’d like to explore the impacts of pollution on the local water supply? There’s so much space for opportunity—all you have to do is map it!

## Structure
- ```geojsons-web```    
  web application for dust density map visualization
- ```geojsons-api```   
  web api returns geoJSON by timestamp
- ```netcdf-to-csv```   
  converts NetCDF datasets to csv format
- ```datasets-to-netcdf```   
  downloads datasets from remote sources, proceses this data and saves to NetCDF format
- ```ml```   
  AI random forest model that predicts NDVI and dust density


# How to

This section provides an overview of how to use the provided services. This code is designed to predict future Normalized Difference Vegetation Index (NDVI) and dust density by using raw data drom NetCDF.

1. Prepare and Process Data:
   - Download the required datasets (dust density and NDVI) from open sources like NASA and Copernicus.
   - Convert NetCDF data into CSV format using ```netcdf-to-csv```.
   - Check the structure of the datasets before running the machine learning scripts.

2. Train the Model:
   - Use the preprocessed data to train the Random Forest model with scripts proveded by ```ml```. The training script will predict future dust density and NDVI values.
   - Adjust the hyperparameters such as the number of estimators (trees) and tree depth for optimal results.
   
3. Deploy the API:
   - After training, run the ```geojsons-api``` Flask application to expose the predictions through a REST API. 
   - You can query the API to receive geoJSON formatted data by timestamp, representing future predictions of dust spread and NDVI impact.

4. Visualize Predictions:
   - The ```geojsons-web``` client fetches data from the API and renders it on a map as GeoJSON layers. 
   - Customize the front-end to display visualizations specific to your local community’s dust density and NDVI predictions.



## Data Sources
- Dust density input data source
  https://disc.gsfc.nasa.gov/datasets/M2TUNXAER_5.12.4/summary
- NDVI input data source
  https://www.wekeo.eu/data


## Links 
- Team page :
  https://www.spaceappschallenge.org/nasa-space-apps-2024/find-a-team/sofa/?tab=details 

- Chellenge description :
  https://www.spaceappschallenge.org/nasa-space-apps-2024/challenges/community-mapping/

## Contacts
- Viktor Chekhovych
  https://www.linkedin.com/in/viktor-chekhovych-a04240280/

- Ivan Kyrylov
  https://www.linkedin.com/in/ivan-kyrylov-597088216/

- Ashot Vdovychenko
  https://www.linkedin.com/in/ashot-vdovychenko-750069281/

- Lidiia Zaparenko
  https://www.linkedin.com/in/lidiia-zaparenko-647457317/

- Heorgii Holovanov
  https://www.linkedin.com/in/heorgii-holovanov-3bb826264/