# Citation Key: Belay2026_DT_CommEff_FedAD

## What problem does it solve?
Communication overhead in federated anomaly detection for resource-constrained IoT.

## Core method
- Compressed model updates between edge + server
- DT reconstruction as communication-efficient anomaly signal
- FedAvg with gradient quantization
- Evaluated under DoS/DDoS scenarios

## Strengths
- Reduces bandwidth 3x vs raw FL
- Good DoS-specific performance

## Limitations
- Limited to specific attack families
- No general non-IID evaluation

## How this repo uses it
Uses their DT reconstruction concept but adds full non-IID evaluation across 5 attack families + normal traffic, achieving broader applicability.
