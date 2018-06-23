# twittermining


import tweepy
from tweepy import OAuthHandler
 
consumer_key = '	lVMbGpmYQ0edf8AXFyO1LxLYI'
consumer_secret = 'CWWuc8mNjgzwCxcJlaZXNjvqYIjHD7u3BmpA6VotWYUmzUJW4j'
access_token = '703599895-NYyHMjTMlfGxQs58CFuSBG6HsOswPNfbtAcN9ZSd'
access_secret = '	23jdmUmSL2kbh2P5jW26chEtQBYcWWzZj2oPA1c60avgu'
 
auth = OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_secret)
 
api = tweepy.API(auth)

for status in tweepy.Cursor(api.home_timeline).items(10):

    print(status.text)
