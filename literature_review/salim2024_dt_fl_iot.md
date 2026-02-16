# Citation Key: Salim2024_DT_FL_IoT

## What problem does it solve?
Combines Digital Twin behavioral modeling with Federated Learning for IoT anomaly detection, addressing privacy concerns in distributed networks.

## Core method
- DT autoencoder learns normal traffic reconstruction patterns
- FL coordinates edge classifiers across heterogeneous devices  
- Simple OR fusion of DT reconstruction + FL predictions
- FedAvg aggregation over 5 communication rounds

## Strengths
- Privacy-preserving through local model updates
- Handles both known attacks + zero-day anomalies

## Limitations
- OR fusion creates excessive false positives
- No percentile-based DT thresholding

## How this repo uses it
Extended their DT-FL concept with **DT-gated AND fusion** (FL ∧ DT) reducing FPR by 81%. Added percentile-normalized reconstruction errors for robust thresholding.

