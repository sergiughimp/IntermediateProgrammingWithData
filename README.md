# AE1 Vishing Data Analysis

## Overview
This project analyzes public conversations on Twitter about voice phishing (vishing) and scam calls from January 2019 to October 2022. The dataset contains tweets in multiple languages, but the analysis focuses on English tweets to understand trends, user behaviors, and public sentiment.

## Steps

### 1. Data Loading & Preprocessing
- Loaded dataset from a zipped CSV file.
- Preprocessed text by:
  - Converting to lowercase
  - Removing special characters and digits
  - Removing redundant whitespace
  - Tokenizing into words
  - Filtering out meaningless words (1 character or less)
- Stored cleaned text in a new column `processed_text`.

### 2. Text Analysis
- **Word frequency analysis** to identify the most common words.
- Calculated **vocabulary richness** (unique words / total words).
- Identified **common words among top users**.
- Found top 10 frequent words: `'call'`, `'to'`, `'scam'`, `'rt'`, `'the'`, `'you'`, `'and'`, `'is'`, `'of'`, `'for'`.

### 3. Data Visualization
- **Word clouds** for the top 10 users to highlight frequent terms.
- **Sentiment analysis** using TextBlob:
  - Computed polarity scores for tweets
  - Visualized average sentiment over time
- **N-gram analysis** (1-grams to 4-grams) to identify common phrases.
- Visualized top n-grams using bar charts.

### 4. Key Findings
- Frequent terms reveal focus on scam calls and warnings.
- Sentiment fluctuates over time, indicating awareness and concern.
- Common phrases (bigrams, trigrams, quadgrams) show recurring themes like `"scam call"` and `"closure is scam dont"`.

### 5. Lessons Learned
- Preprocessing with lists and handling nested text was essential for accurate analysis.
- Safe date conversion using `.loc` avoids errors.
- Flattening text lists enabled comprehensive n-gram and word frequency analysis.
- Project improved skills in text cleaning, sentiment analysis, visualization, and structured data handling.

## Tools & Libraries
- Python, Pandas, Matplotlib, WordCloud, TextBlob, collections.Counter



# AE2 Mastodon Moderation Network Analysis

## Overview
This project analyzes moderation activities on Mastodon, focusing on blocking reasons such as misinformation, spam, harassment, and hate speech. Using network analysis and cosine similarity, the project explores patterns of moderation across different instances and communities.

## Key Steps
1. **Data Loading & Cleaning**
   - Loaded CSV dataset of moderation actions.
   - Standardized blocking reasons and removed missing values.
2. **Significant Moderation Filtering**
   - Focused on major issues: misinformation, spam, harassment, hate speech.
3. **Network Construction**
   - Built a weighted network graph of users.
   - Used cosine similarity to measure similarity in moderation behavior.
4. **Community Detection**
   - Applied the Louvain method to identify groups of instances with similar moderation patterns.
5. **Visualization**
   - Visualized the network and detected communities with color-coded layouts.
   - Explored temporal trends and centrality measures for deeper insights.

## Key Findings
- **Misinformation & Spam** are the most common moderation reasons across instances.
- **Harassment & Hate Speech** are more targeted, appearing in specific communities.
- Communities reveal both widespread moderation patterns and niche behaviors.
- Certain nodes are central in bridging communities, influencing moderation dynamics.

## Lessons Learned
- Preprocessing and filtering are crucial for meaningful network analysis.
- Louvain method effectively detects communities, but interpretation requires context.
- Visualization clarity is essential for large, complex networks.
- Scalability and interactive visualizations are areas for future improvement.

## Tools & Libraries
Python, Pandas, NumPy, NetworkX, Matplotlib, Cosine Similarity, Louvain Method



# AE3 IMDb Top 1000 Movies Analysis

## Project Overview
This project analyzes the top 1000 movies on IMDb to uncover patterns and trends that influence movie popularity and success. By exploring features such as ratings, genres, runtime, release year, and gross earnings, the project aims to provide insights for data analysts, film professionals, and movie enthusiasts.

## Data Source
The dataset contains information about the top 1000 movies on IMDb, including:
- Title, Release Year, Certificate  
- Runtime, Genre  
- IMDB Rating, Meta Score  
- Director, Number of Votes, Gross Earnings  

## Key Steps

### 1. Data Preparation
- Removed unnecessary columns (Poster_Link, Star1–4).  
- Converted runtime and gross to numeric formats.  
- Handled missing values and removed duplicates.  
- Renamed columns for clarity.

### 2. Exploratory Data Analysis (EDA)
- Visualized distributions of IMDB ratings, gross earnings, and number of votes.  
- Generated summary statistics to identify trends and outliers.

### 3. K-Nearest Neighbors (K-NN) Classification
- Created a binary target (`high_rating`) based on IMDB ratings (>8).  
- Trained a K-NN classifier using features: Runtime, Meta_score, No_of_Votes, and Gross.  
- Evaluated performance with accuracy metrics and confusion matrix.  

### 4. K-Means and HDBSCAN Clustering
- Standardized features and applied K-Means (k=3) and HDBSCAN for clustering movies.  
- Visualized clusters to identify patterns in runtime, ratings, and meta scores.  
- Determined optimal k for K-Means using silhouette analysis.  

## Key Findings
- Movies with higher Meta_score, runtime, votes, and gross tend to have higher ratings.  
- Clustering reveals groups of movies with similar characteristics, highlighting patterns in runtime and ratings.  
- K-NN model achieved an accuracy of ~70%, indicating a reasonable prediction ability based on selected features.

## Tools & Libraries
- Python, Pandas, NumPy  
- Matplotlib, Seaborn for visualization  
- scikit-learn for K-NN and K-Means  
- HDBSCAN for density-based clustering  

## Conclusion
This analysis provides insights into what makes movies popular on IMDb, identifies patterns in ratings and earnings, and demonstrates classification and clustering techniques for understanding movie data.





