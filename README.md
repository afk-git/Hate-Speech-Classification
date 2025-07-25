# Hate Speech Classification Project

# Gcloud cli
https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe

## Introduction
This project aims to build a Hate Speech Classification system using Natural Language Processing (NLP) techniques. It classifies text (primarily tweets) as either hate speech or not hate speech. While built using Twitter data, the system is adaptable to other platforms such as Facebook, LinkedIn, Snapchat, WhatsApp, YouTube, and Instagram.

## Problem Statement
As online communication grows, so does harmful content. Detecting and mitigating hate speech is essential to ensure safer digital environments.

## Application Scope
The system can be integrated into social media platforms, enabling automatic detection, warnings, and blocking of offensive content.

## Solution Architecture & Key Technologies
We use an LSTM-based model to classify text. The project follows a modular structure for better maintainability and scalability.

### Key Technologies and Libraries:
- NLP, ML, Deep Learning (LSTM)
- TensorFlow Keras (v2.0+)
- Flask API
- Google Cloud Platform (GCP) for storage
- Python Libraries: pandas, numpy, nltk, seaborn, matplotlib, scikit-learn, google-cloud-storage, etc.

## Project Structure
```
.
└── hate-speech/
    ├── components/
    │   ├── data_ingestion.py
    │   ├── data_transformation.py
    │   ├── model_trainer.py
    │   ├── model_evaluation.py
    │   └── model_pusher.py
    ├── configuration/
    ├── constant/
    ├── entity/
    ├── exception/
    ├── logger/
    ├── ml/
    ├── pipeline/
    │   ├── training_pipeline.py
    │   └── prediction_pipeline.py
    ├── utils/
    ├── app.py
    ├── setup.py
    ├── requirements.txt
    ├── Dockerfile
    ├── .gitignore
    └── .dockerignore
```

## How to Implement the Project

### 1. Repository Setup
- Create a GitHub repo and clone it locally.
- Copy project files into the repo directory.
- Commit and push the initial project structure.

### 2. Environment Setup
- Create and activate a Conda environment with Python 3.8.
- Install dependencies via `pip install -r requirements.txt`.

### 3. GCP Configuration
- Set up GCP and install the `gcloud` CLI.
- Initialize `gcloud`, select your project and region.
- Create a storage bucket and upload `data.zip` (contains `imbalanced_data.csv` and `raw_data.csv`).

### 4. Running the Project
- Run `app.py` using: `python app.py`
- Access via `http://localhost:8080`

#### a. Training Pipeline
- Use `/training` route to trigger ingestion, transformation, training, evaluation, and model upload.

#### b. Prediction Pipeline
- Use `/prediction` route to classify new text input.

### 5. Dockerization
- Use `.dockerignore` to exclude unneeded files.
- Use `Dockerfile` to containerize the app for production.

## Data Source
Twitter data is used, combining `imbalanced_data.csv` and `raw_data.csv`. Datasets are from public sources such as Kaggle.

---