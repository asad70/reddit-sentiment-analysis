# reddit-sentiment-analysis
This program goes thru reddit, finds the most mentioned tickers and uses Vader SentimentIntensityAnalyzer to calculate the ticker compound value.  


## Sample Output
It took 216.65 seconds to analyze 5862 comments in 80 posts in 4 subreddits.

Posts analyzed saved in titles

10 most mentioned picks:\
GME: 197\
BB: 72\
FB: 56\
PLTR: 36\
TSLA: 25\
PLUG: 17\
RC: 15\
NIO: 14\
SPCE: 10\
TLRY: 10

&nbsp; &nbsp; &nbsp; &nbsp; Bearish &nbsp; Neutral &nbsp; Bullish &nbsp; Total/Compound\
GME    &nbsp; 0.087    &nbsp;0.763    &nbsp; &nbsp;0.150           &nbsp; &nbsp; &nbsp;0.161\
BB     &nbsp; 0.058 &nbsp;   0.768 &nbsp; &nbsp;   0.175           &nbsp; &nbsp; &nbsp;0.261\
FB     &nbsp; 0.119    &nbsp;0.708    &nbsp; &nbsp;0.173           &nbsp; &nbsp; &nbsp;0.127\
PLTR    &nbsp;0.062    &nbsp;0.804 &nbsp; &nbsp;   0.134           &nbsp; &nbsp; &nbsp;0.235\
TSLA    &nbsp;0.124    &nbsp;0.690    &nbsp; &nbsp;0.187           &nbsp; &nbsp; &nbsp;0.195\
![](mentioned.png)
![](sentiment.png)

## Data:
Includes US stocks with market cap > 100 Million, and price above $3. As wsb doesn't allow penny stocks discussions.\
Source:  https://www.nasdaq.com/market-activity/stocks/screener?exchange=nasdaq&letter=0&render=download 


Implementation:
I am using sets for 'x in s' comparison, sets time complexity for "x in s" is O(1) compare to list: O(n).


Limitations:
It depends mainly on the defined parameters for current implementation:
It completely ignores the heavily downvoted comments, and there can be a time when
the most mentioned ticker is heavily downvoted, but you can change that in upvotes variable.


