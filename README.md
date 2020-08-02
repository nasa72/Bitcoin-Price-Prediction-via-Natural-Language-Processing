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
:--:
*Prediction Result*

- The prediction has been completed with a high accuracy.
- There is a correlation between the bitcoin price variation and tweet sentiments of influencers.
- Future Bitcoing price changes may be predictable with influencer Twitter posts.

### 5. Rooms for Improvement
- **Still remaining advertisements:** Since there were many advertisements tweets we were not able to delete all of them. It might be positively or negatively affect the model or the final prediction. They aslo could cause errors. In order to remove as many ads as possible, more time should be invested in the preprocessing process.
- **Use of textblob_sent library:** We used Textblob library to calculate sentiment of tweets since we didn't have enough time. However, our original plan was that cluster vectorised tweets using k-means clustering in order to cluster tweets with a higher accuracy. However, due to the time limiit, we could not stick with this plan. If we had used this method, we might have had another result. 
