**RedditStocks_v2.0**


This repository contains a machine learning pipeline for predicting stock market movements using Reddit sentiment analysis combined with historical stock data.

Setup Instructions
Prerequisites
Anaconda or Miniconda installed

GitHub access to clone this repository

Reddit API credentials (for data scraping)

Environment Setup
Clone the repository:


git clone https://github.com/YOUR-USERNAME/RedditStocks_v2.0.git
cd RedditStocks_v2.0
Create and activate the conda environment:

conda create -n RedditStocksV2 python=3.8
conda activate RedditStocksV2
Install required packages:


conda env update --file environment.yml --prune
Reddit API Setup
Create Reddit API credentials by setting the following:


{
  "client_id": "YOUR_CLIENT_ID",
  "client_secret": "YOUR_CLIENT_SECRET",
  "user_agent": "YOUR_USER_AGENT",
  "username": "YOUR_REDDIT_USERNAME",
  "password": "YOUR_REDDIT_PASSWORD"
}


Usage Workflow
Collect Reddit posts:
Run the redditscraper notebook to gather Reddit posts.

Analyze sentiment:
Run the vaderbert notebook to perform sentiment analysis on the collected posts.

Fetch stock data:
Use the yahoofinance notebook to pull historical stock prices.

Merge datasets:
Combine the sentiment and stock data using the merge notebook.

Run machine learning models:
Train and evaluate models using the merged dataset.

Additional Notes
The code is configured for Apple's Metal Performance Shaders (MPS).
If you have an NVIDIA GPU, modify the device settings from mps to cuda to utilize your GPU.

If no GPU is available, the models will automatically run on the system CPU.

Reddit API rate limits may apply.
You may need to increase sleep timers or limit the amount of data scraped to avoid hitting API limits.
