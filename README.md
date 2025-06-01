# 📰 News Headline Market Analysis Toolkit

This project provides a comprehensive exploratory data analysis (EDA) and time series pipeline for analyzing news headlines, focusing on their relationship to financial markets. It includes tools to analyze publication patterns, publisher influence, text statistics, keyword/topic modeling, and more — empowering financial analysts, data scientists, and developers to derive insights from news data.

---

## 📂 Project Structure

```bash
news-sentiment-price-prediction/
├── data/                      # Folder for CSV datasets
├── notebooks/                       # Exploratory Data Analysis tools
│   └── 01_initial_eda.ipynb   # Main EDA class (NewsHeadlineEDA)
├── scripts
├── tests
├── src                 # Jupyter notebooks for experimentation
├── requirements.txt           # Python dependencies
├── main.py                    # Example script to run analysis
└── README.md                  # Project documentation
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/johannesgirmaw/news-sentiment-price-prediction
cd news-sentiment-price-prediction
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate       # On Windows: .venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> Required libraries include `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `spacy`, `gensim`, `nltk`, `numpy`, etc.

---

## How to Use

### 1. Prepare Your Dataset

- The dataset should be a `.csv` file containing at least:
  - `headline`: the text of the news
  - `date`: publication datetime
  - `publisher`: source or author

Example schema:

| headline                        | date                | publisher      |
| ------------------------------- | ------------------- | -------------- |
| FDA approves new cancer drug    | 2024-05-10 14:30:00 | bloomberg.com  |
| Microsoft announces new AI chip | 2024-05-11 10:00:00 | reuters@ai.com |

### 2. Load and Analyze

```python
from eda.news_headline_eda import NewsHeadlineEDA

eda = NewsHeadlineEDA("data/news_headlines.csv")

# Text Stats
eda.show_text_length_stats()

# Publisher Analysis
eda.analyze_publishers_extended()

# Date Trends
eda.analyze_publication_trends()
eda.analyze_publication_times()

# Topic Modeling
eda.perform_topic_modeling(num_topics=5)
```

### 3. Visual Outputs

The EDA module generates multiple visualizations:

- Headline length and word count distributions
- Daily/weekly publication trends
- Heatmaps of monthly frequency
- Top publishers and email domain analysis
- Topic modeling word clouds

---

## Features Implemented

- ✅ Clean and preprocess headline data
- ✅ Textual length statistics and distributions
- ✅ Publisher influence analysis (with email domain tracking)
- ✅ Time-based publication trends (daily, weekly, heatmaps)
- ✅ Topic modeling using NLP techniques (Gensim, spaCy)
- ✅ Interactive plotting with Seaborn and Matplotlib

---

## Example Visuals

> Included visualizations in `/notebooks` and `/outputs` folders.

- 📊 Publication frequency heatmap by year & month
- 📅 Article count by day of the week
- 🔍 Word cloud of top keywords per topic
- 📰 Top 10 publishers by article count

---

## Future Enhancements

- Real-time news ingestion with RSS feeds or APIs
- Sentiment classification pipeline (VADER or transformer models)
- Event detection tied to stock movements
- Integration with financial time series for predictive modeling

---

## Testing

Basic unit tests can be added to a `tests/` directory.

To test:

```bash
pytest tests/
```

## 📄 License

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.
