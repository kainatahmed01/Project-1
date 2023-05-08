# Project 1 - Fintech: FX Market Analysis

## Purpose 

Showcasing FX currency market and comparing it to other global markets, focusing on trends and analysis. 

Pinpointing critical data sets to indicate market volatility/fluctuation and their correlation to current and past FX rates. 

Valuable asset for importers and exporters in goods/services industry for FX risk management strategies. 

Beneficial for day-traders in the FX markets and users making/sending international payments. 

## Technical Goals 

Use an API to collect today’s FX rates for USD/CAD, data Dow Jones Index, Gold, and India Index (NIFTY). 

Create an interactive world map that shows today’s FX rates for the Canadian dollar compared to other countries around the world.

Get correlation heatmaps for market fluctuations and FX rates. Use PyViz, GeoViews, and Hvplot to create six to eight data visualizations. 

## API Location 

Live and historical API data was taken from Historical Prices and Fundamental Financial Data API (eodhistoricaldata.com), which consists of 70+ stock exchanges all over the world and 30 year historical data. 

## Data Cleaning 

Pandas code used to pull EoD Historical Data specific to Major Market Indices around the world. 

The data is filtered to the 'close' column and Nulls are dropped. 

The time period of the data collected is 10 years.

## Mapping 

We used geoviews to create map, adding longitude and latitude to pinpoint the location of the major currency pairs.

## Correlation of USD/CAD FX to Dow Jones Index

Necessary Python packages are imported.

Environment variables are loaded using dotenv.

An instance of the EodHistoricalData class is set up to make requests to the EOD Historical Data API.

A time series request is set up to retrieve the daily close values for the Dow Jones Industrial Average stock index.

The response is converted to a Pandas DataFrame and cleaned up to only include the "close" column, which is then renamed to "DJIA".

The percentage change in DJIA value is calculated and null values are dropped from the DataFrame using the pct_change() and dropna() methods respectively.

Finally, the tail of the resulting DataFrame is printed to the console.

A scatter plot is created using the plot() method from the Pandas DataFrame.

The plot visualizes the relationship between the daily percentage change in the CAD/USD currency pair and the daily percentage change in the Dow Jones Industrial Average stock index.

The daily percentage change in USD/CAD is plotted on the x-axis and the daily percentage change in DJIA is plotted on the y-axis.

The correlation value is calculated using the corr() method from the Pandas DataFrame.

A heatmap visualization is then created using the heatmap() method from the Seaborn package to show the correlation on a scale from -1 to 1.

The heatmap represents the correlation between the two variables, where negative values indicate a negative correlation, positive values indicate a positive correlation, and values close to zero indicate little to no correlation.

## Note 

Similar methods of coding procedures implemented for correlation of USD/CAD FX to Gold, and India Index (NIFTY). 

## Summary of Analysis and Impact 

Based on our findings, we can conclude that the USD/CAD FOREX currencies are definitely influenced by markets that are structured primarily around the known global reserve currency, being the US dollar, when observing markets, such as the Dow Jones, S&P 500, and the Gold index. 

However, may not be as influenced or showing non-existent correlation with international markets structured around different currencies, such as the National Stock Exchange of India, which revolves primarily around the Indian rupee, as its main currency of exchange.

## Contributers 

Larry Gagnon, Ganna Kassantini, Kainat Ahmed, and Jassy Badwal. 
