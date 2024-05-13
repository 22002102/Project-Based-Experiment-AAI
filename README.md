<H3>NAME : SANJAY S</H3>
<H3>REG NO : 212222230132</H3>
<H3>DATE : 13/05/2024</H3>
<H1 Align="center">Project Based Experiment<H1>
  
### Objective:
  Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.
<H3>Program:</H3>

```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)

```

<H3>Output:</H3>

![image](https://github.com/Lavanyajoyce/Project-Based-Experiment-AAI/assets/119091638/a4b530c4-369e-4a1b-b227-3b8c26cd54d1)

![image](https://github.com/Lavanyajoyce/Project-Based-Experiment-AAI/assets/119091638/ea2f04d9-75d9-43c0-a567-3c4f59e53d5d)

<H3>Inference:</H3>
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done.
