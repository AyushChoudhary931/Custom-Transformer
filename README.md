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

flowchart TD
    A[Input Text<br/>(Source Sentence)] --> B[Tokenizer]
    B --> C[Token IDs]
    C --> D[Input Embedding]
    D --> E[Positional Encoding]

    E --> F[Encoder Stack]

    subgraph Encoder[Encoder (N Layers)]
        F1[Multi-Head Self-Attention]
        F2[Add & Layer Normalization]
        F3[Feed Forward Network]
        F4[Add & Layer Normalization]

        F1 --> F2 --> F3 --> F4
    end

    F --> G[Encoder Output<br/>(Context Representation)]

    G --> H[Decoder Stack]

    subgraph Decoder[Decoder (N Layers)]
        H1[Masked Multi-Head Self-Attention]
        H2[Add & Layer Normalization]
        H3[Cross Attention<br/>(Encoder–Decoder)]
        H4[Add & Layer Normalization]
        H5[Feed Forward Network]
        H6[Add & Layer Normalization]

        H1 --> H2 --> H3 --> H4 --> H5 --> H6
    end

    H --> I[Decoder Output]
    I --> J[Linear Projection]
    J --> K[Softmax]
    K --> L[Predicted Output Tokens]

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
