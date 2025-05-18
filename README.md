# 🧠 Vision Transformer (ViT) from Scratch — CIFAR-10 Classification

> A full PyTorch implementation of the Vision Transformer (ViT) architecture, based on the seminal paper **"An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale"** by Dosovitskiy et al., applied to image classification on CIFAR-10.

---

## 📌 Overview

This repository contains a **from-scratch implementation** of the Vision Transformer (ViT), a groundbreaking architecture that adapts the Transformer — originally designed for NLP — to image classification tasks. The implementation closely follows the design and methodology proposed in the influential paper:

> **An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale**  
> *Alexey Dosovitskiy, Lucas Beyer, Alexander Kolesnikov, Dirk Weissenborn, et al. (Google Research, 2020)*  
> [[arXiv:2010.11929](https://arxiv.org/abs/2010.11929)]

This notebook demystifies the core mechanisms of ViT by building each component from scratch and training the model on the **CIFAR-10** dataset.

---

## 📚 Paper Contribution Summary

The Vision Transformer replaces convolutional layers with pure Transformer blocks by:
- Splitting the input image into fixed-size patches (e.g., 16×16)
- Linearly embedding each patch into a vector
- Adding positional encodings
- Feeding the sequence into a standard Transformer encoder architecture
- Using a `[CLS]` token for final classification output

---

## 🧠 Architecture Summary

The key components implemented are:

- **Patch Embedding**: Splits the image into non-overlapping patches, flattens them, and projects to a latent embedding dimension.
- **Class Token**: A learnable token prepended to the patch sequence to aggregate global image representation.
- **Positional Embedding**: Encodes spatial information via learnable embeddings.
- **Transformer Encoder Blocks**: Stacked multi-head self-attention (MHSA) and feedforward layers.
- **MLP Head**: Outputs logits for classification.

---

## 📊 Results Summary

| Metric         | Value     |
|----------------|-----------|
| Dataset        | CIFAR-10  |
| Input Size     | 32 × 32   |
| Accuracy       | 62.90% |
| Epochs         | 200       |
> *Note: CIFAR-10 uses 8×8 patches instead of 16×16 due to image resolution.*

---


