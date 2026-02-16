# Citation Key: Gupta_TWINADAPT

## What problem does it solve?
Fixed-threshold anomaly detection fails under varying IoT traffic volumes.

## Core method
- Autoencoder-based Digital Twin for normal traffic modeling
- Percentile-based dynamic thresholding of reconstruction errors
- Adaptive sensitivity control via quantile calibration
- Evaluated on ToN-IoT dataset

## Strengths
- Data-driven threshold avoids manual tuning
- Robust to traffic volume variations

## Limitations
- Unsupervised only, misses known attack signatures
- No federated learning integration

## How this repo uses it
Directly implements their percentile thresholding ($\tau = \text{Percentile}(e_{\text{normal}}, q)$) but gates it with FL predictions for hybrid F1=0.94 performance.
