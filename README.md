# Wednesdays Off — The Unpopular Opinion That Wasn’t?

> A lighthearted NLP project exploring Reddit’s sentiment about taking Wednesdays off. Because who says weekends should only hug Fridays?

---

## Project Overview

Redditors love strong opinions, and one thread on [r/unpopularopinion](https://www.reddit.com/r/unpopularopinion) sparked a curious debate:  
**Should we adopt a 4-day work week where Wednesday is the day off?**

Using over **1100 comments** scraped via Reddit’s API, this project:
- Cleans and tokenizes Reddit comment text
- Handles tricky language like **negation** (e.g., *"not bad"*)
- Applies **VADER** sentiment scoring
- Visualizes trends with **word clouds** and **score distributions**

The goal? To see how online voices *really* feel about a midweek pause and whether Wednesday deserves its moment.

---

## Project Structure

```
wednesday-off-sentiment/
│
├── wednesday_offs_sentiment.ipynb # Main NLP and sentiment notebook
├── reddit_work_week.ipynb # Reddit API scraping notebook (via PRAW)
├── /data/
│ └── work_week.csv # Raw comment data (scraped)
└── README.md # You’re here
```

---

## Dataset Details

The dataset was collected via Reddit’s API using `PRAW`. It includes **1127 comments** from a single post and contains:

- `comment_id`, `parent_id`: Reddit threading info  
- `author`: Reddit username (anonymized)  
- `score`: upvotes received  
- `body`: full comment text  
- `created_utc`, `depth`, `permalink`: metadata

> *Note: All data was collected from a public subreddit using Reddit’s API. No private or sensitive user data was accessed.*

---

## Features

- Full NLP pipeline: cleaning, tokenizing, stopword removal
- **Negation-aware sentiment processing**
- Sentiment scoring with **VADER**
- Word clouds and violin plots by sentiment/score
- Transparent Reddit scraping notebook included

---

## 💡 Highlights & Findings

- Most top-voted comments were **positive or neutral**, suggesting support for the idea.
- Frequent themes: mental health, burnout, productivity, and better pacing of the week.
- “Midweek reset” emerged as a surprisingly valid concept!

---

## Tech Stack

- Python (NLTK, Pandas, Matplotlib, WordCloud)
- VADER Sentiment Analyzer
- Jupyter Notebook
- Reddit API (PRAW)

---

## Future Improvements

- Compare this with other "work week" debates (e.g., Friday off vs Monday off)
- Train a classifier using manually labeled sentiment
- Analyze comment engagement by thread depth

---

## License & Use

MIT License — open for educational use and adaptation.  
Please respect Reddit's [API terms](https://www.reddit.com/dev/api/) if extending this work.

---
