# ETL_Project
## Purpose
To compare different investment asset classes since early January to see how different classes have performed before, during, and after the recent crash due to global events surrounding the novel Coronavirus. The asset classes chosen include:
```
* Amazon - At home consumer purchase behavior
* Bitcoin - Crypto
* GLD ETF - Gold
* USO ETF - U.S. crude oil
* Netflix - At home entertainment
* S&P500 - The top 500 stocks and widely used indicator for stock performance
* SHY - Treasury Bond ETF
* USO ETF - U.S. crude oil
* ZOOM - Zoom: At home work life
```
## ETL Steps
* **E**xtract: We pulled original investment class sources from Yahoo Finance and [Kaggle](https://www.kaggle.com/) as CSVs.  
       
* **T**ransform: To clean our data, we:
```
* Dropped unnecessary columns
* Dropped Nulls upon merge
* Formatted date columns to be date vs object dataypes
* Renamed columns
* Filtered from <date> to <date> to get desired data
* Merged multiple dataframes
```

* **L**oad: Final Data was loaded into postgres sql. This was chosen based on the primary key (PK) function sql offers wherein the 'date' of future data stock/asset class inputs could be used as the primary key and future data inputs could be analyzed more easily.

## Results
![Trends](ETL_Project/Asset_Trends.png)
