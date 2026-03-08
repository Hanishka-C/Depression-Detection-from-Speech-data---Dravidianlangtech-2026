# 🧠 Depression Detection in Dravidian Languages: ACL 2026
**Official Implementation: Joint Global Rank 1 (Tamil) | Rank 2 (Malayalam)**

[![Status](https://img.shields.io/badge/Paper_Status-Under_Review-yellow.svg)](#-citation--status)

---

## 📌 Project Overview
This repository contains the winning hybrid deep learning implementation for the **DravidianLangTech Shared Task @ ACL 2026**. Our research focuses on detecting signs of depression from raw audio signals in low-resource languages (Tamil and Malayalam).

By leveraging a custom **CNN-BiLSTM** architecture, we successfully captured both the spectral "fingerprints" and the temporal "prosody" of depressed speech.

### 🏆 Global Rankings
* 🥇 **Tamil:** Joint Rank 1 (**Macro F1-Score: 1.0**)
* 🥈 **Malayalam:** Rank 2 (**Macro F1-Score: 0.995**)

---

## 🏗️ Technical Methodology

### 1. Feature Engineering
We utilized a multi-dimensional approach to audio feature extraction:
* **Core Feature:** 40 Mel-Frequency Cepstral Coefficients (MFCCs).
* **Dynamic Features:** Stacked **Delta** and **Delta-Delta** coefficients to track energy changes and speech velocity.
* **Preprocessing:** Audio standardized to **16,000 Hz** with 5-second padding for uniform input.



### 2. Model Architecture: CNN-BiLSTM
The architecture is designed to capture both local acoustic textures and long-term vocal patterns:
* **CNN (Spatial):** Three 1D-Convolutional layers (128, 256, 512 filters) extract acoustic features.
* **BiLSTM (Temporal):** Dual Bidirectional LSTM layers (128, 64 units) capture rhythm and pauses from both past and future contexts.
* **Regularization:** Batch Normalization and Dropout (0.3 - 0.5) were used to ensure generalization across different speakers.



---

## 📊 Evaluation Results
Task : Depression Detection<br>
| Language      | Global Rank | Macro F1-Score |
| :--- | :---: | :---: |
| **Tamil**     |   **1**   |     **1.00**   |
| **Malayalam** |   **2**   |    **0.995**   |



---

## 👥 Authors

* **Hanishka C** — Lead Researcher, Kongu Engineering College  
* **Preethi K** — Lead Researcher, Kongu Engineering College  

> **Note on Authorship:** Both authors contributed equally to this work. This includes the conceptualization of the CNN-BiLSTM architecture, feature extraction pipeline development, and model optimization.

---

## 📜 Status
*This paper is currently **Under Review** for the DravidianLangTech Workshop at ACL 2026. The full paper text is private until official publication.*
