# Transformer from Scratch (PyTorch)

This project implements a full **Encoder–Decoder Transformer architecture from first principles**, following the *“Attention Is All You Need”* paper.  
The model is built **without using `nn.Transformer`**, focusing on architectural understanding and clean design.

The implementation is **CPU-friendly** and intended for educational and internship-level demonstration purposes.

---

## 🔍 Project Overview

Transformers have become the backbone of modern NLP systems.  
This project focuses on:

- Understanding how attention works internally
- Implementing the Transformer step-by-step
- Building a clean, modular, and extensible codebase

The project currently focuses on **architecture correctness and clarity**, with training and evaluation planned as future extensions.

---

## 🧠 Architecture Overview

The Transformer follows the standard Encoder–Decoder design:

Input Tokens
↓
Input Embedding + Positional Encoding
↓
Encoder Stack (N layers)
├─ Multi-Head Self-Attention
├─ Add & Layer Normalization
├─ Feed Forward Network
└─ Add & Layer Normalization
↓
Contextual Encoder Output
↓
Decoder Stack (N layers)
├─ Masked Multi-Head Self-Attention
├─ Add & Layer Normalization
├─ Cross-Attention (Encoder–Decoder)
├─ Add & Layer Normalization
├─ Feed Forward Network
└─ Add & Layer Normalization
↓
Projection Layer
↓
Vocabulary Probabilities


---

## 🧩 Key Components Implemented

- Input Embeddings with scaling
- Sinusoidal Positional Encoding
- Multi-Head Attention (from scratch)
- Residual Connections
- Layer Normalization
- Feed Forward Networks
- Encoder and Decoder stacks
- Output Projection Layer

---

## 🛠️ Tech Stack

- Python
- PyTorch
- HuggingFace `datasets`
- HuggingFace `tokenizers`

---

## 🚀 Current Status

- ✔ Transformer architecture implemented from scratch
- ✔ CPU-ready implementation
- ✔ Modular and readable code structure
- ⏳ Training loop and dataset integration (planned)

---

## 🔮 Future Work

- End-to-end training on a small translation dataset
- Attention weight visualization
- Comparison with `nn.Transformer`
- Performance evaluation on toy datasets

---

## 📌 References

- Vaswani et al., *Attention Is All You Need* (2017)
- PyTorch Documentation
- HuggingFace Tokenizers

---

## 👤 Author

Ayush  
Machine Learning / NLP Enthusiast
