# Global State of Democracy
A visualization and exploration of key factors in the 2020 Global State of Democracy Index (GSoDi) data as found in `data/gsodi_pv_4.csv`.

## Files
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
