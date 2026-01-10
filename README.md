# 📊 Comparative Study of Transformer Models for Twitter Sentiment & Mental Health Analysis

This repository contains the **experimental code and results** for a comparative analysis of **state-of-the-art transformer-based NLP models** applied to **Twitter sentiment analysis and mental health severity detection**.

The work focuses on evaluating **model performance, stability, and efficiency** across **two benchmark datasets**, using multiple transformer architectures under controlled experimental settings.

---

## 🧠 Project Overview

Social media platforms such as Twitter (now X) provide rich textual data reflecting public sentiment and emotional states. This project investigates how different transformer models perform in:

- **Mental health severity detection**
- **General sentiment classification**
- **Efficiency vs accuracy trade-offs**
- **Robustness on noisy, short-text social media data**

---

## 📁 Repository Structure

This repository consists of **three Jupyter Notebook (`.ipynb`) files**, each dedicated to a specific dataset and model configuration:
```text
├── Dataset 1 ADAM-SDMH Results and code.ipynb
├── Dataset 2 RoBERTa-Large.ipynb
├── Dataset-2  BERT, RoBERTa-base, DistilBERT.ipynb
```

---

## 📘 Notebook Descriptions

### 🔹 1. Dataset 1 ADAM-SDMH Results and code.ipynb

- **Dataset**: ADAM-SDMH (Mental Health Severity Detection)
- **Task**: Multi-class mental health severity classification
- **Classes**:
  - 0: Neutral / Non-mental-health-related
  - 1: Mild emotional distress
  - 2: High severity distress
- **Models evaluated**:
  - BERT-base
  - RoBERTa-base
  - RoBERTa-large
  - DistilBERT
- **Includes**:
  - Data preprocessing
  - Model fine-tuning
  - Accuracy & loss curves
  - Confusion matrices
  - Class-wise performance metrics

### 🔹 2. Dataset 2 RoBERTa-Large.ipynb

- **Dataset**: TweetEval – Sentiment Classification
- **Task**: Three-class sentiment classification
- **Classes**:
  - Negative
  - Neutral
  - Positive
- **Model**:
  - RoBERTa-Large
- **Focus**:
  - High-capacity transformer performance
  - Training stability
  - Convergence behavior
  - Performance on large-scale Twitter sentiment data

### 🔹 3. Dataset-2 BERT, RoBERTa-base, DistilBERT.ipynb

- **Dataset**: TweetEval – Sentiment Classification
- **Models compared**:
  - BERT-base
  - RoBERTa-base
  - DistilBERT
- **Objective**:
  - Compare lightweight vs base transformer architectures
  - Analyze efficiency–accuracy trade-offs
  - Benchmark against RoBERTa-Large results

---

## ⚙️ Experimental Setup

- **Platform**: Kaggle Notebook
- **Hardware**: NVIDIA T4 GPU (16 GB VRAM)
- **Optimizer**: AdamW
- **Loss Function**: Categorical Cross-Entropy
- **Frameworks**:
  - PyTorch
  - Hugging Face Transformers
- **Evaluation Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

---

## 📈 Key Observations

- **DistilBERT** achieves strong performance on the ADAM-SDMH dataset despite its lightweight architecture.
- **RoBERTa-Large** performs best on TweetEval sentiment classification.
- Model size alone does not guarantee better performance.
- Mild vs high-severity mental health classes remain challenging due to linguistic ambiguity in tweets.

---

## 🚀 Reproducibility

Each notebook is:

- Fully self-contained
- Includes preprocessing, training, and evaluation
- Ready to run with minimal configuration

⚠️ **Ensure GPU is enabled before execution for reasonable training time.**

---

## 📜 Citation

If you use this work or code, please cite the corresponding research paper or acknowledge the repository.

---

## 🤝 Contributions & Feedback

Contributions, issues, and suggestions are welcome.

Feel free to open an issue or submit a pull request.
