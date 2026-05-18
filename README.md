# Evaluating Grammar and Spelling Correction Models Across Low-Quality Text Domains

A comprehensive empirical evaluation of grammar and spelling correction systems across three noisy real-world domains: social media, OCR output, and product reviews.

## Overview

This research compares **rule-based**, **statistical n-gram**, and **transformer-based** (BERT, BART, T5) models for grammatical error correction on noisy text. It proposes a **domain-adaptive fine-tuning** strategy with character-level synthetic noise injection that improves out-of-distribution F1 by **+8.4 points** on average.

## Key Results

| Model | F1-Score | GLEU | Edit Dist. |
|-------|----------|------|------------|
| Rule-Based (LanguageTool) | 0.58 | 0.51 | 4.82 |
| Statistical (n-gram + KenLM) | 0.68 | 0.63 | 3.41 |
| BERT (fine-tuned) | 0.81 | 0.76 | 2.18 |
| BART-base | 0.84 | 0.79 | 1.94 |
| T5-base (fine-tuned) | 0.87 | 0.82 | 1.71 |
| **Proposed (T5 + Domain Adaptation)** | **0.90** | **0.86** | **1.42** |

## Highlights

- Comprehensive evaluation across **48,000+ sentences** from three noisy domains
- Characterised model robustness at three controlled noise intensities (low/medium/high)
- Proposed system achieves a **35% relative reduction in high-noise degradation**
- Ablation study isolating the contribution of each system component

## Algorithms & Tools

**Models:** BERT, BART, T5, GECToR-style edit tagging, 5-gram Kneser-Ney LM, LanguageTool + Hunspell  
**Training:** AdamW, cosine learning rate decay, FP16 mixed precision, three-stage curriculum learning  
**Stack:** Python 3.11, PyTorch 2.2, HuggingFace Transformers 4.41, KenLM, Tesseract 5.3

## Paper

📄 **[Read the full paper (PDF)](./Ashima_research_paper_enhanced.pdf)**

## Citation

```bibtex
@misc{garg2026gec,
  author = {Ashima Garg},
  title  = {Evaluating Grammar and Spelling Correction Models Across Low-Quality Text Domains},
  year   = {2026},
  note   = {Chitkara University, Punjab, India}
}
```

## Author

**Ashima Garg** — B.E. Computer Science and Engineering, Chitkara University
