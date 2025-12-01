# **JUST-NLP 2025: Legal Summarization Shared Task (L-SUMM)** 
This repository contains our system developed for the Legal Summarization Shared Task (L-SUMM), part of the JUST-NLP 2025 Workshop on NLP for Empowering Justice, co-located with IJCNLP-AACL 2025.
# **INTRODUCTION**
The goal of the L-SUMM shared task is to generate concise, coherent, and fluent abstractive summaries (≈500 words) for Indian court judgments written in English.
The task focuses on improving legal document understanding and supports applications such as case triaging and public access to legal information.
This repository contains the implementation, trained models, and experimental scripts for abstractive summarization system developed for long-form legal case judgment summarization.
# **📂 Dataset: InLSum (Indian Legal Summarization Dataset)**

The dataset is provided in JSONL format and contains three splits:

Split	Count	Files Provided

Train	1200 samples : 	train_judg.jsonl, train_ref_summary.jsonl

Validation	200	samples:val_judg.jsonl, reference summaries hidden

Test	400 samples:	test_judg.jsonl, reference summaries hidden

 **Finetuned BART – Legal Judgment Summarization Script**
This script provides a complete end-to-end pipeline for training, evaluating, and applying a fine-tuned BART model for abstractive summarization of legal case judgments. It includes comprehensive preprocessing, supervised model training using reference summaries, generation of test summaries, and an embedding-based faithfulness scoring module.

 **Finetuned Legal-LED – Long-Document Abstractive Summarization Script**
This script implements a full pipeline for fine-tuning and evaluating the Longformer Encoder–Decoder (LED) model on lengthy legal judgments. LED is designed for extremely long input sequences, making it ideal for Indian court judgments that frequently exceed conventional transformer limits.Tokenization using LED’s extended attention window, enabling effective processing of multi-page case records

 **Fine-Tuned Legal-Pegasus – Gap-Sentence Pretraining Based Legal Summarization Script** 
This script provides the workflow for fine-tuning Legal-Pegasus, a Pegasus model adapted to legal corpora using gap-sentence pretraining. Pegasus excels at high-quality abstractive generation, making it effective for producing human-style legal summaries.

**Fine-Tuned T5 – Unified Text-to-Text Summarization Script for Legal Judgments**
This script implements training and inference for a T5-based model, leveraging the text-to-text framework to cast legal summarization as a sequence generation task. T5’s flexible architecture allows it to learn task-specific patterns in legal reasoning and summary construction.Concise summary generation focusing on key legal issues, orders, and factual elements.

 **Legal Ensemble Summarizer**
It is a multi-model framework built to generate high-quality summaries for long and complex Indian court judgments. It integrates three complementary encoder–decoder models—**BART** for fluent abstractive generation, **Pegasus** for high-compression summarization, and **Longformer-Encoder-Decoder (LED)** for processing very long documents. Each model produces a 400–500-word summary, after which a **semantic reranking step** selects the best output using cosine similarity computed from fine-tuned BART encoder embeddings. This ensures that the final summary is both coherent and highly relevant to the original judgment.


