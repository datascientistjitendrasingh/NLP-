# CODE FOR TEXTBLOB:
from textblob import TextBlob

def detect_sentiment(text):
   
    blob = TextBlob(text)
    
    sentiment = blob.sentiment
    print(sentiment.polarity)

  
    if sentiment.polarity > 0:
        return 'Positive'
    elif sentiment.polarity < 0:
        return 'Negative'
    else:
        return 'Neutral'


text = input("Enter your text: ")
sentiment = detect_sentiment(text)
print(sentiment)
