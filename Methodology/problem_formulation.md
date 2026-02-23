# Problem Formulation (DT-FL IDS)

## Input
- Raw IoT network flows (ToN_IoT dataset)
- Client-partitioned: 10 clients, Non-IID splits
- Features: 44 numerical + 10 categorical [encoded]

## Output  
- Binary anomaly detection: {benign, attack}
- Per-client decisions aggregated centrally

## Objective Metrics
| Metric | Target |
|--------|--------|
| F1-Score | >0.95 |
| Recall | >0.97 |
| FPR | <0.01 |

## Constraints
- **Privacy**: No raw data sharing (FL only)
- **Heterogeneity**: Non-IID client distributions
- **Real-time**: <50ms inference latency
