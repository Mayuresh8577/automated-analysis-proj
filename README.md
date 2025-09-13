📊 Automated Data Analysis with LLMs
🔹 Overview
This project implements an automated analysis pipeline using Python and a Large Language Model (GPT-4o-Mini via AI Proxy).
The script autolysis.py takes any CSV file as input and produces:
A story-driven analysis (README.md)
1–3 visualizations (*.png)
Insights and implications derived from the dataset
The goal is to combine classical data analysis with LLM-powered narration for flexible, dataset-agnostic insights.

🔹 Features
Generic analysis applicable to any dataset (summary stats, correlations, missing values, etc.)
LLM-powered narrative: turns raw analysis into an insightful story
Automatic visualization generation (heatmaps, bar charts, scatter plots, etc.)
Works with different datasets:

📚 goodreads.csv – Book ratings and genres

😀 happiness.csv – World Happiness Report

🎬 media.csv – Ratings of movies, TV, and books


🔹 How It Works

Input CSV → Run the script with:
uv run autolysis.py dataset.csv

Processing → Script performs:
Data profiling (columns, datatypes, missing values)
Summary statistics & correlation checks
LLM calls for narrative analysis
Output → In the same directory, you’ll find:
README.md – Story of dataset analysis
chart1.png, chart2.png, … – Visualizations

🔹 Example Outputs
1. Goodreads Dataset (Books)

Insight: Fiction books dominate in number, while non-fiction often receives higher ratings.

Visualization:


2. Happiness Dataset (World Happiness Report)
Insight: Strong positive correlation between GDP per capita and happiness score.

Visualization:


3. Media Dataset (Movies & Shows)

Insight: TV series receive more consistent ratings compared to movies.

Visualization:


🔹 Tech Stack
Python 3.11+
Pandas, NumPy – Data analysis
Matplotlib / Seaborn – Visualizations
httpx – API calls
GPT-4o-Mini (AI Proxy) – Narrative generation

🔹 Setup & Usage

Clone Repository
git clone <your-repo-url>
cd <repo-name>

Set AI Proxy Token
export AIPROXY_TOKEN="your_token_here"   # Mac/Linux
setx AIPROXY_TOKEN "your_token_here"     # Windows


Run Analysis
uv run autolysis.py goodreads.csv
uv run autolysis.py happiness.csv
uv run autolysis.py media.csv


Check Results
README.md + .png files generated in corresponding dataset directories.

🔹 Repository Structure
├── autolysis.py
├── goodreads/
│   ├── README.md
│   ├── chart1.png
│   └── chart2.png
├── happiness/
│   ├── README.md
│   ├── chart1.png
│   └── chart2.png
├── media/
│   ├── README.md
│   ├── chart1.png
│   └── chart2.png
└── LICENSE

🔹 License

This project is licensed under the MIT License
