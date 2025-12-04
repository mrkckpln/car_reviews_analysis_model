# 🚗 AI-Powered Car Review Analysis System

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/Hugging%20Face-Transformers-yellow?style=for-the-badge&logo=huggingface&logoColor=black)

An NLP pipeline to process, analyze, and extract insights from customer car reviews using modern Large Language Models (LLMs). This repository uses Hugging Face `transformers` to perform sentiment analysis, translation, question answering, and summarization.
---

## 🚀 Key Features & Models


This project implements a multi-task NLP pipeline:

| Task | Model Used | Description |
| :--- | :--- | :--- |
| Sentiment Analysis | `siebert/sentiment-roberta-large-english` | Classifies reviews as Positive (1) or Negative (0). |
| Translation | `Helsinki-NLP/opus-mt-en-es` | Translates English reviews into Spanish. |
| Question Answering | `deepset/minilm-uncased-squad2` | Extracts short answers from review texts. |
| Summarization | `facebook/bart-large-cnn` | Produces concise summaries of long reviews. |

---

## 🛠️ Tech Stack

* **Core:** Python 3.10+
* **Deep Learning:** PyTorch, Transformers (Hugging Face)
* **Data Processing:** Pandas
* **Metrics:** Scikit-learn (Accuracy, F1), Evaluate (BLEU Score)
* **Environment:** Python-dotenv (for secure path management)

---

## 📂 Project Structure

```bash
car_reviews_analysis_model/
│
├── data/
│   ├── car_reviews.csv              # Source dataset
│   └── reference_translations.txt   # Ground truth for translation evaluation
│
├── .env                             # Environment variables (Path configurations)
├── .gitignore                       # Git ignore rules
├── reviews.ipynb                    # Main Jupyter Notebook
├── requirements.txt                 # Project dependencies
└── README.md                        # Documentation

```
## ⚙️ Installation & Setup

1) Clone the repository

Clone the repository (example):

Bash (Linux / macOS / Git Bash / WSL):

```bash
git clone https://github.com/mrkckpln/car_reviews_analysis_model
cd car_reviews_analysis_model
```

Single-line (bash):

```bash
git clone https://github.com/mrkckpln/car_reviews_analysis_model && cd car_reviews_analysis_model
```

PowerShell (Windows PowerShell 5.1):

```powershell
git clone https://github.com/mrkckpln/car_reviews_analysis_model; Set-Location car_reviews_analysis_model
```

If you want to change into the directory only when the clone succeeded:

```powershell
git clone https://github.com/mrkckpln/car_reviews_analysis_model
if ($?) { Set-Location car_reviews_analysis_model }
```

2) Create and activate a virtual environment

Linux / macOS / Git Bash / WSL:

```bash
python -m venv venv
source venv/bin/activate
```

Windows PowerShell:

```powershell
python -m venv venv
venv\Scripts\Activate.ps1
```

3) Install dependencies

```bash
pip install -r requirements.txt
```

4) Configuration (.env)

Create a `.env` file at the project root and define the data paths:

```ini
CAR_REVIEWS_PATH=data/car_reviews.csv
REF_TRANSLATIONS_PATH=data/reference_translations.txt
```

---

## 📊 Example Performance

Example metrics may vary depending on the evaluation set and model checkpoints. Replace the placeholders below with real results after running evaluation scripts:

- Sentiment Classification Accuracy: 1.0
- F1 Score: 1.0
- Translation Quality (BLEU Score): 0.7794483794144498

---