# **INTRODUCTION**
This repository contains the implementation, trained models, and experimental scripts for abstractive summarization system developed for long-form legal case judgment summarization.
# **Finetuned BART – Legal Judgment Summarization Script**
This script provides a complete end-to-end pipeline for training, evaluating, and applying a fine-tuned BART model for abstractive summarization of legal case judgments. It includes comprehensive preprocessing, supervised model training using reference summaries, generation of test summaries, and an embedding-based faithfulness scoring module.
# **Finetuned Legal-LED – Long-Document Abstractive Summarization Script**
This script implements an end-to-end pipeline for fine-tuning and applying LED on very long legal judgments. It includes long-document preprocessing and tokenization using LED’s extended attention window, supervised fine-tuning on reference summaries, generation for test cases, and an encoder-based cosine faithfulness score to measure semantic retention across multi-page case texts.
