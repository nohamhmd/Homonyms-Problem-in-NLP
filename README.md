# Homonyms-Problem-in-NLP
# Homonyms in Sentiment Analysis

## Project Overview
This project explores the challenges posed by homonyms in Natural Language Processing (NLP) tasks, particularly in sentiment analysis. It evaluates different datasets and models to determine how well they handle contextual ambiguities associated with homonyms.

## Problem Definition
Homonyms are words that share the same spelling and pronunciation but have different meanings. This can complicate various NLP tasks, including part-of-speech tagging, word sense disambiguation (WSD), and sentiment analysis. The goal of this project is to assess how well different models can disambiguate homonyms in sentiment analysis.
![image](https://github.com/user-attachments/assets/2993ded5-2422-4e1e-9b0d-5083f34e6023)

## Dataset Selection
Two datasets were considered: the Stanford Sentiment Treebank (SST) and the IMDb dataset. The IMDb dataset was chosen due to its richness in context and higher occurrences of homonyms, making it more suitable for this project.

- **Data Size**: 50,000 records (25,000 positive reviews and 25,000 negative reviews).
- **Balanced Classes**: The dataset is perfectly balanced between positive and negative sentiments.

## Exploratory Data Analysis (EDA)
- Word clouds were generated for all reviews and for positive and negative reviews separately.
- It was observed that positive reviews tend to be longer than negative ones.
- The distribution of the number of words indicates a majority of short reviews.

## Methodology
### Preprocessing
Two cleaning methodologies were implemented:
1. **Comprehensive Cleaning**:
   - Lowercasing
   - Expand contractions
   - Remove punctuation and emojis
   - Remove stop words, URLs, and HTML tags
   - Remove extra white spaces
2. **Minimal Cleaning**:
   - Remove URLs and HTML tags
   - Remove extra white spaces

### Machine Learning Baseline
Logistic Regression was used as a baseline model:
- **Experiment 1**: Utilized TF-IDF for feature extraction.
- **Experiment 2**: Minor adjustment to ignore numbers in TF-IDF.

### Transformer Models
Evaluation was performed using BERT and RoBERTa:
- **BERT**: Tested with varying sequence lengths and cleaning methods.
- **RoBERTa**: Used with minimal cleaning and a maximum length of 512 tokens.

## Results
- **Best Model**: RoBERTa (max length = 512, minimal cleaning) achieved a validation accuracy of 95.53%.
- Comparison with state-of-the-art benchmarks indicates robust performance.

## Tools Used
- **Programming Language**: Python
- **Libraries**: 
  - Transformers (Hugging Face)
  - Scikit-learn
  - Pandas
  - NumPy
  - Matplotlib and Seaborn
- **Hardware**: GPU for accelerated model training
