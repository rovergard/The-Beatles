# The-Beatles Portfolio Project

This is a fun project that assembles data from many sources for all songs from The Beatles. The intent of this project is to demonstrate a portfolio of data science skills without disclosing any proprietary information from former employers. I've organized the project into several sections that fit logically together, though they may not be in chronological order. These are outlined below. This project is still in-progress, so there are chunks I have yet to build.

# Step 1: Extract, Transform and Load Beatles data from many sources using many techniques
## In this step, I demonstrate data acquisition through many methods including multiple API types, flat files, web scraping, SQL, Excel and even some old fashioned data entry for fixing anomalies and manual business rules.

* Data Source: Python API from Spotify to get a multitude of metadata about every Beatles song 
* Data Source: REST API to get a popularity score for every song
* Data Source: Web Scraping a table from Wikipedia to get song writers and lead vocalists 
* Data Source: A flat file from Kaggle that contains song lyrics for all songs 
* Data Source: Web Scraping data in a page of text from Billboard to get chart performance for a subset of applicable songs 
* Data Source: Postgres SQL database from musicbrainz.org for more metadata 
* Data Source: Excel spreadsheet with qualitative data from a few friends and family. If this were a real marketing research project, 
Merge all data sources into one tidy analysis file with one row per song and all important metadata Standardize naming convention Delete unused columns Data Destination: Python Pandas Dataframe and SQL Server DBMS

# Step 2: Simple Data Quality check

Browse the dataframe for correctness and completeness. Check for missing and duplicate values. Verify correct datatypes. Fix weirdness 

# Step 3: Preliminary Exploratory Data Analysis

* Do preliminary univariate analyses and frequency counts 
* Gain understanding of distributions 
* Check for outliers or other weirdness 
* Look at correlations and consider multicollinearity 
* Build visualizations to support identified trends using Python libraries (pandas, matplotlib and seaborn) and Tableau - boxplots, histograms, heatmaps, pairplots

# Step 4: Use multiple methods of Natural Language Processing

Implement several different algorithms to understand the emotional valence of each Beatles tune
* Use "conventional" Bag of Words approach using **VADER** (Valence Aware Dictionary and sEntiment Reasoner) lexicon in the Python Natural Language Toolkit package. 
* Use **Roberta transformer model** that was pretrained on very large corpus of Twitter data
* Use **Transformers Pipeline on Hugging Face** to see which algo it recommends for this task and provide valence analysis. This was unbelievably simple as it literally asks for what class of model I want (sentiment analysis) and then an input of each string of song's lyrics. This is basically AI writing AI. 
* Use **distilbertsentiment** to look at not only the words but their relatrive positioning to infer greater meaning
* Try out **"amanda-cristina/finetuning-sentiment-model-4500-lyrics"** which is pretrained specifically on song lyrics. 
* Compare different valence values with the valence provided by Spotify and popularity scores 
* Create word clouds based on popularity, valence values, individual user preferences

# Step 4A - Use OpenAI API apply several different LLMs (Large Language Models) to summarize lyrics and provide emotional valance from lyrics alone.
This opens up a much wider line of inquiry to see how well each model captures not only the literal explanation of the lyrics but it also attempts to infer deeper poetic meaning intended by the songwriter. GPT-4 is radically better than the previous LLMs from OpenAI. 


# Step 5: Unsupervised Learning - K-Means clustering

Analyze quantitative data about each song and group songs into **clusters** that are similar to each other and also different from members of other clusters

* Create dummy values using **One-Hot_Encoder** for songwriter, lead vocalist, Era (grouping of release years), song key, Billboard and Rolling Stone ratings, time signature. 
* Rotate through different values from previous sentiment analysis (completed elsewhere in Step 4 of this workflow)
* Scale features to have zero means and unit variance 
* Train several iterations of K-Means clustering on song metadata values, with various values of K. 
* Use Elbow method to select a good value of K Profile clusters to understand their composition
* Profile characteristics and song membership in each cluster. Interpret profiles and provide meaningful names for all clusters

# Step 6: Supervised Learning - regressions

* Perform different linear regressions on the metadata to determine the most important drivers of popularity, ratings and individual preferences

# Step 7: Supervised Learning - classification models such as:
* Logistic Decision Trees
* Random Forests
* SVMs

# Step 8: Provide observations and consider additional possibilities

# Step 9: More Exploration of additional currently available AI models and methods to see what's new.
* Langchain and AutoGPT
* Code Interpreter

