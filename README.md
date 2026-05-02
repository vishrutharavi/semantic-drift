# Semantic Drift

This project studies semantic drift, i.e., how the meaning and usage of words evolve over time, particularly in online communities.

Using contextual embeddings from transformer models, the system analyzes Reddit discussions across multiple subreddits and compares them with historical news data to detect when and how word meanings shift. Instead of analyzing all words, the pipeline first performs candidate word selection to identify the most relevant words likely to exhibit semantic change. For each selected word, contextual usages are extracted, converted into embeddings, and clustered to identify distinct meanings. These meanings are then compared across time to quantify semantic drift.

In addition to quantitative analysis, the system integrates a Large Language Model (LLM) to generate human-readable explanations of semantic change. While drift detection is performed using embedding-based similarity measures, the LLM is used only as an interpretation layer, improving the understandability of results without affecting robustness.

## Project Goal

Language on the internet evolves rapidly. Words like:

- cloud
- viral
- tablet
- mouse
- stream

often develop new meanings over time.

The goal of this project is to:

- Detect emerging meanings of words
- Track how meanings change over time
- Automatically identify candidate words likely to exhibit semantic drift
- Analyze semantic usage patterns in Reddit communities
- Measure semantic drift using contextual embeddings
- Generate human-readable explanations of semantic changes using LLMs
  
## Pipeline Overview

```
Raw Text Data (News + Reddit)
     ↓
Preprocessing & Cleaning
     ↓
Candidate Word Selection (Top-N words)
     ↓
Context Extraction (Old vs New)
     ↓
Sentence Embeddings (MiniLM)
     ↓
Clustering (K-Means)
     ↓
Early vs Late Meaning Comparison
     ↓
Drift Score Computation (Cosine Similarity)
     ↓
Filtering & Quality Control
     ↓
Semantic Drift Classification
     ↓
LLM-Based Explanation 

```

## Repository Structure

```
├── 01_news_preprocessing.ipynb
│   News dataset preprocessing
│
├── 02A_reddit_processing.ipynb
│   Reddit data cleaning and context extraction
│
├── 02B_reddit_processing.ipynb
│   Additional Reddit filtering and refinement
│
├── 03_two_meaning_classifier.ipynb
│   Sentence embeddings and clustering (K-Means)
│
├── 04_prototype_semantic_drift.ipynb
│   Drift detection experiments
│
├── 05_pipeline_analysis.ipynb
│   End-to-end semantic drift analysis
│
├── 06_candidate_words.ipynb
│   Candidate word selection and ranking
│
├── 07_context_extraction_and_drift_calculation.ipynb
│   Context extraction and drift score computation
│
├── 08_LLM_and_visualization.ipynb
│   LLM explanations and visualization
│
└── README.md

```

## Raw and Preprocessed dataset Google Drive Link

https://drive.google.com/drive/folders/1XJFM7M7VP6Gat6uU3pICbGzCpKtttkcK?usp=sharing

## Key Features

- Multi-source analysis (News + Reddit)
- Context-based semantic modeling
- Scalable pipeline for multiple words
- Visualization of semantic clusters
- LLM-based interpretation layer

