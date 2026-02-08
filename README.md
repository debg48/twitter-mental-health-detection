# 🧠 Comparative Study: Transformers for Mental Health & Sentiment Analysis

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-ee4c2c?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![Hugging Face](https://img.shields.io/badge/Transformers-4.30%2B-yellow?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

> **Analysing mental health severity and sentiment on Twitter using state-of-the-art Transformer models.**

This repository hosts the **code and experimental results** for a comprehensive study evaluating the performance, stability, and efficiency of various transformer architectures (BERT, RoBERTa, DistilBERT) on social media text.

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Repository Structure](#-repository-structure)
- [Datasets & Tasks](#-datasets--tasks)
- [Experimental Setup](#-experimental-setup)
- [Key Findings](#-key-findings)
- [Getting Started](#-getting-started)
- [Citation](#-citation)

---

## 🔭 Project Overview

Social media platforms like Twitter (X) are valuable sources for understanding public sentiment and mental well-being. This project rigorously compares how different transformer models handle the nuances of these short, often noisy texts.

**Core Objectives:**
*   **Mental Health Severity Detection**: Classifying the level of distress in user posts.
*   **Sentiment Analysis**: Robust classification of general sentiment (Positive/Neutral/Negative).
*   **Performance Benchmarking**: Analyzing trade-offs between model size (e.g., DistilBERT vs. RoBERTa-Large) and accuracy.

---

## � Repository Structure

The project is organized into three primary Jupyter Notebooks, each targeting specific experiments:

| File Name | Description | Key Models |
| :--- | :--- | :--- |
| `Dataset 1 ADAM-SDMH Results and code.ipynb` | **Mental Health Severity**: Full pipeline for detecting depression/anxiety levels. | BERT, RoBERTa, DistilBERT |
| `Dataset 2 RoBERTa-Large.ipynb` | **Sentiment Analysis (SOTA)**: High-capacity model focus on the TweetEval benchmark. | RoBERTa-Large |
| `Dataset-2 BERT, RoBERTa-base, DistilBERT.ipynb` | **Sentiment Analysis (Comparative)**: Efficiency benchmarking of base vs. distilled models. | BERT-Base, RoBERTa-Base, DistilBERT |

---

## 📊 Datasets & Tasks

### 1. ADAM-SDMH (Mental Health)
*   **Focus**: Severity Detection
*   **Classes**:
    *   `0`: Neutral / Non-clinical
    *   `1`: Mild Distress
    *   `2`: Severe Distress
*   **Highlights**: Handles class imbalance and linguistic ambiguity in mental health disclosures.

### 2. TweetEval (Sentiment)
*   **Focus**: General Sentiment Classification
*   **Classes**: `Negative`, `Neutral`, `Positive`
*   **Highlights**: Standard benchmark for NLP on social media.

---

## ⚙️ Experimental Setup

All experiments were conducted under controlled conditions to ensure fair comparison.

*   **Platform**: Kaggle Kernels / Google Colab
*   **Compute**: NVIDIA T4 GPU (16GB VRAM)
*   **Frameworks**: `PyTorch`, `Hugging Face Transformers`, `Scikit-learn`
*   **Optimization**:
    *   Optimizer: **AdamW**
    *   Loss Function: **Categorical Cross-Entropy** (Weighted for imbalance)
    *   Batch Size: 16/32
    *   Learning Rate: 2e-5 / 3e-5

---

## 📈 Key Findings

> [!NOTE]
> **Efficiency Surprise**: `DistilBERT` retained **~95%** of the performance of larger models while being **40% smaller and 60% faster**, making it ideal for real-time monitoring applications.

*   **RoBERTa-Large** achieved the highest F1-score on the sentiment task, demonstrating the benefit of larger pre-training corpora and dynamic masking.
*   **Class Separation**: Distinguishing between *Mild* and *Severe* distress remains the biggest challenge across all models due to overlapping linguistic markers.
*   **Preprocessing**: Consistent emoji and noise removal (implemented across all notebooks) proved critical for model stability.

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.8+ and the necessary libraries installed:

```bash
pip install torch transformers pandas scikit-learn emoji tqdm openpyxl matplotlib seaborn
```

### Running the Experiments

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/twitter-mental-health-detection.git
    cd twitter-mental-health-detection
    ```
2.  **Launch Jupyter/Colab**:
    Open any of the `.ipynb` files in your preferred environment.
3.  **Enable GPU**:
    Make sure to select a GPU runtime for training (Runtime > Change runtime type > GPU).

---

## 📜 Citation

If you use this code or findings in your research, please cite:

```bibtex
@misc{twitter-mental-health-2024,
  author = {Debg48},
  title = {Comparative Study of Transformer Models for Twitter Mental Health Analysis},
  year = {2024},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/debg48/twitter-mental-health-detection}}
}
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to verify the results, test on new datasets, or propose architecture improvements.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request
