# The-Beatles Portfolio Project

This is a fun project that assembles data from many sources for all songs from The Beatles. The intent of this project is to demonstrate a portfolio of data science skills without disclosing any proprietary information from former employers. I've organized the project into several sections that fit logically together, though they may not be in chronological order

# Step 1: Extract, Transform and Load Beatles data from many sources using many techniques
## In this step, I demonstrate data acquisition thourh many methods including multiple API types, flat files, web scraping, SQL, Excel and even somd old fashioned data entry for fixing anomolies. 

* Data Source: Python API from Spotify to get a multitude of metadata about every Beatles song 

* Data Source: REST API to get a popularity score for every song Data Source: Web Scraping a table from Wikipedia to get song writers and lead vocalists 

* Data Source: A flat file from Kaggle that contains song lyrics for all songs 

* Data Source: Web Scraping data in a page of text from Billboard to get chart performance for a subset of applicable songs 

* Data Source: Postgres SQL database from musicbrainz.org for more metadata 

* Data Source: Excel spreadsheet with qualitative data from a few individual users

Merge all data sources into one tidy analysis file with one row per song and all important metadata Standardize naming convention Delete unused columns Data Destination: Python Pandas Dataframe and SQL Server DBMS

# Step 2: Simple Data Quality check

Browse the dataframe for context Check for missing values and duplication Check for any constant columns Verify and correct datatypes as needed

# Step 3: Exploratory Data Analysis

Do preliminary univariate analyses and frequency counts 
Gain understanding of distributions 
Check for outliers or other weirdness 
Look at correlations and consider multicollinearity 
Build visualizations to support identified trends using Python libraries (pandas, matplotlib and seaborn) and Tableau - boxplots, histograms, heatmaps, pairplots

# Step 4: Use multiple methods of Natural Language Processing

Implement several different algorithms to understand the emotional valence of each Beatles tune

Use "confentional" Bag of Words approach using VADER (Valence Aware Dictionary and sEntiment Reasoner) lexicon in the Python Natural Language Toolkit package. 

Use Roberta transformer model that was pretrained on very large corpus of Twitter data

Use Transformers Pipeline on Hugging Face to see which algo it recommends for this task and provide valence analysis 

Use distilbertsentiment to look at not only the words but their relatrive positioning to infer meaning

Try out "amanda-cristina/finetuning-sentiment-model-4500-lyrics" which is a pretrained specifically on song lyrics. This was unbelievably simple as it literally asks for what class of model I want and then just an input of each string of song lyrics

Compare different valence values with the valence provided by Spotify and popularity scores Create word clouds based on popularity, valence values, individual user preferences

# Step 5: Unsupervised Learning - K-Means clustering

Create dummy values for songwriter, lead vocalist using one-hot-encoder for label encoding 
Rotate through different values from previous sentiment analysis (completed elsewhere in Step 4 of this workflow)

Scale features to have zero means and unit variance 

Train several iterations of K-Means clustering on song metadata values, with various values of K. 

Use Elbow method to select a good value of K Profile clusters to understand their composition

# Step 6: Supervised Learning - regressions

Perform different regressions on the metadata to determine the most important drivers of popularity, ratings and individual preferences

# Step 7: Provide observations and consider additional possibilities

# Step 8: Add observations from using multiple currently available AI models
