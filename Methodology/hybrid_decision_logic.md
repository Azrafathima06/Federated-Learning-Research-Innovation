# Hybrid Decision Logic (DT-FL)

## Inputs
```python
p(y|x): FL classifier confidence 
e(x): DT reconstruction error (MSE)
T_p: 95th percentile threshold (benign recon errors)

Decision Rule
IF e(x) > T_p:
    return ANOMALY  // Novel/unknown attack
ELSE:
    return FL_classifier(x)  // Known attack/benign

Threshold Selection
T_p = percentile(benign_recon_errors, 95%)

Key Properties:

Client-agnostic: Percentile normalization

Adaptive: Auto-computes per Digital Twin

Balanced: Recall(0.97) vs FPR(0.01)

