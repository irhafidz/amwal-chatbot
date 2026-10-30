---
title: "Amwal Chatbot: Source-Grounded Retrieval-Augmented Generation for Enhancing Public Access to Indonesian Islamic Philanthropy Regulations"
author: "Annisa Nur Fauzi, Irmasari Hafidz*, Najwan Firdaus, Haris Nur Aini Rakhmawati *corresponding author"
date: "30/10/2026"
conference: "Submission for the IEEE 2026 8th Symposium on Future Telecommunication Technologies (SOFTT), 1-2 December, Yogyakarta, Indonesia"
---




## Introduction #amwal-chatbot
Amwal stands for *Aplikasi Waqaf Aman Legal*. It is an Indonesian-language chatbot for questions about zakat, infaq, sadaqah, waqf, and qurban. This repository accompanies the research paper **“Amwal Chatbot: Source-Grounded Retrieval-Augmented Generation for Enhancing Public Access to Indonesian Islamic Philanthropy Regulations”** The paper is submitted to the IEEE 2026 8th Symposium on Future Telecommunication Technologies (SOFTT), under the theme “Forging Trustworthy and Sustainable Telecommunication Systems in the AI and Quantum Era.”

The system combines retrieval-augmented generation (RAG), query normalization, cross-encoder re-ranking, and source citations to provide answers grounded in publicly available Indonesian regulations, fatwas, and educational materials, including documents from the Ministry of Religious Affairs, Badan Wakaf Indonesia (BWI), Badan Amil Zakat Nasional (BAZNAS), and the Indonesian Ulema Council (MUI), including its National Sharia Council (DSN-MUI).

## Repository Structure

```text
amwal-chatbot/
├── figures/              # High resolution figures from the paper
├── source-regulatory/    # 68 source documents, the 50-question evaluation (Q&A) set with its reference answers
├── evaluation/           # Ragas evaluation and statistical analysis
└── README.md             # Project introduction
```

## Dataset

- 68 Indonesian documents: 41 regulatory and 27 educational documents.
- 2,618 indexed text chunks.
- 50 expert-validated evaluation questions across four topic groups and three difficulty levels.
- User acceptance evaluation involving 30 respondents.

## Methodology

1. Extract, clean, and segment documents using structure-aware chunking.
2. Embed passages using `multilingual-e5-base` and index them with FAISS.
3. Normalize informal or misspelled questions through query analysis.
4. Compare three configurations: LLM only, RAG with three retrieved passages, and RAG with ten candidates re-ranked to three using `mxbai-rerank-base-v2`.
5. Evaluate GPT-4o mini and Gemini 3.6 Flash using four Ragas metrics, paired Wilcoxon tests, and user acceptance ratings.

## Results

GPT-4o mini’s Factual Correctness increased from 0.357 without retrieval to 0.516 with RAG and re-ranking (p = 0.001). Re-ranking improved mean scores for both generators, but its additional gains over basic RAG were not statistically significant. User acceptance averaged 4.51 out of 5.

## Acknowledgment

This research is funded by the Higher Education Technology and Innovation (HETI) Project ADB Loan 4110-INO under Contract Number 0008/01.PKS/PPK-HETI/ITS/2026. The authors gratefully acknowledge the cooperation of Yayasan Manarul Ilmi and Masjid Manarul Ilmi at Institut Teknologi Sepuluh Nopember for their support during the chatbot development.

## Disclaimer

Amwal is an informational research prototype, not a substitute for an official fatwa.
