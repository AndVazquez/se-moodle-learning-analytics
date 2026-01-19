# se-moodle-learning-analytics

Analysis pipeline for mining student learning behavior patterns from Moodle LMS logs in software engineering courses.

## Overview

This repository contains the code and analysis notebooks accompanying the paper *Learning to Learn with AI: How AI Policy Reshapes Learning Trajectories in Software Engineering Education*. The pipeline processes multi-year Moodle event logs to identify student engagement patterns and their relationship with academic performance.

## Repository structure

```
├── a1_pseudonymization_and_processing.ipynb  # data preparation & anonymization
├── a2_moodle_analysis.ipynb                  # event log analysis & feature extraction
├── a3_clustering.ipynb                       # behavioral clustering & statistical validation
├── DATA                                      # pseudonymized data
└── README.md
```

## Pipeline

| Notebook | Description |
|----------|-------------|
| **A1** | merges Moodle logs with evaluation data, applies SHA-256 pseudonymization |
| **A2** | parses events, infers resource availability, builds student×resource matrices |
| **A3** | K-Means clustering on PCA features, MANOVA/ANOVA validation, cross-cohort comparison |

## Requirements

- Python ≥ 3.10
- pandas, numpy, scikit-learn, pingouin, statsmodels, seaborn, matplotlib

## Privacy

All student identifiers are replaced with salted cryptographic hashes. Raw data is not included in this repository.

## Citation

If you use this code, please cite:

Andrea Vázquez-Ingelmo. (2025). Code repository supporting the analysis of learning trajectories in software engineering education under AI policy changes (Version 1.0). Zenodo. https://doi.org/10.5281/zenodo.XXXXXXX
