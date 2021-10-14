# data-512-a2
This repository contains code and data for an analysis of Wikipedia articles on politicians related to country population. 
This was created as a homework assignment for DATA 512, Autumn 2021, by Emily Linebarger (elineb@uw.edu).

## Organization
The directory structure of the repository is as follows: 

 ### raw/: 
 Contains raw, unaltered data from outside sources
1. WPDS_2020_data - WPDS_2020_data.csv.csv: Raw data from the World Population Data Set, found at https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit#gid=283125346. Originally accessed on October 9, 2021. 
2. country/ : Unzipped folder of Politicians by Country dataset from FigShare. Available at https://figshare.com/articles/dataset/Untitled_Item/5513449. Originally accessed on October 9, 2021. 

### cleaned/: 
Contains cleaned data used for analysis. 
1. pages_with_scores.csv: Contains all of the pages from the Politicians by Country dataset that could be assigned a score by the ORES model. 
2. population.csv: Contains the cleaned WPDS 2020 data. 
3. unable_to_score_pages.csv: Contains the pages from the Politicians by Country dataset that could not be assigned a score by the ORES model.
4. wp_wpds_politicians_by_country.csv: Contains the results from the merged population and politicians datasets. Only rows that matched on 'country' value and were able to be scored by the ORES model were kept in this dataset. 
5. regions_to_countries_map.csv
6. politicians.csv: Contains the cleaned Politicians by Country data. Some pages were dropped from the raw dataset; please see 'hcds-a2-bias.ipynb' for notes. 
7. wp_wpds_countries-no_match.csv: Contains the results from the merged population and politicians datasets that were unable to be matched with a score through the ORES model. 

### api_queries_raw/: 
This folder contains raw JSON queries from the ORES machine learning API. These queries were saved to aid in reproducibility. 

### cleaned_queries/:
This folder contains the cleaned JSON query results from api_queries_raw, which are then used for the analyses in the final sections of the notebook. 


## Reproduction
All code is contained in the jupyter notebook "hcds-a2-bias.ipynb', which can be rerun from the start to reproduce the analysis. 

## License
This code is licensced by a MIT License. 

