# Hybrid Digital Twin – Federated Learning IDS (DT-FL-IDS)

**Authors:** Azra Fathima, Naren Kumar  

Privacy-preserving intrusion detection framework designed to remain robust under highly Non-IID data distributions and zero-day attack scenarios in IoT environments.

---

## Overview

This work proposes a hybrid Digital Twin + Federated Learning architecture for intrusion detection.  

Each client maintains a Digital Twin autoencoder that learns device-specific normal behavior. Reconstruction errors are then used to gate federated classifier decisions, reducing false positives while maintaining high recall for novel attacks.

---

## Key Idea

Per-client Digital Twin autoencoders model normal traffic patterns.

If:
reconstruction_error(x) > T_p

→ Flag as anomaly (zero-day detection)

Else:
FL_classifier(x)

→ Classify as known attack or benign

Where:
T_p = 95th percentile of benign reconstruction errors


This hybrid decision fusion improves robustness under Non-IID settings.

---

## Dataset

Evaluated on **CICIDS2017**.

---

## Performance Summary

| Metric | DT-FL Hybrid | Standalone FL | Centralized LSTM |
|--------|--------------|---------------|------------------|
| F1 Score | 0.94 | 0.72 | 0.91 |
| Recall | 0.97 | 0.85 | 0.93 |
| False Positive Rate | 0.19 | 0.35 | 0.22 |

- ~30% F1 improvement over standard federated baselines  
- Significant reduction in false positives  
- Stable convergence under extreme label skew  

---

## Non-IID Simulation Framework

10-client partitioning with:

- 90% attack-skewed clients  
- 90% benign-skewed clients  
- Balanced distributions  

FedAvg aggregation maintains convergence even under severe heterogeneity.

---

## Technical Contributions

- Hybrid Digital Twin + Federated Learning architecture  
- Percentile-based anomaly gating mechanism  
- Robust performance under distribution drift  
- Zero-day detection beyond purely supervised FL models  

---

## Research Context

This work addresses three major gaps in IoT cybersecurity:

1. Privacy-preserving learning across heterogeneous edge devices  
2. Robustness degradation under distribution drift  
3. Zero-day attack detection beyond supervised classification  

---

## Repository Structure
literature/
methodology/
experiments/
├── experimental_setup.md
├── results_main.md
└── ablation_study.md


All methodology and experiments are documented for reproducibility.

---

## Manuscript Status

IEEE-format LaTeX draft completed.  
Currently undergoing internal review.
