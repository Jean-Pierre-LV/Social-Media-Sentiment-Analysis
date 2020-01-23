# Social-Media-Sentiment-Analysis
Social media data today has become relevant for branding, marketing, and business as a whole. A sentiment analyser learns about various sentiments behind a “content piece”  (could be IM, email, tweet or any other social media post) through machine learning and predicts the same using AI.Twitter data is considered as a definitive entry point for beginners to practice sentiment analysis  machine learning problems. 

```ruby
import tweepy
from textblob import TextBlob
consumer_key = 'VFAR0XP5VmFVwSVqlu547zINS'
consumer_secret = 'sEdHaupgBmJc1pDkZhEN1BmzYMj7vkI6v0t81CRnmnqFXNAo5h'

access_token = '320474822-37hWN652IVzN25nYNtp1grn3Fas3moqZGNmskrht'
access_token_secret = 'zBqtKcM7AREWevvDYcPLeGNyLecObjZmvQBOQBOEY8YP0'

auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)

api = tweepy.API(auth)
public_tweets = api.search('Australia')

for tweet in public_tweets:
    print(tweet.text)
    analisys = TextBlob(tweet.text)
    print(analisys.sentiment)
```
