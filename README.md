# UNDatathon
This repository contains data and code for the UN-Datathon 2023 team UN-Mercatorians.

## AIS extraction

The notebooks `notebooks/ais_extract_ports.ipynb` and `notebooks/ais_extract_straits.ipynb` (TODO) extract the raw shipping data from spark. (Note: `notebooks/ais_extract_ports.ipynb` uses a HTML data URL to make the resulting csv files available, therefore the notebook could not be saved after execution).

Once all raw ship csvs are generated, the `notebooks/ais_merge_all.ipynb` notebook merges the data into one big csv file.
The `notebooks/ais_agg.ipynb` notebook identifies ships by their MMSI id and determines whether for any given point in time the ship has been to one of the locations of interest in the past two months. The locations of interest are Ukrainian Ports, Russian Western Ports, the Bosphorus Strait, and the Suez Canal.
Finally, `notebooks/ais_analysis.ipynb` does some preliminary exploratory analysis of the data.
