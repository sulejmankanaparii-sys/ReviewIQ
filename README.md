# ReviewIQ – AI-Powered Review Intelligence System

> Understand any Amazon product in seconds — no reading required.

## Overview

ReviewIQ is a deep learning-powered NLP system that analyzes Amazon product reviews and breaks them down into meaningful insights. Instead of reading hundreds of reviews, users simply enter a Product ID and instantly see how customers feel about the product's **quality**, **price**, **packaging**, and **taste/smell**.

Built on the [Amazon Fine Food Reviews dataset](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) (568,454 reviews, 1999–2012).

---

## Problem Statement

Amazon products often show an average rating of 4.5/5, but that number hides the full story. Customers rarely read all reviews — they trust the star rating and buy. ReviewIQ solves this by automatically analyzing the text of every review and surfacing what people actually talk about: what they love, what they complain about, and why.

---

## What ReviewIQ Does

- Enter a **Product ID** from the dataset
- Get an instant breakdown:
  - Overall sentiment (Positive / Negative)
  - Aspect scores: Quality, Price, Packaging, Taste/Smell
  - Top complaints and top praises
  - Buy recommendation based on review analysis

---

## Dataset

| Field | Details |
|---|---|
| Source | [Kaggle – Amazon Fine Food Reviews](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) |
| Size | 568,454 reviews |
| Period | October 1999 – October 2012 |
| Key columns | `ProductId`, `Score`, `Summary`, `Text`, `HelpfulnessNumerator` |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3.10+ |
| Deep Learning | PyTorch / Keras (TensorFlow) |
| NLP Model | DistilBERT (fine-tuned) + LSTM (from scratch) |
| Demo | Streamlit |
| Notebook | Google Colab |
| Version Control | GitHub |

---

## Project Structure

```
ReviewIQ/
├── notebook/
│   └── ReviewIQ_main.ipynb     # Main notebook (EDA → Model → Evaluation)
├── streamlit/
│   └── app.py                  # Streamlit demo application
├── README.md                   # Project description
└── requirements.txt            # Python dependencies
```

---

## Notebook Structure

Following the course project requirements:

1. Dataset details & business problem
2. Preprocessing (cleaning, tokenization, normalization)
3. Model — from scratch (LSTM) + pretrained (DistilBERT fine-tuning)
4. Hyperparameter tuning
5. Training loss & accuracy tracking (model.history)
6. model.predict()
7. model.evaluate() — Accuracy, F1, Confusion Matrix
8. Result interpretation & aspect analysis
9. Technical report (GPU/CPU details, memory usage)
10. Next steps
11. Lessons learned
12. Presentation

---

## Team

| Student | Responsibility |
|---|---|
| Student 1 | Dataset analysis, EDA, business problem, labeling |Preprocessing, tokenization, NLP pipeline |Deep learning model, training, hyperparameter tuning |
| Student 2 | Evaluation, aspect analysis |
| Student 3 | Streamlit demo, final report |

---

## How to Run

### Notebook
Open directly in Google Colab:
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. File → Open notebook → GitHub → search `ReviewIQ`
3. Open `ReviewIQ_main.ipynb`

### Streamlit Demo
```bash
pip install -r requirements.txt
streamlit run streamlit/app.py
```

---

## Course Information

- **Course:** Deep Learning / AI
- **Session:** Presentation in Session 7 & 8
- **Submission:** Notebook (.ipynb) + PDF uploaded to D2L
