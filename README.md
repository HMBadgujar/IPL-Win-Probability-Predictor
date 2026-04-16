# 🏏 IPL Win Probability Predictor

**An end-to-end Machine Learning web app predicting real-time IPL win probabilities using Streamlit.**

## 📌 Overview
The **IPL Win Probability Predictor** is a machine learning-based web application that forecasts the real-time, over-by-over winning probability of teams in the Indian Premier League (IPL). By inputting current match situations (such as target score, current runs, overs completed, and wickets lost), the model evaluates historical match data and current constraints to accurately output the winning percentage for both the batting and bowling teams.

## ✨ Features
* **Live Match Situation Analysis:** Input current match metrics (Target, Score, Overs, Wickets) to get instant probabilities.
* **Venue & Team Specifics:** Factors in the host city and the specific teams playing, accounting for venue biases and team strengths.
* **Smooth Probability Scaling:** Uses Logistic Regression under the hood to ensure probability percentages scale realistically over the course of the match rather than jumping erratically.
* **Interactive UI:** A clean, easy-to-use web interface built completely in Python using Streamlit.

## 🛠️ Tech Stack
* **Language:** Python
* **Machine Learning:** Scikit-Learn (Logistic Regression / Pipeline / ColumnTransformer)
* **Data Manipulation:** Pandas, NumPy
* **Frontend/UI:** Streamlit
* **Deployment:** Ready for cloud hosting (Heroku/Render) via `Procfile` and `setup.sh`

## 📂 Dataset Details
The model is trained on extensive historical IPL data. The repository includes several statistical datasets to enrich the analysis:
* `matches.csv` - Historical match data including venues, toss decisions, and outcomes.
* `teams.csv` & `teamwise_home_and_away.csv` - Team identifiers and performance splits.
* `players.xlsx` & `most_runs_average_strikerate.csv` - In-depth player profiles and batting statistics.

## 🚀 Run Locally

Follow these steps to run the project on your local machine:

**1. Clone the repository**
```bash
git clone [https://github.com/HMBadgujar/IPL-Win-Probability-Predictor.git]
cd IPL-Win-Probability-Predictor
```

2. Create a Virtual Environment (Optional but recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install Dependencies

```bash
pip install -r requirements.txt
```

4. Model Training (Optional)
If you wish to retrain the model or see the exploratory data analysis, run the Jupyter Notebook:

```bash
jupyter notebook
(Open the source .ipynb file and run the cells to generate the pipe.pkl model file).
```

5. Run the Streamlit App

```bash
streamlit run app.py
The web app will open automatically in your browser at http://localhost:8501.
```

## 🌐 Deployment

This repository is pre-configured for cloud deployment on platforms like Heroku.

1. requirements.txt: Lists all python dependencies.

2. setup.sh: Configures the Streamlit server settings for the cloud environment.

3. Procfile: Contains the command to execute the app on the web server.
