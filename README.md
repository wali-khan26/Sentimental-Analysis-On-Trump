# Sentimental-Analysis-On-Trump
Trump Sentiment Analysis
# Overview
This project focuses on performing sentiment analysis on Reddit posts related to Donald Trump.
It collects data using the Reddit API via the asyncpraw library, processes and cleans the text data, and then applies sentiment analysis techniques using TextBlob and VADER.
The final processed dataset is exported for use in Tableau to create interactive sentiment dashboards.

# Objectives
Retrieve Reddit posts related to Donald Trump from multiple subreddits.

Preprocess and clean the collected data to ensure high-quality text input for sentiment analysis.

Perform sentiment analysis using:

TextBlob for polarity-based classification.

VADER for compound sentiment scoring.

Export the processed data for visualization in Tableau.

Provide visual insights into public sentiment trends.

# Data Source
Platform: Reddit

API Wrapper: asyncpraw (Asynchronous Reddit API Wrapper)

Keywords Used:

Trump

Trump election

Trump covid

Trump 2020

Donald Trump

Subreddits Searched:

politics

worldnews

news

conservative

democrats

# Project Workflow
# 1. Data Collection

Uses asyncpraw for asynchronous data retrieval to improve performance.

Retrieves up to 500 posts per keyword-submission combination.

Extracted fields include:

Post title and body text (combined)

Timestamp

Username

Subreddit name

Score

Number of comments

URL

# 2. Data Cleaning
The dataset undergoes extensive cleaning steps:

Removal of:

Emojis

URLs and domain names

Special characters and numbers

Duplicate entries

Posts starting with "RT" (retweets or re-shares)

Conversion of text to lowercase.

Normalization of whitespace.

Splitting of long posts into separate lines for finer sentiment granularity.

Sampling (optional) to limit dataset size for processing efficiency.

# 3. Sentiment Analysis
Two sentiment analysis approaches are applied:

a. TextBlob

Calculates polarity score for each text:

Positive sentiment if polarity > 0

Negative sentiment if polarity < 0

Neutral sentiment if polarity = 0

b. VADER (Valence Aware Dictionary and sEntiment Reasoner)

Calculates four sentiment scores:

Positive

Negative

Neutral

Compound (overall score)

Classifies sentiment based on compound score:

Positive if > 0

Negative if < 0

Neutral if = 0

# 4. Data Visualization
Visualizes sentiment distribution using Seaborn and Matplotlib.

Prepares cleaned and labeled dataset for Tableau.

Possible dashboard features:

Sentiment distribution bar charts.

Time series trends of sentiment.

Subreddit-level sentiment comparison.

5. Exporting Results
f.csv: Intermediate cleaned dataset.

final_trump_compressed.csv: Final processed dataset with sentiment labels.

