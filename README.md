<H3>ENTER YOUR NAME</H3>
<H3>ENTER YOUR REGISTER NO.</H3>
<H3>DATE:</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Perform sentiment analysis using your Facebook data and count the number of Occurrences of Krishna in the extracted text for the code given in the following link
<H3>Program:</H3>
Insert your code here
import pandas as pd
from textblob import TextBlob

# Read data from Excel file
data = pd.read_csv("fb_sentiment.csv")  # Replace "facebook_data.xlsx" with your file path

# Given name to count occurrences
given_name = "Krishna"

# Initialize counters for sentiment analysis and name occurrences
sentiment_counts = {'positive': 0, 'negative': 0, 'neutral': 0}
name_occurrences = 0

# Perform sentiment analysis and count occurrences of the given name
for index, row in data.iterrows():
    # Perform sentiment analysis
    blob = TextBlob(row['FBPost'])
    polarity = blob.sentiment.polarity
    if polarity > 0:
        sentiment_counts['positive'] += 1
    elif polarity < 0:
        sentiment_counts['negative'] += 1
    else:
        sentiment_counts['neutral'] += 1

    # Count occurrences of the given name
    name_occurrences += row['FBPost'].lower().count(given_name.lower())

# Print sentiment analysis results
print("Sentiment Analysis Results:")


# Print occurrences of the given name
print(f"Occurrences of '{given_name}': {name_occurrences}")
# Print occurrences of the given name
print(f"Occurrences of '{given_name}': {name_occurrences}")
<H3>Output:</H3>
![Screenshot (97)](https://github.com/Shobika187/Project-Based-Experiment-AAI/assets/94508142/a63c2898-f196-4271-9dac-d51a6e18431e)
![Screenshot (96)](https://github.com/Shobika187/Project-Based-Experiment-AAI/assets/94508142/481a9e13-2822-4bc4-a5a2-d25f07c8fafd)

Perform sentiment analysis using your Facebook data and count the number of Occurrences of Krishna in the extracted text for the code given in the following link
<H3>Inference:</H3>
Write about your learning experience out of this project. (What you have learned)
