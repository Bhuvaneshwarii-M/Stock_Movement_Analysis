Reddit Stock Sentiment Analysis and Stock Prediction
This project aims to analyze Reddit posts related to stocks, extract sentiment data, match the posts with historical stock prices, and predict potential stock movements based on social media sentiment and stock price trends.

Project Objectives::
Extract Reddit posts from relevant subreddits like r/stocks to gather public sentiment on specific stock symbols.
Perform sentiment analysis on Reddit posts to classify them as positive, negative, or neutral.
Correlate Reddit sentiment with stock data by matching the dates, times, and stock symbols.
Analyze stock price changes and predict trends based on sentiment and historical stock price movements.

Technologies and Tools Used::
      Python: For data extraction, sentiment analysis, and stock price fetching.
Libraries:
      PRAW: To interact with Reddit's API and fetch posts.
      TextBlob: For performing sentiment analysis.
      yfinance: For fetching historical stock price data.
      re: For regex-based text processing.
      datetime: For handling date and time operations.
      math: To handle numerical validations (e.g., NaN checks).
      JSON: To save the extracted and processed data.

Key Steps in the Project::
1. Reddit Data Extraction
      Connected to Reddit API using PRAW with necessary credentials.
      Fetched posts from r/stocks and filtered them based on stock symbols of interest (e.g., TSLA, AAPL).
      Extracted key details from posts, including:
      Title and content
      Date and time
      Sentiment of the post
      Number of mentions of the stock symbol
2. Sentiment Analysis
      Used TextBlob to determine the sentiment polarity of each post:
      Positive: Polarity > 0
      Negative: Polarity < 0
      Neutral: Polarity = 0
      Stored the sentiment score and categorized each post accordingly.
3. Stock Data Extraction
      Used yfinance to fetch historical stock prices for the last five years for the selected stock symbols.
      Matched stock price data with Reddit post dates to find:
      Closing price on the day of the post
      Percentage change in stock price
4. Data Matching and Processing
      Mapped Reddit posts with corresponding stock prices using:
      Nearest matching date to the post timestamp
      Regex-based extraction for prices and changes mentioned in the text
5. Data Storage
      Saved the processed data in a structured JSON format (reddit_stock_data_final.json) for further analysis.
      Challenges Faced
      Handling API Rate Limits: Ensured efficient use of the Reddit API to fetch data without hitting rate limits.
      Data Gaps in Stock Prices: Handled cases where stock data for specific dates was unavailable or mismatched.
      Sentiment Analysis Accuracy: Improved sentiment analysis by combining title and content for better context.
