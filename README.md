# Reddit-BERT-TopicModeling
NLP project using BERT and BERTopic to analyze 8M+ Reddit comments on the Israel-Hamas conflict. Identifies and classifies ~198K controversial comments into Pro/Anti-Israel and Pro/Anti-Hamas categories using topic modeling and BERT-based real-time classification.

📊 Dataset
This project analyzes Reddit discussions related to the Israel-Hamas conflict, collected between August and November 2023. The dataset includes:

8M+ Reddit comments scraped from public subreddits

100+ subreddits in total, including:

Conflict-centric: r/IsraelPalestine, r/IsraelHamasWar, etc.

Conflict-inclusive: r/worldnews, r/news, r/politics, etc.

Extracted 198,000+ controversial comments based on Reddit’s controversiality flag

🧾 Fields Collected:
body: Comment text

created_utc: Timestamp (converted from UNIX to human-readable)

subreddit: Name of the subreddit

ups / downs: Upvotes and downvotes

controversiality: Indicator if the comment is marked as controversial

🔍 Data Preprocessing Steps:
Chunked comment loading for memory efficiency

Controversial comment filtering

Timestamp normalization

Custom keyword scoring and labeling

Due to privacy and platform security concerns, raw Reddit comments are not included in this repository. Only preprocessed metadata and structural information are shared to demonstrate the methodology. Users are encouraged to collect fresh data using the Reddit API or Pushshift for replication.

## Tech Stack
- Python, Jupyter, Hugging Face Transformers
- BERTopic, Scikit-learn, Pandas, NumPy
- Reddit API (data sourced)

## Structure
- `notebooks/` – Data prep, modeling, classification logic
- `data/` – Keyword filters, category mappings
- `models/` – Serialized models
