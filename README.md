# 📰 News Headline Market Analysis Toolkit

\*\*# Predicting Price Moves with News Sentiment

## Project Overview

This project, "Predicting Price Moves with News Sentiment," aims to explore and establish correlations between financial news sentiment and stock market movements. Developed as part of the Nova Financial Solutions challenge, it focuses on enhancing predictive analytics capabilities through advanced data analysis, specifically leveraging Natural Language Processing (NLP) and quantitative financial techniques.

The core objectives are:

1. Sentiment Analysis: To quantify the emotional tone of financial news headlines.
2. Correlation Analysis: To establish statistical relationships between news sentiment and corresponding stock price movements.

Ultimately, the insights derived from this analysis will be used to suggest innovative investment strategies.

## Dataset

The project utilizes the Financial News and Stock Price Integration Dataset (FNSPID), a comprehensive dataset combining qualitative news data with quantitative stock information. Key data fields include:

- headline: The title of the news article.
- url: Direct link to the full news article.
- publisher: Author/creator of the article.
- date: Publication date and time (UTC-4 timezone).
- stock: Stock ticker symbol (e.g., AAPL).

## Project Structure and Tasks

The project is structured into three main tasks, each building upon the previous one:

├── .vscode/
│ └── settings.json
├── .github/
│ └── workflows
│ ├── unittests.yml
├── .gitignore
├── requirements.txt
├── README.md
├── src/
│ ├── **init**.py
├── notebooks/
│ ├── **init**.py
│ └── README.md
├── tests/
│ ├── **init**.py
└── scripts/
├── **init**.py
└── README.md

### Task 1: Exploratory Data Analysis (EDA) & Statistical Thinking

This initial phase focuses on understanding the raw data and setting up the development environment.

Key Activities:

- Environment Setup: Configure a reproducible Python data science environment.
- Git & GitHub: Set up a GitHub repository, create branches (task-1), and commit work regularly with descriptive messages.
- Descriptive Statistics: Obtain basic statistics for textual lengths (headline length), count articles per publisher, and analyze publication date trends.
- Text Analysis (Topic Modeling): Identify common keywords/phrases and significant events using NLP.
- Time Series Analysis: Investigate publication frequency variations over time and analyze publishing times.
- Publisher Analysis: Determine most prolific publishers and differences in reporting.

### Task 2: Quantitative Analysis using PyNance and TA-Lib

This phase involves integrating additional financial data and applying quantitative analysis.

Key Activities:

- Branch Management: Merge task-1 into main via Pull Request (PR), then create a new branch task-2.
- Data Preparation: Load stock price data (Open, High, Low, Close, Volume) into pandas DataFrames.
- Technical Indicators: Calculate Moving Averages (MA), Relative Strength Index (RSI), and MACD using TA-Lib.
- Financial Metrics: Utilize PyNance for advanced financial metrics.
- Data Visualization: Create visualizations to understand data and indicator impact on stock prices.

### Task 3: Correlation between News and Stock Movement

The final and most critical task focuses on establishing the direct correlation between news sentiment and stock price changes.

Key Activities:

- Branch Management: Merge task-2 into main via Pull Request (PR), then create a new branch task-3.
- Data Preparation:

  - Date Alignment: Normalize timestamps to align news items with corresponding stock trading days.
  - Sentiment Analysis: Conduct sentiment analysis on news headlines using nltk and TextBlob to assign sentiment scores.
  - Calculate Stock Movements: Compute daily percentage changes in stock closing prices to represent returns.

- Correlation Analysis:

  - Aggregate Sentiments: Compute average daily sentiment scores.
  - Calculate Correlation: Determine the Pearson correlation coefficient between average daily sentiment scores and stock daily returns.

## Technologies Used

- Python: Primary programming language.
- pandas: Data manipulation and analysis.
- nltk: Natural Language Toolkit for text processing.
- TextBlob: Simple API for common NLP tasks, including sentiment analysis.
- TA-Lib: Technical Analysis Library for financial indicators.
- PyNance: Python library for financial analysis.
- Git: Version control system.
- GitHub: Repository hosting and collaboration.

## Setup and Installation

To set up the project locally, follow these steps:

1. Clone the repository:
   git clone https://github.com/johannesgirmaw/news-sentiment-price-prediction/
   cd news-sentiment-price-prediction/
2. Create a virtual environment (recommended):
   python -m venv venv
   source venv/bin/activate # On Windows: `venv\Scripts\activate`
3. Install dependencies:
   pip install -r requirements.txt

   (Note: TA-Lib might require specific installation steps depending on your OS. Refer to the official TA-Lib Python wrapper documentation for details.)

4. Data Acquisition: The FNSPID dataset is assumed to be available. Ensure it is placed in an accessible location, or update the data loading paths in the notebooks/scripts accordingly.

## Usage

- Notebooks: The notebooks/ directory contains Jupyter notebooks for EDA, quantitative analysis, and correlation analysis. You can run these interactively.
- Scripts: The src/ and scripts/ directories will contain modularized Python code for data processing, sentiment analysis, and correlation calculations.

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature (git checkout -b feature/your-feature-name).
3. Commit your changes following [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
4. Push to your branch (git push origin feature/your-feature-name).
5. Open a Pull Request to the main branch.

## License

This project is licensed under the [MIT License](http://docs.google.com/LICENSE.md).
