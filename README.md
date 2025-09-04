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
