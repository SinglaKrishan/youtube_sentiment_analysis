🎯 YouTube Sentiment Analysis System

An end-to-end YouTube Comment Sentiment Analysis project that combines Machine Learning, MLOps practices (DVC), a Flask API, and a Chrome Extension frontend to analyze and visualize public sentiment on YouTube videos.

The project is designed with modular architecture, experiment tracking, and reproducibility in mind.

🚀 Key Features

📊 Sentiment classification of YouTube comments

🧠 TF-IDF + LightGBM based ML model

🔄 Reproducible ML pipeline using DVC

📁 Clean separation of data, model, and API layers

🌐 Flask-based inference API

🧩 Chrome Extension frontend for user interaction

🧪 Model evaluation with confusion matrix

📝 Centralized error logging

🛠 Tech Stack

Machine Learning

Python

TF-IDF Vectorization

LightGBM

Scikit-learn

MLOps

DVC (Data Version Control)

YAML-based configuration

Experiment metadata tracking

Backend

Flask

Pickle-based model loading

Frontend

Chrome Extension

HTML, JavaScript

🧠 ML Pipeline Overview

Data Ingestion

Raw YouTube comment datasets loaded from CSV

Data Preprocessing

Cleaning, normalization, and vectorization

Model Training

TF-IDF feature extraction

LightGBM classifier training

Model Evaluation

Accuracy, confusion matrix

Model Registration

Versioned model artifacts saved

Inference

Flask API serves predictions to frontend

📂 Project Structure
youtube-sentiment-analysis/
│
├── data/
│   ├── raw/
│   │   ├── train.csv
│   │   └── test.csv
│   └── interim/
│       ├── train_processed.csv
│       └── test_processed.csv
│
├── src/
│   ├── data/
│   │   ├── data_ingestion.py
│   │   └── data_preprocessing.py
│   └── model/
│       ├── model_building.py
│       ├── model_evaluation.py
│       └── register_model.py
│
├── flask_api/
│   └── main.py
│
├── yt-chrome-plugin-frontend/
│   ├── manifest.json
│   ├── popup.html
│   └── popup.js
│
├── dvc.yaml
├── dvc.lock
├── params.yaml
├── requirements.txt
├── setup.py
│
├── lgbm_model.pkl
├── tfidf_vectorizer.pkl
├── confusion_matrix_Test Data.png
│
├── experiment_info.json
├── errors.log
├── model_building_errors.log
├── model_evaluation_errors.log
├── model_registration_errors.log
├── preprocessing_errors.log
│
├── LICENSE
└── README.md

📊 Model Artifacts

TF-IDF Vectorizer → tfidf_vectorizer.pkl

Trained LightGBM Model → lgbm_model.pkl

Evaluation Output

Confusion matrix image

Experiment metadata in JSON

🧪 Experiment Tracking & Reproducibility

All datasets, models, and pipelines are versioned using DVC

Parameters managed via params.yaml

Experiments logged using structured metadata files

Ensures reproducibility across environments

🌐 Chrome Extension Workflow

User opens a YouTube video

Extension captures video context

Requests sentiment prediction via API

Displays aggregated sentiment result in popup UI

⚠️ Limitations

Sentiment accuracy depends on comment quality

Sarcasm and mixed-language comments can reduce accuracy

Large-scale comment analysis may require optimization

🔮 Future Enhancements

Multilingual sentiment analysis

Emotion-level classification (happy, angry, sad)

Time-based sentiment trends

Model performance monitoring

Advanced UI visualization

📌 Author

Krishan Singla
AI / Machine Learning Engineer
Focused on building real-world, production-oriented ML systems 🚀