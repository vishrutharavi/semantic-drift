# Semantic Drift

- This project studies semantic drift, how the meaning and usage of words evolve over time in online communities.

- Using contextual embeddings from transformer models, we analyze Reddit discussions across multiple subreddits and detect when and how words shift in meaning.

- The system builds embeddings for contextual usages of words, clusters them to identify meanings, and compares earlier vs later periods to measure semantic change.

- This work demonstrates how modern embedding models can be used to analyze language evolution in large-scale social media data.

## Project Goal

Language on the internet evolves rapidly. Words like:

- cloud
- viral
- tablet
- mouse
- stream

often develop new meanings over time.

The goal of this project is to:

- detect emerging meanings of words
- track how meanings change over time
- analyze semantic usage patterns in Reddit communities
- measure semantic drift using contextual embeddings

## Pipeline Overview

```
Raw Text Data
     ↓
Preprocessing
     ↓
Context Extraction
     ↓
Sentence Embeddings (MiniLM)
     ↓
Clustering (K-Means)
     ↓
Early vs Late Meaning Comparison
     ↓
Semantic Drift Detection

```

## Repository Structure

```

├── 01_news_preprocessing.ipynb
│   News dataset preprocessing
│
├── 02A_reddit_processing.ipynb
│   Reddit context extraction
│
├── 02B_reddit_processing.ipynb
│   Additional Reddit filtering and processing
│
├── 03_two_meaning_classifier.ipynb
│   Sentence embedding generation and clustering
│
├── 04_prototype_semantic_drift.ipynb
│   Drift detection experiments
│
├── 05_pipeline_analysis.ipynb
│   End-to-end semantic drift analysis
│
└── README.md

```

## Raw and Preprocessed dataset Google Drive Link

https://drive.google.com/drive/folders/1XJFM7M7VP6Gat6uU3pICbGzCpKtttkcK?usp=sharing


