# Public Sentiment of Enterprise Artificial Intelligence

This project analyzes public sentiment around enterprise artificial intelligence using Reddit and NewsAPI data.

It combines natural language processing, keyword-based risk indicators, weekly trend analysis, and a forecasting experiment to explore public AI sentiment and risk signals across major AI companies.

## What the project does

- Collects AI-related public discussion from Reddit using PRAW.
- Collects AI-related news articles using NewsAPI.
- Cleans and preprocesses text for analysis.
- Matches records to companies or AI-related topics.
- Applies VADER sentiment scoring.
- Labels risk-related discussion using keyword-based risk indicators.
- Uses TF-IDF and other text-derived features in the analysis workflow.
- Aggregates records into weekly company-level sentiment trends.
- Compares a historical mean baseline with a feedforward neural network forecasting experiment.
- Provides a Streamlit dashboard for exploring sentiment, discussion volume, weekly trends, recent records, and forecast results.

## Data sources

- Reddit comments collected with PRAW
- News articles collected with NewsAPI

The dashboard uses the existing CSV exports in `data/` and does not require API credentials to run.

## Dashboard

Run the Streamlit dashboard:

```bash
streamlit run app.py
```

The dashboard reads from the existing CSV files:

- `data/powerbi_record_level_export.csv`
- `data/powerbi_weekly_trend_export.csv`
- `data/powerbi_company_topic_summary.csv`
- `data/powerbi_prediction_results.csv`
- `data/prediction_results_actual_vs_feedforward_nn.csv`

## Notebook

The original analysis notebook is:

```text
AI_Risk_Project.ipynb
```

The notebook contains the data collection, preprocessing, sentiment scoring, company/topic matching, risk keyword labeling, weekly feature generation, and forecasting experiment.

## Forecasting experiment

The forecasting portion compares:

- Historical mean baseline
- Feedforward neural network

The model comparison is an experiment using weekly sentiment features. The historical mean baseline is included so the neural network results can be interpreted against a simple reference point.

## Technologies used

- Python
- Pandas
- NumPy
- PRAW
- NewsAPI
- NLTK / VADER sentiment
- Scikit-learn
- TensorFlow / Keras
- Streamlit
- Plotly

## Setup

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the dashboard:

```bash
streamlit run app.py
```

To rerun the notebook collection workflow, provide your own Reddit and NewsAPI credentials in your environment or notebook runtime. Do not commit API keys or secrets.
