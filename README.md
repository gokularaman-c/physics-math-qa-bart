# Domain-Specific QA for Physics & Math (BART Fine-tuning)

This project builds a domain-specific Question Answering (QA) model for physics and mathematics research paper text by fine-tuning an encoder–decoder Transformer (BART) to generate answers given a question and its corresponding context.

The objective is to adapt a general-purpose sequence-to-sequence model for answering domain-specific scientific questions.

## What’s inside

- notebooks/01-train-bart-qa.ipynb  
  Fine-tunes the BART model for question answering using Hugging Face Transformers.

- notebooks/02-evaluation-metrics.ipynb  
  Evaluates the fine-tuned model using ROUGE, BLEU, and Exact Match metrics.

## Method (high level)

1. Research papers are cleaned and divided into smaller text passages.
2. A question-generation model is used to create question–context pairs.
3. BART is fine-tuned to generate answers conditioned on the question and context.

## Reported results (from the paper)

- ROUGE-1: 0.5449
- ROUGE-2: 0.3053
- ROUGE-L: 0.5442
- Exact Match: 42.32%

## Dataset

This repository does not include dataset files.

The original work used the arXiv summarization dataset, and question–answer pairs were generated programmatically.
Dataset paths in the notebooks reference Kaggle-style directories and should be updated when running locally.

## Local setup

Create a virtual environment and install dependencies:

python -m venv .venv

source .venv/bin/activate

pip install -r requirements.txt

## Notes

- Training and evaluation were originally performed on Kaggle.
- This repository reorganizes the project for clarity and reproducibility on GitHub.
- Some notebook sections are exploratory and not part of the final training pipeline.
