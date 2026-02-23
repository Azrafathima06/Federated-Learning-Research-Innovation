# Hybrid Decision Logic (DT-FL)

## Inputs
python
p(y|x): FL classifier confidence [0,1]
e(x): DT reconstruction error (MSE) 
T_p: 95th percentile threshold (benign recon errors)
Decision Rule (Pseudocode)
text
IF e(x) > T_p:
    return ANOMALY  // Novel/unknown attack
ELSE:
    return FL_classifier(x)  // Known attack/benign
Threshold Selection
text
T_p = percentile(benign_recon_errors, 95%)

