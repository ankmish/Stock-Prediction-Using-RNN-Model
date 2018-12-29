### Predict stock market prices using RNN


#### Steps

It uses RNN Deep Learning algorithm to predict the Stock Market price.

1. Make sure `tensorflow` has been installed.
2. First download the full S&P 500 data from [Yahoo! Finance ^GSPC](https://finance.yahoo.com/quote/%5EGSPC?p=^GSPC) (click the "Historical Data" tab and select the max time period). And save the .csv file to `data/SP500.csv`.
3. Run `python data_fetcher.py` to download the prices of individual stocks in S & P 500, each saved to `data/{{stock_abbreviation}}.csv`.
(NOTE: Google Finance API returns the prices for 4000 days maximum. If you are curious about the data in even early times, try modify `data_fetcher.py` code to send multiple queries for one stock. Here is the data archive ([stock-data-lilianweng.tar.gz](https://drive.google.com/open?id=1QKVkiwgCNJsdQMEsfoi6KpqoPgc4O6DD)) of stock prices I crawled up to Jul, 2017. Please untar this file to replace the "data" folder in the repo for test runs.)
4. Run `python main.py --help` to check the available command line args.
5. Run `python main.py` to train the model.


