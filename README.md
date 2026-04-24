# Kaggle: Fake or Real — The Impostor Hunt in Texts

This repository contains my notebook and modeling experiments for the Kaggle competition **Fake or Real: The Impostor Hunt in Texts**, part of the European Space Agency’s *Secure Your AI* competition series.

The challenge focuses on detecting which text in a pair is “real” and which is “fake” after both have been substantially modified using large language models. Each sample contains two related texts: one closer to the hidden original document and one more corrupted or misleading version.

The competition is framed around AI security risks, including data poisoning, hallucination, hidden triggers, and overreliance on LLM-generated outputs.

My entry placed 395 out of 992 entrants (top 40%).

## Problem

For each document pair, the model must choose which file is the real text:

- `file_1.txt`
- `file_2.txt`

The task is not ordinary binary classification of isolated documents. It is a **pairwise preference problem**: given two texts from the same underlying source, predict which one is more faithful to the original.

Submissions are evaluated using **pairwise accuracy**, meaning the score depends on how often the model selects the correct text within each pair.

## Competition Context

The data comes from public, space-related research and organizational texts, including materials about scientific devices, research outcomes, workshops, engineering, science, and astronauts.

The competition is connected to ESA’s work on AI assurance for space-domain applications and is based on real AI security concerns relevant to mission operations and document-processing workflows.

## Repository Contents

```text
.
├── phase3-sci-ensemble-inference-v1.ipynb   # Main Kaggle notebook
├── README.md                                # Project overview
└── .gitignore                               # Excludes data, model artifacts, and local files