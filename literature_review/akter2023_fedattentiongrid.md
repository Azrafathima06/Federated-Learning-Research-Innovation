# Citation Key: Akter2023_FedAttentionGrid

## What problem does it solve?
Federated IDS performance degradation under realistic non-IID client distributions in IoT networks.

## Core method
- Attention-based CNN for network traffic classification
- 5 clients with skewed attack distributions (DDoS-heavy, scan-heavy)
- FedAvg over 10 rounds with local epoch=2 training
- CICIDS2017 dataset partitioning by attack type

## Strengths
- Realistic non-IID evaluation setup
- Attention mechanism improves feature extraction

## Limitations
- No zero-day anomaly detection capability
- FPR remains high (0.72) under drift conditions

## How this repo uses it
Adopted their exact 5-client non-IID setup. Our DT gating reduces their FPR from 0.72 to 0.19 through reconstruction validation.
