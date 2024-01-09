# CODE FOR TEXTBLOB:
from textblob import TextBlob

def detect_sentiment(text):
    # Create a TextBlob object
    blob = TextBlob(text)
    # Obtain the sentiment of the text
    sentiment = blob.sentiment
    print(sentiment.polarity)

    # polarity is a float within the range [-1.0, 1.0]
    # subjectivity is a float within the range [0.0, 1.0] where 0.0 is very objective and 1.0 is very subjective
    if sentiment.polarity > 0:
        return 'Positive'
    elif sentiment.polarity < 0:
        return 'Negative'
    else:
        return 'Neutral'

# Test the function
text = input("Enter your text: ")
sentiment = detect_sentiment(text)
print(sentiment)
