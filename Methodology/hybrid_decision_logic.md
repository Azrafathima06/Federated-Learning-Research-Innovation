Decision Rule
IF e(x) > T_p:
    return ANOMALY  // Novel/unknown attack
ELSE:
    return FL_classifier(x)  // Known attack/benign

Threshold Selection
T_p = percentile(benign_recon_errors, 95%)

Normalizes across client heterogeneity

Balances Recall vs FPR

Auto-adapts per Digital Twin

