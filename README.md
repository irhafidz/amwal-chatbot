---
title: "Amwal Chatbot: Development and Evaluation of a Source-Grounded RAG for Indonesian Islamic Philanthropy Law"
author: "Annisa Nur Fauzi, Irmasari Hafidz*, Najwan Firdaus Haris, Nur Aini Rakhmawati" *corresponding author: irma (at) its.ac.id
affiliation: "Institut Teknologi Sepuluh Nopember, Surabaya, Indonesia"
---

## Repository Structure

Planned organization; research files have not yet been uploaded.

```text
amwal-chatbot/
├── data/           # Corpus metadata and evaluation materials
├── src/            # Indexing, retrieval, re-ranking, and chatbot implementation
├── evaluation/     # Ragas evaluation and statistical analysis
└── README.md       # Project introduction
```

## Introduction

This repository accompanies the research paper **"Amwal Chatbot: Development and Evaluation of a Source-Grounded RAG for Indonesian Islamic Philanthropy Law."**

Amwal provides Indonesian-language answers about zakat, infaq, sadaqah, waqf, and qurban using retrieval-augmented generation (RAG). The system combines query normalization, document retrieval, cross-encoder re-ranking, and source citations to make answers traceable to their references.

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

## Main Results

GPT-4o mini’s Factual Correctness increased from 0.357 without retrieval to 0.516 with RAG and re-ranking (p = 0.001). Re-ranking improved mean scores for both generators, but its additional gains over basic RAG were not statistically significant. User acceptance averaged 4.51 out of 5.

## Acknowledgment

The authors thank Yayasan Manarul Ilmi (YMI) ITS for supporting this study as a pilot project.

## Disclaimer

Amwal is an informational research prototype, not a substitute for an official fatwa.
