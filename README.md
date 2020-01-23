# Social-Media-Sentiment-Analysis
Social media data today has become relevant for branding, marketing, and business as a whole. A sentiment analyser learns about various sentiments behind a “content piece”  (could be IM, email, tweet or any other social media post) through machine learning and predicts the same using AI.Twitter data is considered as a definitive entry point for beginners to practice sentiment analysis  machine learning problems. 

1. Install dependencies:
```
pip install tweepy
pip install textblob
```
2. Create an API in twitter https://developer.twitter.com/en/apps/ , only field the name and write any url. This step is important because we need the costumer an access token keys, to conect this algorithm with twitter.

```ruby
import tweepy
from textblob import TextBlob

# Step 1 - Authenticate
consumer_key= 'CONSUMER_KEY_HERE'
consumer_secret= 'CONSUMER_SECRET_HERE'

access_token='ACCESS_TOKEN_HERE'
access_token_secret='ACCESS_TOKEN_SECRET_HERE'

auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)

api = tweepy.API(auth)

#Step 2 - Retrieve Tweets
# In this step we select the key word that we will be search in tweets.
public_tweets = api.search('Australia')

for tweet in public_tweets:
    print(tweet.text)
    analisys = TextBlob(tweet.text)
    print(analisys.sentiment)
```
3. The results shown the polarity of bad or good sentiment between -1 and 1.
America mourns the loss of our three brave firefighters who died battling bush fires in Australia. Our hearts are with their…
Sentiment(polarity=0.8, subjectivity=1.0)

