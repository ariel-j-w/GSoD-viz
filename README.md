# Global State of Democracy
A visualization and exploration of key factors in the 2020 Global State of Democracy Index (GSoDi) data as found in `data/gsodi_pv_4.csv`.

## Dataset
This project relies on the [Global State of Democracy Index](https://www.idea.int/gsod-indices/dataset-resources), and the variables in the dataset can be understood through the [2019 cookbook](https://www.idea.int/gsod-indices/sites/default/files/idea-gsodi-2019-codebook-v3.pdf) and the [2020 provisional update](https://www.idea.int/gsod-indices/sites/default/files/gsodi_2020_update.pdf). 

### `Global State of Democracy Index 2020.png`
This image is a Lucidchart diagram I created to more quickly understand and conceptualize the shape of the dataset. Though the data should not be full interpreted without the use of the aforementioned cookbook, this image is an excellent resource for quick reference and on-the-fly translation of obscure variable names.

## Files
### `exploration.Rmd`
This R markdown files works with preliminary exploration and visualization of the data. A couple of files (`democracy-clusters.csv` and `genderEquality-correlation.csv`) are artifcats of the script, but the primary purpose of the document is to explore the data, build models for future visualizations, and conceptualize future work. None of the visualization in this document will be part of the final deliverable, but the models and calculations created through this script *will* be.

### `pre-processing.py`
This file takes the entire GSoDi data and splits it into different subsets for the purposes of training and testing models. Several csv files are created as an artificact of this file:
- `data/complete-2019.csv` - all GSoDi observations from 2019 (the most recent year of available data)
- `data/complete-countries.csv` - all years of GSoDi observations at the country level (removing aggregate regional data)
- `data/countries-2019.csv` - 2019 GSoDi observations at the country level
- `data/train-countries.csv` - 60% of all country data (for model training)
- `data/train-2019.csv` - 60% of the 2019 data (for model training) 
- `data/query-countries.csv` - 20% of all country data (for model querying)
- `data/query-2019.csv` - 20% of the 2019 data (for model querying)
- `data/train80-countries.csv` 80% of all country data (for model training; the complement of `data/test-countries.csv`)
- `data/train80-2019.csv` - 80% of the 2019 data (for model training; the complement of `data/test-2019.csv`)
- `data/test-countries.csv` - 20% of all country data (for model testing)
- `data/test-2019.csv` - 20% of the 2019 data for (for model testing)
