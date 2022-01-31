# Cherry Blossom Peak Bloom Prediction

## Generating datasets and training the model

1. Download ghcnd_all.tar.gz https://www1.ncdc.noaa.gov/pub/data/ghcn/daily/ and extract on preprocessing_data
2. Download ghcnd-stations.txt https://www1.ncdc.noaa.gov/pub/data/ghcn/daily/ and save on preprocessing_data
3. Execute gen_stations_data.ipynb to gen a dataset (preprocessing_data/stations.parquet) that contains the location and id of all climate stations
4. Execute gen_eua_csv.ipynb to process the USA-NPN_status_intensity_observations_data.csv create the eua.csv file that has the same format as the other .csv on the same folder
5. Execute gen_full_station_data.ipynb to generate an aggregate file with all the data for all stations on merged_bloom. It also saves aggregated information for each station on preprocessing_data/stations and the best station for each location on preprocessing_data/best_station
6. Execute kyoto.ipynb, liestal.ipynb, washingtondc.ipynb or vancouver.ipynb to train the model
