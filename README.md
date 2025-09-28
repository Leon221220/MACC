# **From Long to Lean: Performance-aware and Adaptive Chain-of-Thought Compression via Multi-round Refinement**

[![Paper](https://img.shields.io/badge/Paper-EMNLP%202025-blue)](link_to_paper_pdf)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📌 Overview
This repository provides the official implementation of **MACC**, a framework for **adaptive multi-round compression of Chain-of-Thought (CoT) reasoning**.  
MACC dynamically shortens reasoning traces while preserving accuracy, achieving:

* **5.6% higher accuracy** vs. state-of-the-art CoT compression baselines  
* **~47 tokens shorter CoT** on average  
* Significant **inference-latency reduction**

Key idea: **Token Elasticity** – overly tight token budgets may paradoxically increase output length.  
MACC exploits this with **progressive multi-round compression** and a **performance estimation module** that predicts final accuracy/length before fine-tuning.


---

## ✨ Features
* **Multi-round adaptive compression** with automatic stopping criterion  
* **Performance Estimation Hypothesis**: Bayesian regression to predict compressed-CoT accuracy & token cost  
* Plug-and-play with various LLMs (e.g., LLaMA-3.1, Qwen2.5, DeepSeek-R1) and compressors (e.g., GPT-4o-mini)

---

## 🛠️ Installation
```bash
git clone https://github.com/<your-username>/MACC.git
cd MACC
conda create -n macc python=3.10
conda activate macc
pip install -r requirements.txt
```

## 🧠 Citation

If you find this work useful, please cite:

```
@inproceedings{yan2025macc,
  title     = {From Long to Lean: Performance-aware and Adaptive Chain-of-Thought Compression via Multi-round Refinement},
  author    = {Jianzhi Yan and Le Liu and Youcheng Pan and Shiwei Chen and Zike Yuan and Yang Xiang and Buzhou Tang},
  booktitle = {Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing},
  year      = {2025}
}
```
