## Bitcoin Price Prediction via Natural Language Processing

### 1. Data Crawling
#### Twitter Data
- Crawl 7 days data with keyword 'Bitcoin' in order to find keywords or hashtags related to Bitcoin
- Generate a word cloud and choose 5 different keywords
- Using those five keywords, crawl five years amount data from Twitter
#### Price Chart Data
- Download five years amount Bitcoin price data in a csv format
### 2. Data Pre-Processing
#### Twitter Data
- Basic analysis using crawled data to use the data effectively e.g. Create a Likes or Retweets Frequency Graph
- Text Clening
  - Remove hashtags, urls, punctuation, etc.
  - Lemmatize words
  - Remove advertisements
  - Save the data in a new csv file
#### Twitter Sentiment Value
- Using textblob_sent library, calculate sentiment of each tweet.
- Save the result next to each corresponding Twitter data.
#### Final Dataset
- Merge the price dataset and the Twitter dataset by date in order to use it for the final prediction.
### 3. Modelling
#### Data
- Normalise data using MinMaxScaler
- Create a training and testing set, 70% and 30%.
#### LSTM
- Build LSTM layer with 128 internal units and a dense layer with 1 unit.
- Train and test the model
### 4. Findings
![Results](https://github.com/yunhe1/Bitcoin-Price-Prediction-via-Natural-Language-Processing/blob/master/LSTM%20predition.png)

- The prediction has been completed with high accuracy.
- There is a correlation between the bitcoin price variation and tweet sentiments of influencers.
- Future Bitcoing price changes may be predictable with influencer Twitter posts.
