# BiLSTM Models with and Without Pretrained Embeddings and BERT on German Patient Reviews
## Paper Link in IEEE-https://ieeexplore.ieee.org/abstract/document/10582115
📄 *Published in:* 2024 International Conference on Advances in Modern Age Technologies for Health and Engineering Science (AMATHE)  
📅 *Date:* May 16, 2024  
📍 *Pages:* 1–5  
📚 *Publisher:* IEEE  
🔗 *Citations:* Cited by 7 (as of 2025)

---

## 🧠 Overview

This repository accompanies the research paper:

> **"BiLSTM Models with and Without Pretrained Embeddings and BERT on German Patient Reviews"**  
> *Authors:* Prosenjit Roy, Md Jahid Alam Riad, Lija Akter, Nobanul Hasan, Mahfuzur Rahman Shuvo, Montaser Abdul Quader, Mozdaher Abdul Quader, Ahmed Selim Anwar

This study explores deep learning techniques for **sentiment analysis** in the healthcare domain, using a large dataset of German patient reviews. The models evaluated include:

- **BiLSTM with random embeddings**  
- **BiLSTM with pretrained word embeddings (e.g., GloVe/word2vec)**  
- **BERT (Bidirectional Encoder Representations from Transformers)**

Our objective was to determine which approach most accurately classifies patient sentiments as either **‘poor’** or **‘excellent’**.

---

## 🔍 Problem Statement

Healthcare platforms often gather large volumes of unstructured patient feedback. Automatically analyzing such feedback can:

- Help healthcare providers improve services  
- Enable patients to make informed decisions  
- Streamline review classification tasks at scale  

This research evaluates the effectiveness of different NLP models in understanding and classifying sentiment expressed in **German-language medical reviews**.

---

## 📊 Dataset

- Source: Patient review platform (approx. 500,000 reviews)  
- Data includes:
  - **Numerical rating** (used as label: ‘poor’ or ‘excellent’)
  - **Free-text review comment**

### 🔧 Preprocessing:
- Lowercasing, tokenization, stop-word removal
- Padding for BiLSTM models
- SentencePiece tokenizer for BERT input

---

## 📈 Key Results

| Model                          | Accuracy | F1 Score | Remarks                            |
|-------------------------------|----------|----------|-------------------------------------|
| BiLSTM (Random Embeddings)     | ~78%     | ~0.76    | Underperformed due to sparse vocab |
| BiLSTM (Pretrained Embeddings) | ~83%     | ~0.81    | Improved contextual understanding  |
| **BERT (German model)**        | **89%**  | **0.88** | Best performance, robust results   |

The BERT-based model outperformed both BiLSTM architectures in accuracy and class balance, demonstrating the strength of transformer-based models in multilingual sentiment analysis.

---

## 🗂️ Repository Structure

```bash
├── data/                   # Sample dataset (anonymized)
├── preprocessing/          # Scripts for data cleaning and transformation
├── models/                 # BiLSTM and BERT implementations
├── results/                # Metrics, confusion matrix, and visualizations
├── notebooks/              # Experimentation and analysis notebooks
├── paper/                  # Published paper and citation info
└── README.md               # Project overview
