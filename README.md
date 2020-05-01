# ETL_Project
## Purpose
To compare different investment asset classes since early January to see how different classes have performed before, during, and after the recent crash due to global events surrounding the novel Coronavirus. The asset classes chosen include:
```
* Amazon - At home consumer purchase behavior
* Bitcoin - Crypto
* GLD ETF - Gold
* USO ETF - U.S. crude oil
* Netflix - At home entertainment
* S&P500 - Stock market index that measures the stock performance of the 500 large companies listed on stock exchanges in the United States. A widely used indicator for stock performance, many consider it to be one of the best representations of the U.S. stock market as a whole.
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
![Asset_Trends](https://user-images.githubusercontent.com/37835407/80780252-4d55f900-8b3c-11ea-88b4-e1f5b85c3b91.png)

### Findings:
```
* AMZN (Amazon) - Saw its largest decline from February highs on March 13th, however it quickly grew after that as more people stayed home and increased ordering items online.
* BTC (Bitcoin)- A typically risky asset, also saw steep declines very quicly between March 11 and 12, and has only been on a steady increase since. 
* GLD (SPDR Gold ETF) - Gold is typically seen as a safe asset during times of crisis and people will rush to invest in it versus other riskier assets like stocks.  We see that here with its rise along with Amazon.
* NFLX (Netflix) - Like Amazon, Netflix has been on a meteoric rise since the crash due to more people staying home and consuming more media.  It is trading above even its highs earlier in the year.
* SHY (iShares 1-3 Year U.S. Treasury Bond ETF) - Also considered a very safe asset in times of crisis it has never seen declines, and has only increased since mid-March.
* SP (S&P 500) - March 23rd was the day when the S&P 500 saw it biggest lows and has been on a somewhat steady rise since.  It is still still below where it was in January however.
* USO (United States Oil ETF) - Has only been on a decline since earlier in 2020 as less energy is consumed due to people all around the world staying home.  It never sees an increase unlike the other asset classes.
```
