# The-Beatles
Beatles Portfolio Project

This is a fun project that assembles data from many sources for all songs from The Beatles. The intent of this project is to demonstrate a portfolio of data science skills without disclosing anything proprietary from former employers. I've organized the project into several sections that fit logically together, though they may not be in chronological order

# Step 1: Extract, Transform and Load Beatles data from many sources using many techniques

Data Source: Python API from Spotify to get a multitude of metadata about every Beatles song Data Source: REST API to get a popularity score for every song Data Source: Web Scraping a table from Wikipedia to get song writers and lead vocalists Data Source: A flat file from Kaggle that contains song lyrics for all songs Data Source: Web Scraping data in a page of text from Billboard to get chart performance for a subset of applicable songs Data Source: Postgres SQL database from musicbrainz.org for more metadata Data Source: Excel spreadsheet with qualitative data from a few individual users Merge all data sources into one tidy analysis file with one row per song and all important metadata Standardize naming convention Delete unused columns Data Destination: Python Pandas Dataframe and SQL Server DBMS

# Step 2: Data Quality check

Browse the dataframe for context Check for missing values and duplication Check for any constant columns Verify and correct datatypes as needed

#Step 3: Exploratory Data Analysis

Do preliminary univariate analyses and frequency counts Gain understanding of distributions Check for outliers or other weirdness Look at correlations and consider multicollinearity Build visualizations to support identified trends using Python libraries (pandas, matplotlib and seaborn) and Tableau - boxplots, histograms, heatmaps, pairplots

# Step 4: Use multiple methods of Natural Language Processing

Use VADER (Bag of Words), Roberta and Hugging Face algo to do valence analysis Compare different valence values with the valence provided by Spotify and popularity scores Create word clouds based on popularity, valence values, individual user preferences

# Step 5: Unsupervised Learning - K-Means clustering

Create dummy values for songwriter, lead vocalist and possibly sentiment analysis (completed elsewhere in this workflow) using one-hot-encoder for label encoding Scale features to have zero means and unit variance Train several iterations of K-Means clustering on song metadata values, with various values of K. Use Elbow method to select a good value of K Profile clusters to understand their composition

# Step 6: Supervised Learning - regressions

Perform different regressions on the metadata to determine the most important drivers of popularity, ratings and individual preferences

# Step 7: Provide observations and consider additional possibilities

# Step 8: Add observations from using multiple currently available AI models
