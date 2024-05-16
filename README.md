<H3>ENTER YOUR NAME : SHOBIKA P</H3>
<H3>ENTER YOUR REGISTER NO : 212221230096</H3>
<H3>DATE: 14/05/2024</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Perform sentiment analysis using your Facebook data and filter the data that has only neutral feedback for the code given in the following link.
<H3>Program:</H3>
    
 ```
    
import pandas as pd
from textblob import TextBlob

# Load your Facebook data from CSV into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Filter the DataFrame to include only rows with neutral sentiment
neutral_feedback = df[df['Sentiment'] == 0]  # Sentiment polarity of 0 indicates neutral sentiment
```

<H3>Output:</H3>

![Screenshot 2024-05-14 230936](https://github.com/Dhanashreemullaithasan/Project-Based-Experiment-AAI/assets/94165415/13f69a29-d296-4ded-827b-4f769a5f73ba)

![Screenshot 2024-05-14 230950](https://github.com/Dhanashreemullaithasan/Project-Based-Experiment-AAI/assets/94165415/08261ce8-f044-4385-b320-172fcb1c5a83)

<H3>Inference:</H3>
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only neutral feedback for the code is done.
