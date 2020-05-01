# ETL_Project
## Project Report
* **E**xtract: 
        *Our original sources of data is from Yahoo Finance and [Kaggle](https://www.kaggle.com/)
        *The Data was formated as csv files for download.
* **T**ransform: 
        *To Clean our data, we used:
                *Drop Columns. 
                *Drop Nulls
                *Format date column to be date datatype
                *Rename columns
                *Filter from <date> to <date> to get desired data
                *Merge multiple dataframes
                
* **L**oad: 
        *Final Data was loaded into postgres sql. This was chosen based on primary key (PK) function sql offers. Making 'date' to be the PK would make future data input and relate to other stock data sets more easily. 
