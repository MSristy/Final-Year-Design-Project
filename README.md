# Deciphering Unknown Scripts Using Statistical Analysis and Zero-Reference Machine Learning

Final Year Design Project (FYDP)

Department of Computer Science and Engineering  
United International University (UIU)

---

## Abstract

This repository contains the complete implementation of our Final Year Design Project, which proposes a two-phase computational framework for analysing and deciphering unknown writing systems without relying on bilingual inscriptions, translation dictionaries, or external linguistic references.

The framework combines statistical language modelling, machine learning, information theory, computational linguistics, and cryptographic techniques to determine whether an unknown symbol sequence represents a natural language and, if so, attempts zero-reference decipherment using language-family-aware decoding strategies.

---

## Repository Structure

```
FYDP/

├── Phase1/
│   ├── phase1-fydp3.ipynb
│   └── phase_1_figures/
│
├── Phase2/
│   ├── phase2-fydp3.ipynb
│   └── phase_2_figures/
│
└── README.md
```

---

## Project Overview

The framework is divided into two independent but connected phases.

### Phase 1 — Statistical Classification of Unknown Symbol Sequences

Phase 1 determines whether an unknown sequence belongs to one of four structural categories.

- Natural Language
- Cipher
- Random Sequence
- Decorative Pattern

The notebook implements the following pipeline:

1. Image-based symbol extraction
2. Multilingual corpus construction
3. Synthetic dataset generation
4. Statistical language modelling
5. Feature engineering
6. XGBoost classification

The classifier is trained using thirteen statistical features derived from entropy, n-gram probability, Index of Coincidence, Zipf statistics, and sequence-level structural characteristics.

---

### Phase 2 — Zero-Reference Decipherment

Sequences classified as language-like proceed to the second phase.

The second notebook implements seven independent modules:

1. Multilingual corpus collection
2. Statistical fingerprint generation
3. Script type detection
4. Language family classification
5. Novel language detection
6. Zero-reference decoding
7. Extended cipher handling

The decoding framework combines frequency analysis, Markov Chain Monte Carlo (Metropolis-Hastings), Expectation Maximization refinement, and statistical language models to recover hidden character mappings without any prior key.

---

## Methodology

The complete workflow is shown below.

```

Unknown Script
│
├── Image Processing
│
├── Symbol Extraction
│
├── Statistical Feature Extraction
│
├── XGBoost Classification
│
├── Language?
│
├── No
│ ├── Cipher
│ ├── Random
│ └── Decorative
│
└── Yes
│
├── Script Type Detection
├── Language Family Identification
├── Novel Language Detection
├── Zero-Reference Decoding
└── Decoded Output

```

---

## Technologies

Programming Language

- Python 3.10

Machine Learning

- XGBoost
- Scikit-learn

Deep Learning

- PyTorch

Image Processing

- OpenCV

Data Analysis

- NumPy
- Pandas

Visualization

- Matplotlib

Development Platform

- Kaggle Notebook

---

## Experimental Results

### Phase 1

| Metric | Value |
|---------|------:|
| Overall Classification Accuracy | 90.14% |
| Language Precision | 99% |
| Decorative Precision | 100% |
| Best Accuracy (Long Sequences) | 98.9% |

### Phase 2

| Metric | Value |
|---------|------:|
| Script Type Detection | 95.7% |
| Language Family Classification | 74.62% |
| Novel Language Detection | 100% |
| Long Text Decoding Accuracy | 72–95% |
| Best Decoding Accuracy | 95.37% |

---

## Figures

All experimental figures generated throughout the project are available in

```

Phase1/phase_1_figures/

Phase2/phase_2_figures/

```

---

## Running the Project

Clone the repository

```bash
git clone https://github.com/USERNAME/FYDP.git
```

Open either notebook using Jupyter Notebook or Kaggle.

```
Phase1/phase1-fydp3.ipynb

Phase2/phase2-fydp3.ipynb
```

Run all notebook cells sequentially.

---

## Research Contributions

This work introduces a unified framework capable of

- Classifying unknown symbol sequences without external references
- Detecting previously unseen language families
- Performing language-family-aware statistical decoding
- Recovering character mappings using zero-reference optimisation
- Supporting multiple cipher structures within a single framework

