# Sentiment Analysis Web App

Sentiment Analysis Web App is a Flask-based machine learning project that predicts whether a piece of text expresses positive or negative sentiment. The application uses an NLP preprocessing pipeline, a Bag-of-Words vectorizer, and a saved classification model to convert raw text into structured features and generate sentiment predictions through a simple web interface.

## Features

- Sentiment prediction for user-entered text
- NLP preprocessing with text cleaning and stemming
- Removal of mentions, special characters, and emojis
- Bag-of-Words feature extraction using a saved vectorizer
- Pretrained machine learning model for binary sentiment classification
- Lightweight web interface built with Flask templates

## Tech Stack

- Python
- Flask
- Scikit-learn
- NLTK
- Joblib
- Pickle
- HTML

## Project Structure

```text
Sentiment_Analysis/
|-- app.py
|-- wsgi.py
|-- index.py
|-- templates/
|   |-- home.html
|-- regmodel.pkl
|-- bow_vectorizer.joblib
|-- xgb_model.joblib
|-- xgb_model.json
|-- Twitter_Sentiments.csv
|-- Twitter_sentiment.ipynb
|-- requirenments.txt
|-- README.md
```

## How It Works

1. The user enters text through the web interface.
2. The app preprocesses the text by removing mentions, emojis, and unwanted characters.
3. The cleaned text is transformed into numerical features using the saved Bag-of-Words vectorizer.
4. The trained model predicts the sentiment label.
5. The final result is displayed back to the user in the browser.

## Dataset

The project includes `Twitter_Sentiments.csv`, which contains labeled tweet data for sentiment-related experimentation and model development.

## Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd Sentiment_Analysis
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

On Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:

```bash
source venv/bin/activate
```

### 3. Install dependencies

If you are using the existing dependency file:

```bash
pip install -r requirenments.txt
```

Or install the common packages manually:

```bash
pip install flask nltk scikit-learn joblib
```

## Running the Project

Start the Flask app with:

```bash
python app.py
```

Then open the local server in your browser:

```text
http://127.0.0.1:5000
```

## Files Used in Inference

- `regmodel.pkl` stores the trained sentiment classification model
- `bow_vectorizer.joblib` stores the fitted Bag-of-Words vectorizer
- `templates/home.html` provides the frontend interface
- `app.py` contains the preprocessing and prediction logic

## NLP Preprocessing Steps

The application applies several preprocessing steps before prediction:

- removes tagged usernames such as `@user`
- removes special characters and non-letter symbols
- strips emojis and unsupported Unicode characters
- filters short words
- applies stemming using `PorterStemmer`

## Example Use Cases

- Social media sentiment testing
- Introductory NLP project demonstrations
- Text classification portfolio projects
- Web deployment practice for ML models

## Current Limitations

- The current application performs binary sentiment classification only
- Model performance depends on the quality of the saved training artifacts
- The app uses pretrained local model files rather than retraining dynamically
- Some file names, such as `requirenments.txt`, may need cleanup for production use

## Future Improvements

- Add confidence scores for predictions
- Support neutral sentiment classification
- Improve the frontend with history and batch input support
- Add retraining scripts and evaluation metrics
- Deploy the app using a cloud platform

## Author Note

This project is suitable for demonstrating practical skills in Flask, NLP preprocessing, text vectorization, and ML model integration in a web application.

