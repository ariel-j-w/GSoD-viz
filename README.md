# Global State of Democracy
A visualization and exploration of key factors in the 2020 Global State of Democracy Index (GSoDi) data as found in `data/gsodi_pv_4.csv`. Ultimately this project;s final form lives on [my personal portfolio](https://ariel-j-w.github.io/democracy-project/). If you haven't been already, I'd start there for first understanding of this body of worl.

## Dataset
This project relies on the [Global State of Democracy Index](https://www.idea.int/gsod-indices/dataset-resources), and the variables in the dataset can be understood through the [2019 cookbook](https://www.idea.int/gsod-indices/sites/default/files/idea-gsodi-2019-codebook-v3.pdf) and the [2020 provisional update](https://www.idea.int/gsod-indices/sites/default/files/gsodi_2020_update.pdf). 

### `GSoD-Overview.png`
This image is a Lucidchart diagram I created to more quickly understand and conceptualize the shape of the dataset. Though the data should not be fully interpreted without the use of the aforementioned cookbook, this image is an excellent resource for quick reference and on-the-fly translation of obscure variable names.

## Key Files
In general, each of the key files are self-documenting, but here is a quick overview of each.

### `exploration.Rmd`
This R markdown files works with preliminary exploration and visualization of the data. A couple of files (`democracy-clusters.csv` and `genderEquality-correlation.csv`) are artifcats of the script, but the primary purpose of the document is to explore the data, build models for future visualizations, and conceptualize future work. None of the visualization in this document will be part of the final deliverable, but the models and calculations created through this script *will* be.

### `pre-processing.ipynb`
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

### `genderEquality.Rmd`
Arguably the most interesting file in this repository, here I perform decision tree analysis in order to identify strong predictors of gender equality.

### `GSoDi.twb`
This does not natively render well on GitHub, but if you check out the repository you will find here a Tableau workbook where I created some key visualizations that are ultimately housed on my portfolio.
