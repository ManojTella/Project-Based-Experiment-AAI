<H3>ENTER YOUR NAME: Manoj Guna Sundar Tella.</H3>
<H3>ENTER YOUR REGISTER NO: 212221240026.</H3>
<H3>DATE:</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Perform sentiment analysis using your Facebook data and filter the data that has only Positive feedback for the code given in the following link.
### Program:
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

# Filter out rows with positive sentiment (label 'P')
positive_feedback = df[df['Label'] == 'P']

# Output the negative feedback
print(positive_feedback)
  ```
### Output:
Show your execution results here
### Inference:
Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
